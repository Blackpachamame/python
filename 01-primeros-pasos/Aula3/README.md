# Aula 3: Estructuras Condicionales

- [Aula 3: Estructuras Condicionales](#aula-3-estructuras-condicionales)
  - [Operadores Relacionales](#operadores-relacionales)
  - [Tabla de la Verdad](#tabla-de-la-verdad)
    - [Operador `and`](#operador-and)
    - [Operador `or`](#operador-or)
    - [Operador `not`](#operador-not)

## Operadores Relacionales

Una condición es una comparación entre datos que puede dar como resultado **verdadero** o **falso**. Para realizar comparaciones se utilizan los operadores relacionales.

| **Operador** | **Descripción**                                              | **Ejemplo**              | **Salida**                            |
| ------------ | ------------------------------------------------------------ | ------------------------ | ------------------------------------- |
| `>`          | Mayor que: Verdadero si el primer valor es mayor             | `if 10 > 5:`             | ✅ `True` (10 es mayor que 5)          |
| `<`          | Menor que: Verdadero si el primer valor es menor             | `if 3 < 7:`              | ✅ `True` (3 es menor que 7)           |
| `>=`         | Mayor o igual: Verdadero si el primer valor es mayor o igual | `if 8 >= 8:`             | ✅ `True` (8 es igual a 8)             |
| `<=`         | Menor o igual: Verdadero si el primer valor es menor o igual | `if 4 <= 6:`             | ✅ `True` (4 es menor que 6)           |
| `==`         | Igualdad: Verdadero si los valores son iguales               | `if "libro" == "libro":` | ✅ `True` ("libro" es igual a "libro") |
| `!=`         | Diferente de: Verdadero si los valores son distintos         | `if 9 != 5:`             | ✅ `True` (9 es diferente de 5)        |

Ejemplos:
```python
# Comparación de edades
edad_maria = int(input('Ingrese la edad de María: '))
edad_beatriz = int(input('Ingrese la edad de Beatriz: '))

if edad_maria > edad_beatriz:
    print('María es mayor que Beatriz.')

# Comparación de empleados en empresas
empleados_empresa_1 = int(input('Ingrese la cantidad de empleados de la empresa 1: '))
empleados_empresa_2 = int(input('Ingrese la cantidad de empleados de la empresa 2: '))

if empleados_empresa_1 >= empleados_empresa_2:
    print('La empresa 1 tiene una cantidad de empleados mayor o igual a la empresa 2.')
```

## Tabla de la Verdad

Cuando usamos operadores lógicos (`and`, `or`, `not`), es importante entender cómo funcionan a través de la **tabla de la verdad**.

### Operador `and`
El operador `and` devuelve `True` solo si **ambos operandos** son `True`.

| **operando_1** | **operando_2** | **operando_1 and operando_2** |
| -------------- | -------------- | ----------------------------- |
| `False`        | `False`        | `False`                       |
| `False`        | `True`         | `False`                       |
| `True`         | `False`        | `False`                       |
| `True`         | `True`         | `True`                        |

Ejemplo:
```python
llueve = True
tengo_paraguas = False

if llueve and tengo_paraguas:
    print("Puedo salir sin mojarme.")
else:
    print("Me mojaré.")
```

### Operador `or`
El operador `or` devuelve `True` si **al menos uno de los operandos** es `True`.

| **operando_1** | **operando_2** | **operando_1 or operando_2** |
| -------------- | -------------- | ---------------------------- |
| `False`        | `False`        | `False`                      |
| `False`        | `True`         | `True`                       |
| `True`         | `False`        | `True`                       |
| `True`         | `True`         | `True`                       |

Ejemplo:
```python
llueve = False
tengo_paraguas = True

if llueve or tengo_paraguas:
    print("Puedo salir sin problemas.")
else:
    print("No puedo salir sin mojarme.")
```

### Operador `not`
El operador `not` **invierte el valor** del operando.

| **operando** | **not operando** |
| ------------ | ---------------- |
| `True`       | `False`          |
| `False`      | `True`           |

Ejemplo:
```python
es_dia = False

if not es_dia:
    print("Es de noche.")
else:
    print("Es de día.")
```
