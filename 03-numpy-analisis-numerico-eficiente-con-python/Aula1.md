## Visualización y selección

### Notación de segmento (Slice Notation) ✂️

Permite acceder a porciones específicas de un array de forma similar a las listas.  
Por ejemplo, para obtener la primera columna de una matriz:

```python
fechas = datos[:, 0]  # Todas las filas, columna 0
```

Y para obtener desde la segunda columna en adelante (por ejemplo, precios):

```python
precios = datos[:, 1:]  # Todas las filas, desde la columna 1
```

### np.arange() 📅

La función `np.arange(inicio, fin, paso)` genera secuencias de números.  
Es útil para crear un eje temporal artificial cuando no contamos con fechas reales bien formateadas.

**Ejemplo**:

```python
fechas = np.arange(1, 88)  # Del 1 al 87, representando meses
```

Esto es útil para graficar series temporales cuando queremos ver la evolución de un dato (como precios de manzanas en varias ciudades) a lo largo del tiempo.

### Visualización de datos con Matplotlib 📉

Aunque NumPy no genera gráficos por sí solo, puede integrarse con **Matplotlib** para visualizar datos:

```python
import matplotlib.pyplot as plt

plt.plot(fechas, precios[:, 0])  # Precios de Moscú
plt.title("Precio de manzanas en Moscú")
plt.xlabel("Mes")
plt.ylabel("Precio")
plt.show()
```

## Comparación entre arrays y análisis estacional

Una vez que tenemos nuestros datos de precios organizados por ciudad y por mes, es posible **comparar el comportamiento de los precios entre distintos años**, para detectar patrones estacionales o tendencias relevantes.

### Análisis por año 📊

Podemos dividir el array de una ciudad en porciones de 12 meses (1 año) usando slice notation:

```python
moscu_1 = moscu[0:12]    # Año 2013
moscu_2 = moscu[12:24]   # Año 2014
moscu_3 = moscu[24:36]   # Año 2015
moscu_4 = moscu[36:48]   # Año 2016
```

Esto nos permite **graficar cada año por separado**, facilitando la comparación visual:

```python
meses = np.arange(1, 13)

plt.plot(meses, moscu_1)
plt.plot(meses, moscu_2)
plt.plot(meses, moscu_3)
plt.plot(meses, moscu_4)
plt.legend(["2013", "2014", "2015", "2016"])
plt.title("Precios mensuales de manzanas en Moscú")
plt.xlabel("Mes")
plt.ylabel("Precio (Rublos)")
plt.show()
```

### Comparación de arrays 🔍

NumPy permite comparar arrays de diferentes maneras:

- ✅ `np.array_equal(arr1, arr2)`: retorna `True` si ambos arrays son **exactamente iguales**.
- 🔍 `np.allclose(arr1, arr2, atol=x)`: permite comparar si los arrays son **aproximadamente iguales**, tolerando una diferencia `x` (por ejemplo, 2 rublos).

**Ejemplo:**

```python
np.array_equal(moscu_1, moscu_2)      # False
np.allclose(moscu_1, moscu_2, atol=2) # True (si la diferencia es ≤ 2 rublos)
```

Perfecto, Claudio. Aquí tenés el **resumen integrado** de esta sección sobre tratamiento de valores faltantes (NaN), en línea con los resúmenes anteriores:

## Tratamiento de NaN

Al trabajar con datos reales, es común encontrar valores faltantes representados como **NaN** ("Not a Number"). Estos pueden interferir en cálculos estadísticos, como el promedio, y deben ser tratados adecuadamente.

### ¿Cómo detectar un NaN? 🔍

Si al calcular el promedio obtenemos `np.mean(array)` y devuelve `nan`, es probable que haya uno o más valores faltantes.

Podemos identificarlos con:

```python
np.isnan(Kaliningrado)         # Devuelve un array booleano
np.sum(np.isnan(Kaliningrado)) # Cuenta cuántos NaN hay
```

Cada `True` equivale a un valor NaN.

### ¿Cómo reemplazar un NaN? 🔧

Una técnica común es la **interpolación**: reemplazar el NaN con el promedio del valor anterior y posterior:

```python
valor_interp = (Kaliningrado[3] + Kaliningrado[5]) / 2
Kaliningrado[4] = valor_interp
```

Esto elimina el NaN y permite continuar con los cálculos:

```python
np.mean(Kaliningrado)  # Ya devuelve un valor válido
```

### Gráficos después del tratamiento ✅

Una vez corregido el NaN, el gráfico de la ciudad se visualiza correctamente:

```python
plt.plot(fechas, Kaliningrado)
plt.title("Precios de manzanas en Kaliningrado (sin NaN)")
plt.xlabel("Mes")
plt.ylabel("Precio (Rublos)")
plt.show()
```