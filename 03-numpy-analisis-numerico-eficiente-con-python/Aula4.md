## Generación de números aleatorios

NumPy permite generar números aleatorios, útiles para simulaciones, pruebas y modelado estadístico.

### 🔢 Números enteros aleatorios

```python
np.random.randint(40, 100, size=100)  # 100 enteros entre 40 y 100
````

### 🔢 Números decimales aleatorios (float)

```python
np.random.uniform(0.1, 0.9, size=100)  # 100 valores decimales entre 0.1 y 0.9
```

Podemos usarlos para probar múltiples pendientes en una regresión y evaluar cuál minimiza el error con `np.linalg.norm`.

## Evaluación automática de normas

Para encontrar la mejor pendiente en una regresión lineal:

```python
pendientes = np.random.uniform(0.1, 0.9, size=100)
normas = np.array([])

for i in range(100):
    y_pred = pendientes[i] * x + b
    error = np.linalg.norm(moscu - y_pred)
    normas = np.append(normas, error)
```

Esto guarda la norma (error) para cada pendiente generada.

## Reproductibilidad 🔁

NumPy genera **números pseudoaleatorios**, por lo que es posible hacerlos reproducibles usando una semilla:

```python
np.random.seed(99)  # Fija la semilla
np.random.uniform(0.1, 0.9, size=5)  # Siempre dará los mismos valores
```

> 🧠 Importante: si no se fija la semilla, los valores cambiarán en cada ejecución.

## Exportación de arrays

Es posible guardar arrays de NumPy en archivos `.csv` usando `np.savetxt`:

### 📦 Crear datos combinados:

```python
datos = np.column_stack((normas, pendientes))
```

### 💾 Guardar archivo `.csv`:

```python
np.savetxt("normas_y_pendientes.csv", datos, delimiter=",")
```

Esto exporta una tabla de 100 filas por 2 columnas, que podés abrir con cualquier editor de texto o Excel.