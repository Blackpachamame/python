# Aula 4: Estructuras de Repetición

- [Aula 4: Estructuras de Repetición](#aula-4-estructuras-de-repetición)
  - [Operadores de Atribución](#operadores-de-atribución)
  - [Comandos de Control](#comandos-de-control)
    - [**continue**](#continue)
    - [**break**](#break)

## Operadores de Atribución
Los operadores de asignación permiten modificar el valor de una variable de forma más concisa.  
El operador básico es `=`, que asigna un valor a una variable, pero existen otros operadores que combinan la asignación con operaciones matemáticas.

| **Operador** | **Descripción**                                   | **Ejemplo** | **Salida**   |
| ------------ | ------------------------------------------------- | ----------- | ------------ |
| `=`          | Asignación simple                                 | `x = 10`    | `x = 10`     |
| `+=`         | Suma y asigna el resultado                        | `x += 5`    | `x = x + 5`  |
| `-=`         | Resta y asigna el resultado                       | `x -= 3`    | `x = x - 3`  |
| `*=`         | Multiplica y asigna el resultado                  | `x *= 2`    | `x = x * 2`  |
| `/=`         | Divide y asigna el resultado                      | `x /= 4`    | `x = x / 4`  |
| `//=`        | Realiza una división entera y asigna el resultado | `x //= 6`   | `x = x // 6` |
| `%=`         | Calcula el módulo y asigna el resultado           | `x %= 5`    | `x = x % 5`  |

Ejemplo:
```python
precio = 2.00
precio += 3
print(precio)  # Salida: 5.0
```

## Comandos de Control
Cuando trabajamos con bucles, a veces es necesario **controlar su flujo de ejecución** para saltar iteraciones o finalizar el bucle antes de tiempo.  
Los comandos `continue` y `break` nos permiten hacer esto.

### **continue**
El comando `continue` **salta** la iteración actual y pasa a la siguiente, sin ejecutar el código restante en esa vuelta del bucle.

Ejemplo:
```python
for i in range(1, 6):
    if i == 4:
        continue
    print(i)
```
**Salida:**  
```
1
2
3
5
```
Cuando `i == 4`, `continue` omite la ejecución de `print(i)`, por lo que el número 4 no se muestra.

### **break**
El comando `break` **finaliza** el bucle de inmediato, deteniendo todas las iteraciones restantes.

Ejemplo:
```python
for i in range(1, 6):
    if i == 4:
        break
    print(i)
```
**Salida:**  
```
1
2
3
```
Cuando `i == 4`, `break` detiene completamente el bucle y no se ejecutan más iteraciones.