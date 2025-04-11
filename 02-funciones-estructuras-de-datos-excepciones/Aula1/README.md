# 📚 Bibliotecas en Python: pip, PyPI e importaciones

## 🛠️ pip y PyPI

### ¿Qué es pip?
- Es el **administrador de paquetes de Python**.
- Permite **instalar, actualizar y eliminar** bibliotecas desde la línea de comandos.
- Se conecta con **PyPI (Python Package Index)**, el repositorio central de bibliotecas Python.

### Ejemplo para ver los paquetes instalados en Colab:
```python
!pip list
```

### ¿Qué es PyPI?
- Es el **repositorio oficial de paquetes Python**.
- Mantenido por la **Python Software Foundation**.
- Contiene **miles de bibliotecas** para instalar con pip.

---

## 📦 Formas de importar paquetes

### 1. `import nombre_biblioteca`
- Importa **toda la biblioteca**.
- Ejemplo:
```python
import math
print(math.sqrt(9))
```

### 2. `from nombre_biblioteca import metodo`
- Importa **un solo método** de una biblioteca.
- Ventajas:
  - Ahorra memoria.
  - Mejora la claridad del código.
  - Reduce conflictos de nombres.
  - Puede acelerar el tiempo de ejecución.

#### Ejemplo:
```python
from math import sqrt
print(sqrt(9))
```

### 3. `from nombre_biblioteca import met_1, met_2`
- Importa **varios métodos** específicos.
- Ejemplo con la biblioteca `random`:
```python
from random import randrange, sample

lista = []
for i in range(20):
    lista.append(randrange(100))

print(sample(lista, 5))
```

### 4. `from nombre_biblioteca import *`
- Importa **todos los métodos** directamente (sin usar el prefijo del nombre de la biblioteca).
- Ejemplo:
```python
from math import *
print(sqrt(16))  # No se necesita usar math.sqrt
```

> ⚠️ **Cuidado con esta forma**:
> - Puede haber **conflictos de nombres**.
> - **Disminuye la claridad** del origen de las funciones.
> - Puede **cargar funciones innecesarias**, afectando el rendimiento.