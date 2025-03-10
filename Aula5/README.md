# Aula 5: Resumen - Estructuras de Datos

## Índice
- [Aula 5: Resumen - Estructuras de Datos](#aula-5-resumen---estructuras-de-datos)
  - [Índice](#índice)
  - [Strings](#strings)
    - [Conversión de Strings a Listas](#conversión-de-strings-a-listas)
    - [Conversión de Listas a Strings](#conversión-de-listas-a-strings)
  - [Manipulación de Listas](#manipulación-de-listas)
    - [Acceder al último elemento](#acceder-al-último-elemento)
    - [Invertir una lista](#invertir-una-lista)
  - [Listas en Diccionarios](#listas-en-diccionarios)
  - [Funciones Incorporadas](#funciones-incorporadas)
    - [sum() - Sumar elementos](#sum---sumar-elementos)
    - [len() - Obtener la longitud](#len---obtener-la-longitud)
    - [range() - Generar secuencias](#range---generar-secuencias)
    - [all() - Verificar valores](#all---verificar-valores)

## Strings
Las **cadenas de texto (strings)** son secuencias de caracteres **indexadas**.  

```python
texto = "Python"
print(texto[0], texto[-1])  # Salida: P n
```
📌 **Los strings son inmutables**, por lo que **no se pueden modificar directamente**.

### Conversión de Strings a Listas
El método `.split()` divide un string en una lista usando un separador.

```python
frase = "Hola, ¿cómo estás?"
palabras = frase.split()  # Divide por espacios
print(palabras)  # ['Hola,', '¿cómo', 'estás?']
```

### Conversión de Listas a Strings
El método `.join()` une los elementos de una lista en un string.

```python
colores = ["Rojo", "Verde", "Azul"]
resultado = ", ".join(colores)
print(resultado)  # "Rojo, Verde, Azul"
```

---

## Manipulación de Listas
Las **listas** permiten almacenar múltiples valores y ofrecen métodos útiles.

| Método          | Descripción                           | Ejemplo                   |
| --------------- | ------------------------------------- | ------------------------- |
| `.append(x)`    | Agrega `x` al final                   | `lista.append(10)`        |
| `.insert(i, x)` | Inserta `x` en la posición `i`        | `lista.insert(1, "Hola")` |
| `.pop(i)`       | Elimina y devuelve `i`-ésimo elemento | `lista.pop(2)`            |
| `.sort()`       | Ordena la lista en orden ascendente   | `lista.sort()`            |
| `.reverse()`    | Invierte el orden de la lista         | `lista.reverse()`         |

### Acceder al último elemento
Usamos índices negativos para acceder a los elementos desde el final.

```python
numeros = [10, 20, 30, 40, 50]
print(numeros[-1])  # Salida: 50
```

### Invertir una lista
Varias formas de invertir una lista:
```python
# Con slicing
print(lista[::-1])  

# Con .reverse() (modifica la lista original)
lista.reverse()

# Con reversed() (devuelve un iterador)
print(list(reversed(lista)))
```

---

## Listas en Diccionarios
Las listas pueden almacenarse dentro de diccionarios para estructurar mejor los datos.

```python
tienda = {
    "productos": ["Laptop", "Teléfono", "Tablet"],
    "precios": [1500, 700, 1200]
}
```

Podemos recorrer los datos con un bucle:
```python
for clave, valores in tienda.items():
    print(f"{clave}: {valores}")
```

---

## Funciones Incorporadas

### sum() - Sumar elementos
Calcula la suma de los elementos en un iterable.
```python
numeros = [10, 20, 30]
print(sum(numeros))  # Salida: 60
```

### len() - Obtener la longitud
Devuelve la cantidad de elementos en una lista, string o tupla.
```python
nombres = ["Ana", "Carlos", "María"]
print(len(nombres))  # Salida: 3
```

### range() - Generar secuencias
Crea una secuencia de números, útil en bucles.
```python
for i in range(1, 6):
    print(i)  # Salida: 1, 2, 3, 4, 5
```

### all() - Verificar valores
Retorna `True` si **todos los elementos** en un iterable son `True`.
```python
numeros = [2, 3, 5, 7]
print(all(n % d != 0 for d in range(2, n)))  # Verifica si n es primo
```