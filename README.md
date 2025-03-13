# Python
Aquí colocare lo aprendido y la resolución de los desafíos de las clases de Python.

## Índice de Aulas
1. [Aula 1: Comenzando con Python](Aula%201/Readme.md)
2. [Aula 2: Manipulando Datos en Python](Aula%202/Readme.md)
3. [Aula 3: Estructuras Condicionales](Aula%203/Readme.md)
4. [Aula 4: Estructuras de Repetición](Aula%204/Readme.md)
5. [Aula 5: Estructuras de Datos](Aula%205/Readme.md)

## Índice de Equivalencias entre Python y JavaScript
1. [Conceptos Básicos](#1-conceptos-básicos)
2. [Operaciones y Conversión de Tipos](#2-operaciones-y-conversión-de-tipos)
3. [Condicionales y Bucles](#3-condicionales-y-bucles)
4. [Strings y sus Métodos](#4-strings-y-sus-métodos)
5. [Listas/Arrays y sus Métodos](#5-listasarrays-y-sus-métodos)
6. [Diccionarios/Objetos](#6-diccionariosobjetos)
7. [Funciones](#7-funciones)

### 1. Conceptos Básicos
| **Concepto**                     | **Python**                                       | **JavaScript**                                      |
|----------------------------------|--------------------------------------------------|-----------------------------------------------------|
| **Impresión en consola**         | `print("Texto")`                                 | `console.log("Texto")`                              |
| **Entrada del usuario**          | `input("Ingresa algo: ")`                        | `prompt("Ingresa algo: ")`                          |
| **Comentario de una línea**      | `# Comentario`                                   | `// Comentario`                                     |
| **Comentario de varias líneas**  | `""" Comentario multilínea """`                  | `/* Comentario multilínea */`                       |
| **Booleanos**                    | `True`, `False`                                  | `true`, `false`                                     |
| **Nombres de variables**         | `snake_case` (ej. `lista_estudiantes`)           | `camelCase` (ej. `listaEstudiantes`)                |
| **Tipos de datos simples**       | `str`, `int`, `float`, `bool`, `None`            | `string`, `number`, `boolean`, `null`, `undefined`  |
| **Tipos de datos compuestos**    | `list`, `dict`, `set`, `tuple`                   | `array`, `object`, `set`, `Map`                     |
| **Comprobación de tipo de variable** | `type(x)`                                    | `typeof x`                                          |

### 2. Operaciones y Conversión de Tipos
| **Operación**                    | **Python**                                       | **JavaScript**                                      |
|----------------------------------|--------------------------------------------------|-----------------------------------------------------|
| **Suma**                         | `a + b`                                          | `a + b`                                            |
| **Resta**                        | `a - b`                                          | `a - b`                                            |
| **Multiplicación**               | `a * b`                                          | `a * b`                                            |
| **División**                     | `a / b`                                          | `a / b`                                            |
| **División entera**              | `a // b`                                         | `Math.floor(a / b)`                                |
| **Módulo (resto de división)**   | `a % b`                                          | `a % b`                                            |
| **Exponente**                    | `a ** b`                                         | `Math.pow(a, b)` o `a ** b` (ES6)                  |
| **Convertir a entero**           | `int(valor)`                                     | `parseInt(valor)`                                   |
| **Convertir a flotante**         | `float(valor)`                                   | `parseFloat(valor)`                                |
| **Convertir a string**           | `str(valor)`                                     | `String(valor)` o `valor.toString()`               |

### 3. Condicionales y Bucles
| **Estructura**                   | **Python**                                       | **JavaScript**                                      |
|----------------------------------|--------------------------------------------------|-----------------------------------------------------|
| **Condicional `if`**             | `if condición:`                                  | `if (condición) { ... }`                            |
| **Condicional `elif`**           | `elif condición:`                                | `else if (condición) { ... }`                       |
| **Condicional `else`**           | `else:`                                         | `else { ... }`                                      |
| **Bucle `for` (rango de valores)**| `for i in range(5):`                             | `for (let i = 0; i < 5; i++) { ... }`               |
| **Bucle `for` (iterar sobre lista)** | `for item in lista:`                             | `for (let item of lista) { ... }`                   |
| **Bucle `while`**                | `while condición:`                               | `while (condición) { ... }`                         |
| **Bucle `forEach` en listas**    | `for item in lista:`                             | `lista.forEach(item => { ... })`                    |

### 4. Strings y sus Métodos
| **Método**                        | **Python**                                       | **JavaScript**                                      |
|----------------------------------|--------------------------------------------------|-----------------------------------------------------|
| **Concatenar cadenas**          | `"Hola " + "mundo"`                             | `"Hola " + "mundo"` o `` `Hola ${mundo}` ``        |
| **Longitud de una cadena**      | `len(texto)`                                    | `texto.length`                                     |
| **Convertir a mayúsculas**      | `texto.upper()`                                 | `texto.toUpperCase()`                              |
| **Convertir a minúsculas**      | `texto.lower()`                                 | `texto.toLowerCase()`                              |
| **Reemplazar subcadenas**       | `texto.replace("viejo", "nuevo")`               | `texto.replace("viejo", "nuevo")`                  |
| **Separar una cadena**          | `texto.split(",")`                              | `texto.split(",")`                                 |
| **Eliminar espacios laterales** | `texto.strip()`                                 | `texto.trim()`                                     |
| **Verificar si una cadena contiene otra** | `"mundo" in texto`                      | `texto.includes("mundo")`                          |

### 5. Listas/Arrays y sus Métodos
| **Método**                        | **Python (`list`)**                             | **JavaScript (`Array`)**                           |
|----------------------------------|--------------------------------------------------|-----------------------------------------------------|
| **Crear una lista/array**        | `lista = [1, 2, 3]`                            | `let lista = [1, 2, 3]`                            |
| **Longitud de una lista**        | `len(lista)`                                    | `lista.length`                                     |
| **Agregar un elemento al final** | `lista.append(4)`                               | `lista.push(4)`                                    |
| **Eliminar el último elemento**  | `lista.pop()`                                   | `lista.pop()`                                      |
| **Agregar un elemento al inicio** | `lista.insert(0, 0)`                           | `lista.unshift(0)`                                 |
| **Eliminar el primer elemento**  | `lista.pop(0)`                                  | `lista.shift()`                                    |
| **Revertir una lista**           | `lista.reverse()`                              | `lista.reverse()`                                  |
| **Ordenar una lista**            | `lista.sort()`                                 | `lista.sort()` (alfabético) / `lista.sort((a, b) => a - b)` (numérico) |
| **Filtrar una lista**            | `list(filter(lambda x: x > 2, lista))`         | `lista.filter(x => x > 2)`                         |
| **Mapear una lista**             | `list(map(lambda x: x * 2, lista))`            | `lista.map(x => x * 2)`                            |

### 6. Diccionarios/Objetos
| **Método**                        | **Python (`dict`)**                             | **JavaScript (`Object`)**                          |
|----------------------------------|--------------------------------------------------|-----------------------------------------------------|
| **Crear un diccionario/objeto** | `diccionario = {"key": "value"}`                | `let objeto = { key: "value" }`                    |
| **Obtener valor por clave**      | `diccionario["key"]`                            | `objeto.key` o `objeto["key"]`                     |
| **Agregar un par clave-valor**   | `diccionario["nuevo"] = "valor"`                | `objeto.nuevo = "valor"`                           |
| **Eliminar una clave**           | `del diccionario["key"]`                        | `delete objeto.key`                                |
| **Obtener todas las claves**     | `diccionario.keys()`                            | `Object.keys(objeto)`                              |
| **Obtener todos los valores**    | `diccionario.values()`                          | `Object.values(objeto)`                            |
| **Verificar existencia de clave** | `"key" in diccionario`                         | `"key" in objeto`                                  |

### 7. Funciones
| **Concepto**                     | **Python**                                       | **JavaScript**                                      |
|----------------------------------|--------------------------------------------------|-----------------------------------------------------|
| **Definir una función**          | `def funcion():`                                | `function funcion() { ... }`                        |
| **Llamar una función**           | `funcion()`                                     | `funcion()`                                        |
| **Parámetros en funciones**      | `def suma(a, b): return a + b`                 | `function suma(a, b) { return a + b; }`            |
| **Funciones lambda**             | `lambda x: x + 1`                               | `(x) => x + 1`                                     |

