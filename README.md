# ar-manejo-ciclos-python

# Uso de `break` y `continue` en Python

## 📌 Introducción
En Python, `break` y `continue` son dos instrucciones que alteran el flujo de un bucle. Ambas se utilizan dentro de estructuras iterativas como `for` y `while`, pero con efectos diferentes:

- **`break`**: Detiene completamente la ejecución del bucle cuando se cumple una condición.
- **`continue`**: Omite una iteración específica, pero el bucle continúa con las siguientes.

Este documento explora cómo funcionan ambas instrucciones con un ejemplo donde `i` es elevado al cuadrado (`i**2`).

---

## 🔴 Código 1: Uso de `break`
```python
"""
Uso de break
"""

for i in range(1, 11):
    if i == 5:
        break
    print(i ** 2)
```

### **Explicación**
1. Se inicia un bucle `for` desde `i = 1` hasta `i = 10`.
2. Se verifica si `i == 5`.
3. Si `i == 5`, se ejecuta `break`, lo que **detiene el bucle inmediatamente**.
4. Solo se imprimen los valores antes de `i = 5`.

### **Salida esperada**
```
1
4
9
16
```

✅ El `break` interrumpe el bucle completamente cuando `i == 5`, por lo que **no se imprimen valores para `i = 5` en adelante**.

---

## 🟢 Código 2: Uso de `continue`
```python
"""
Uso de continue
"""

for i in range(1, 11):
    if i == 5:
        continue
    print(i ** 2)
```

### **Explicación**
1. Se inicia un bucle `for` desde `i = 1` hasta `i = 10`.
2. Se verifica si `i == 5`.
3. Si `i == 5`, se ejecuta `continue`, lo que **omite solo esta iteración y pasa a la siguiente**.
4. Se imprimen todos los valores excepto `i = 5`.

### **Salida esperada**
```
1
4
9
16
36
49
64
81
100
```

✅ Con `continue`, **se omite `i = 5`, pero el bucle sigue ejecutándose hasta `i = 10`**.

---

## 🔎 Comparación Final
| **Característica** | `break` | `continue` |
|--------------------|---------|------------|
| **Efecto en el bucle** | Detiene completamente el bucle. | Omite solo la iteración actual y sigue con las demás. |
| **Cuándo usarlo** | Cuando queremos **salir del bucle** en una condición. | Cuando queremos **saltar una iteración específica**, pero seguir con el bucle. |
| **Salida esperada** | `1, 4, 9, 16` (el bucle termina en `i == 5`). | `1, 4, 9, 16, 36, 49, 64, 81, 100` (se omite solo `i == 5`). |

---

## 💡 **Conclusión**
- **`break`** → **Detiene el bucle por completo** cuando `i == 5`, por lo que **solo imprime hasta `i = 4`**.
- **`continue`** → **Salta la iteración cuando `i == 5`**, pero sigue ejecutándose para `i = 6` en adelante.

Estas instrucciones son útiles cuando se necesita **controlar el flujo de ejecución de un bucle**. Su correcta aplicación puede mejorar la eficiencia y claridad del código en diversas situaciones.

---
