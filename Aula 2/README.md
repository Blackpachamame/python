# Aula 2: Manipulando datos en Python

## Comentarios en Python

### Comentarios de una línea
Se escriben utilizando el símbolo `#`. Todo lo que sigue a este símbolo en una línea es ignorado por Python.

Ejemplo:
```python
# Este es un comentario de una línea
```

### Comentarios de varias líneas
Se escriben utilizando comillas triples (`'''` o `"""`) para envolver el comentario.

Ejemplo:
```python
'''
Este es un comentario
de varias líneas.
'''
```

## Operadores Aritméticos

### Exponenciación (`**`)
El operador `**` eleva un número a una potencia específica.

Ejemplo:
```python
2**3  # Resultado: 8
```

### Módulo (`%`)
El operador `%` devuelve el residuo de una división entre dos números.

Ejemplo:
```python
7%3  # Resultado: 1
```

### División entera (`//`)
El operador `//` devuelve solo la parte entera de una división.

Ejemplo:
```python
7//3  # Resultado: 2
```

## Métodos de Formateo de Cadenas

### f-strings
Permiten insertar variables dentro de una cadena utilizando `{}`.

Ejemplo:
```python
nombre = "Ana María"
edad = 17
print(f"El nombre de la alumna es {nombre} y su edad es {edad} años.")
```

### Operador de formateo (`%`)
Utiliza marcadores como `%s` para cadenas, `%d` para enteros, y `%f` para flotantes.

Ejemplo:
```python
nombre_alumno = 'Penélope Camacho'
print('Nombre del alumno: %s' %(nombre_alumno))
```

### `.format()`
Permite insertar variables dentro de una cadena con `{}`.

Ejemplo:
```python
nombre_alumno = 'Penélope Camacho'
print('Nombre del alumno: {}'.format(nombre_alumno))
```

## Caracteres Especiales

- `\n`: Salto de línea.
- `\t`: Tabulación.
- `\\`: Imprime una barra invertida.
- `\"`: Imprime comillas dobles.
- `\'`: Imprime comillas simples.

Ejemplos:
```python
print("Estudiar es un esfuerzo constante,\nEs como cultivar una planta,\nNecesitamos dedicación y paciencia,\nPara ver madurar el fruto.")
print('Cantidad\tCalidad\n5 muestras\tAlta\n3 muestras\tBaja')
print("Ruta del archivo: C:\\archivos\\documento.csv")
print("Una vez oí: \"Los frutos del conocimiento son los más dulces y duraderos de todos.\"")
print('Mi profesora una vez dijo: \'Estudiar es la clave del éxito.\'')
```
```