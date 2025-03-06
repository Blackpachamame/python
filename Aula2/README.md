# Aula 2: Manipulando datos en Python

## Índice
1. [Comentarios en Python](#comentarios-en-python)
2. [Operadores aritméticos](#operadores-aritméticos)
3. [Métodos de formateo de cadenas](#métodos-de-formateo-de-cadenas)
4. [Caracteres especiales](#caracteres-especiales)

## Comentarios en Python

### Comentarios de una línea
Se escriben utilizando el símbolo `#`. Todo lo que sigue después del `#` es ignorado por Python.

```python
# Este es un comentario de una línea
print("Hola, mundo")  # También se pueden usar al final de una línea de código
```

### Comentarios de varias líneas
Para escribir comentarios largos, se pueden usar **comillas triples** (`'''` o `"""`).

```python
"""
Este es un comentario
de varias líneas.
"""
```

---

## Operadores Aritméticos
Los operadores aritméticos permiten realizar operaciones matemáticas en Python.

| **Operador** | **Descripción**               | **Ejemplo** | **Resultado** |
| ------------ | ----------------------------- | ----------- | ------------- |
| `+`          | Suma                          | `5 + 3`     | `8`           |
| `-`          | Resta                         | `10 - 4`    | `6`           |
| `*`          | Multiplicación                | `6 * 2`     | `12`          |
| `/`          | División                      | `7 / 2`     | `3.5`         |
| `//`         | División entera               | `7 // 2`    | `2`           |
| `%`          | Módulo (resto de la división) | `7 % 3`     | `1`           |
| `**`         | Exponenciación (potencia)     | `2**3`      | `8`           |

---

## Métodos de Formateo de Cadenas

### f-strings (Python 3.6+)
Permiten insertar variables dentro de una cadena de forma sencilla.

```python
nombre = "Ana María"
edad = 17
print(f"El nombre de la alumna es {nombre} y su edad es {edad} años.")
```

### Operador de formateo (`%`)
Utiliza marcadores como `%s` (cadenas), `%d` (enteros) y `%f` (flotantes).

```python
nombre_alumno = 'Penélope Camacho'
print('Nombre del alumno: %s' % (nombre_alumno))
```

### Método `.format()`
Permite insertar variables usando `{}` como marcadores de posición.

```python
nombre_alumno = 'Penélope Camacho'
print('Nombre del alumno: {}'.format(nombre_alumno))
```

---

## Caracteres Especiales
Los caracteres especiales permiten agregar formato o caracteres reservados dentro de las cadenas.

| **Carácter** | **Descripción**                   | **Ejemplo**                                  | **Salida**                      |
| ------------ | --------------------------------- | -------------------------------------------- | ------------------------------- |
| `\n`         | Salto de línea                    | `print("Hola\nMundo")`                       | Hola <br> Mundo                 |
| `\t`         | Tabulación                        | `print("Hola\tMundo")`                       | Hola    Mundo                   |
| `\\`         | Barra invertida `\`               | `print("Ruta: C:\\archivos\\documento.csv")` | Ruta: C:\archivos\documento.csv |
| `\"`         | Comillas dobles dentro de string  | `print("Dijo: \"Hola Mundo\"")`              | Dijo: "Hola Mundo"              |
| `\'`         | Comillas simples dentro de string | `print('Dijo: \'Hola Mundo\'')`              | Dijo: 'Hola Mundo'              |

### Ejemplos de uso:
```python
print("Estudiar es un esfuerzo constante,\nEs como cultivar una planta,\nNecesitamos dedicación y paciencia,\nPara ver madurar el fruto.")

print('Cantidad\tCalidad\n5 muestras\tAlta\n3 muestras\tBaja')

print("Ruta del archivo: C:\\archivos\\documento.csv")

print("Una vez oí: \"Los frutos del conocimiento son los más dulces y duraderos de todos.\"")

print('Mi profesora una vez dijo: \'Estudiar es la clave del éxito.\'')
```