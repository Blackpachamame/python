# Aula 5: Estructuras de Datos

- [Aula 5: Estructuras de Datos](#aula-5-estructuras-de-datos)
  - [Strings: Una secuencia de caracteres](#strings-una-secuencia-de-caracteres)
    - [**Conversión de Strings a Listas**](#conversión-de-strings-a-listas)
    - [**Conversión de Listas a Strings**](#conversión-de-listas-a-strings)
  - [Manipulación de Listas](#manipulación-de-listas)
  - [Listas en Diccionarios](#listas-en-diccionarios)
  - [Funciones Incorporadas](#funciones-incorporadas)
    - [**`sum()` - Sumar elementos de una lista**](#sum---sumar-elementos-de-una-lista)
    - [**`help()` - Consultar documentación**](#help---consultar-documentación)
    - [**`dir()` - Listar atributos y métodos de un objeto**](#dir---listar-atributos-y-métodos-de-un-objeto)

## Strings: Una secuencia de caracteres
Las cadenas de texto (**strings**) son secuencias de caracteres indexadas. Cada carácter en una cadena tiene un índice, comenzando en `0` para el primer carácter y en `-1` para el último.

Ejemplo:
```python
lenguaje = 'Python'
print(lenguaje[0], lenguaje[1], lenguaje[2], lenguaje[-3], lenguaje[-2], lenguaje[-1])
```
**Salida:**  
`P y t h o n`

📌 **Importante:** Las cadenas son **inmutables**, lo que significa que **no se pueden modificar directamente** como una lista.

### **Conversión de Strings a Listas**
Podemos convertir una cadena en una lista utilizando el método `.split()`.  
Si especificamos un delimitador, la cadena se dividirá en base a él; si no se especifica, se divide por espacios.

```python
pregunta = '¿Quién vino primero? ¿El huevo? ¿O fue la serpiente?'
lista_palabras = pregunta.split('?')
print(lista_palabras)
```
**Salida:**  
`['¿Quién vino primero', ' ¿El huevo', ' ¿O fue la serpiente', '']`

Si no se define un delimitador:
```python
lista_palabras = pregunta.split()
print(lista_palabras)
```
**Salida:**  
`['¿Quién', 'vino', 'primero?', '¿El', 'huevo?', '¿O', 'fue', 'la', 'serpiente?']`

### **Conversión de Listas a Strings**
Para unir los elementos de una lista en una cadena, usamos `.join()`.

```python
mezclas = ['Rojo y azul: morado', 'Rojo y amarillo: naranja', 'Azul y amarillo: verde']
resultado = '. '.join(mezclas)
print(resultado)
```
**Salida:**  
`Rojo y azul: morado. Rojo y amarillo: naranja. Azul y amarillo: verde`

## Manipulación de Listas
Las listas permiten almacenar múltiples valores en una sola variable y ofrecen diversos métodos para manipular sus elementos.

Ejemplo base:
```python
razas_de_perros = ['Labrador Retriever', 'Bulldog Francés', 'Pastor Alemán', 'Poodle']
```

| **Método**     | **Descripción**                                   | **Ejemplo**                                     |
| -------------- | ------------------------------------------------- | ----------------------------------------------- |
| `insert(i, x)` | Inserta `x` en la posición `i`                    | `razas_de_perros.insert(1, 'Golden Retriever')` |
| `append(x)`    | Agrega `x` al final de la lista                   | `razas_de_perros.append('Beagle')`              |
| `pop(i)`       | Elimina y devuelve el elemento en la posición `i` | `razas_de_perros.pop(1)`                        |
| `index(x)`     | Devuelve el índice de `x` en la lista             | `razas_de_perros.index('Pastor Alemán')`        |
| `sort()`       | Ordena la lista en orden ascendente               | `razas_de_perros.sort()`                        |

Ejemplo:
```python
razas_de_perros.insert(1, 'Golden Retriever')
print(razas_de_perros)
```
**Salida:**  
`['Labrador Retriever', 'Golden Retriever', 'Bulldog Francés', 'Pastor Alemán', 'Poodle']`

## Listas en Diccionarios
Podemos almacenar listas dentro de un diccionario, lo que nos permite asociar múltiples valores a una misma clave.

Ejemplo:
```python
tienda = {
    'nombres': ['televisión', 'celular', 'notebook', 'heladera', 'estufa'],
    'precios': [2000, 1500, 3500, 4000, 1500]
}

for clave, elementos in tienda.items():
    print(f'Clave: {clave}\nElementos:')
    for dato in elementos:
        print(dato)
```
**Salida:**  
```
Clave: nombres
Elementos:
televisión
celular
notebook
heladera
estufa

Clave: precios
Elementos:
2000
1500
3500
4000
1500
```
También podemos modificar los valores dentro del diccionario:
```python
tienda['nombres'].append('microondas')
tienda['precios'].append(1200)
```

## Funciones Incorporadas
Python proporciona varias funciones predefinidas que facilitan la manipulación de datos.

### **`sum()` - Sumar elementos de una lista**
```python
precios = [100.0, 400.0, 200.0]
total = sum(precios)
print(total)  # Salida: 700.0
```

### **`help()` - Consultar documentación**
```python
help(print)
```
Muestra la documentación de `print()`.

### **`dir()` - Listar atributos y métodos de un objeto**
```python
lista = [1, 2, 3]
print(dir(lista))
```
**Salida:**  
Muestra todos los métodos disponibles para listas (`append`, `pop`, `sort`, etc.).