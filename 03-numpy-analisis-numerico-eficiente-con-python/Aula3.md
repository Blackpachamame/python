## Diferencia entre arrays y ajuste con línea recta

Al observar series temporales (como el precio mensual de manzanas en Moscú), una forma simple de describir su comportamiento general es mediante una **línea recta**. Esta línea se define con la ecuación:

```text
y = ax + b
```

Donde:
- `x` representa el tiempo (meses),
- `a` es la pendiente (crecimiento promedio por mes),
- `b` es el valor de intersección con el eje Y (valor inicial estimado).

Podemos graficar tanto los valores reales (`moscu`) como la línea estimada (`y`):

```python
x = fechas
y = 0.5 * x + 78

plt.plot(x, moscu)
plt.plot(x, y)
plt.title("Comparación entre valores reales y línea estimada")
plt.show()
```

Luego, analizamos la diferencia entre `moscu` y `y`:

```python
diferencia = moscu - y
```

Para cuantificar qué tan buena es la aproximación, usamos la **norma del error**, calculando la raíz cuadrada del error cuadrático total:

```python
np.sqrt(np.sum(np.power(diferencia, 2)))
```

También se puede calcular de forma más elegante con:

```python
np.linalg.norm(moscu - y)
```

## Regresión lineal desde cero con NumPy

En lugar de ajustar la pendiente "a ojo", podemos calcularla con una fórmula basada en álgebra lineal. Si `x` son las fechas y `y` los precios:

```python
N = np.size(x)
a = (N * np.sum(x * y) - np.sum(x) * np.sum(y)) / (N * np.sum(x**2) - (np.sum(x))**2)
b = np.mean(y) - a * np.mean(x)
```

La recta resultante `y = a * x + b` es la que **mejor ajusta** el conjunto de datos en términos de regresión lineal simple.

## Aplicación práctica de la regresión

Una vez que obtenemos `a` y `b`, podemos estimar precios para cualquier mes:

```python
mes_25 = a * 25 + b
mes_75 = a * 75 + b
```

Y visualizarlo:

```python
plt.plot(x, moscu)
plt.plot(x, a * x + b)
plt.plot(25, mes_25, "r*")
plt.plot(75, mes_75, "r*")
```

Esto permite **predecir valores** en fechas intermedias y analizar tendencias. Aunque se puede probar con modelos más complejos, como polinomios de orden superior, se debe tener cuidado con el **sobreajuste (overfitting)**.