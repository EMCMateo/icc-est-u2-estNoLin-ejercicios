
# Algoritmos de Árboles Binarios

## 📌 Información General
- **Título:** Implementación de Algoritmos de Árboles Binarios  
- **Asignatura:** Estructura de Datos  
- **Carrera:** Computación  
- **Estudiantes:** Mateo Molina  
- **Fecha:** 6 de julio del 2025  
- **Profesor:** Ing. Pablo Torres  

---

## 🔍 Descripción del Proyecto

Este proyecto contiene la resolución de una práctica guiada basada en el uso de **árboles binarios**, abordando problemas clásicos de estructuras no lineales. Cada ejercicio fue diseñado para explorar y comprender operaciones esenciales sobre árboles binarios, desarrolladas en el lenguaje **Java**:

- **Inserción ordenada en un árbol de búsqueda** (BST)
- **Transformación estructural de un árbol** mediante inversión
- **Agrupación de nodos por niveles** utilizando recorrido BFS
- **Determinación de la profundidad máxima** en la estructura

Cada solución fue implementada pensando en la claridad del algoritmo, su eficiencia y facilidad de comprensión, siguiendo buenas prácticas de programación orientada a objetos.

---

## 🚀 Instrucciones para Ejecutar

1. Verifica tener Java 11 o superior instalado en tu sistema.
2. Desde la raíz del proyecto, compila usando:
   ```bash
   javac -cp ".:lib/*" src/main/App.java
   ```
3. Ejecuta el programa con:
   ```bash
   java -cp ".:lib/*:src" main.App
   ```

Para pruebas (si aplicas JUnit):
```bash
java -cp ".:lib/*:src" org.junit.runner.JUnitCore test.Ejercicio_01_insert.InsertBSTTest
```

---

## 📁 Estructura del Proyecto

```
src/
├── main/
│   ├── App.java                          # Clase principal
│   ├── Ejercicio_01_insert/
│   │   └── InsertBST.java               # Inserción en BST
│   ├── Ejercicio_02_invert/
│   │   └── InvertBinaryTree.java        # Inversión de árbol
│   ├── Ejercicio_03_listLeves/
│   │   └── ListLevels.java              # Listado por niveles
│   ├── Ejercicio_04_depth/
│   │   └── Depth.java                   # Cálculo de profundidad
│   └── Materia/
│       ├── Controllers/
│       │   ├── AVLTree.java             # Árbol AVL auto-balanceado
│       │   ├── ArbolBinario.java        # Árbol binario básico
│       │   └── ArbolRecorridos.java     # Métodos de recorrido
│       └── Models/
│           └── Node.java                # Clase nodo del árbol
└── test/
    └── [Pruebas unitarias para cada ejercicio]
```

---

## ⚙️ Detalle de Implementación

### 🟢 Ejercicio 01: Árbol Binario de Búsqueda (BST)
Se implementó una inserción recursiva que asegura que los valores menores se ubiquen en el subárbol izquierdo y los mayores en el derecho. Esta lógica permite mantener ordenados los datos, optimizando búsquedas futuras. Se imprimió el recorrido **in-order** para evidenciar la correcta colocación de los nodos.

**Ejemplo de entrada:** `[5, 3, 7, 2, 4, 6, 8]`  
**Salida esperada (in-order):** `2, 3, 4, 5, 6, 7, 8`

---

### 🔁 Ejercicio 02: Inversión del Árbol Binario
La inversión del árbol se realizó aplicando recursión para intercambiar los nodos izquierdo y derecho en cada nivel. Esta técnica es muy útil para comprender el recorrido post-order y permite modificar la forma del árbol conservando la jerarquía.

**Entrada:**
```
    4
   2 7
  1 3 6 9
```
**Salida esperada (invertido):**
```
    4
   7 2
  9 6 3 1
```

---

### 🧩 Ejercicio 03: Listado por Niveles
A través de una cola (estructura FIFO), se implementó un recorrido en anchura (BFS) para agrupar los nodos por niveles. Se simula la representación de listas enlazadas imprimiendo los valores con flechas.

**Salida esperada:**
```
Nivel 1: 4  
Nivel 2: 2 -> 7  
Nivel 3: 1 -> 3 -> 6 -> 9
```

---

### 📏 Ejercicio 04: Cálculo de Profundidad
Mediante recursividad, se calculó el camino más largo desde la raíz hasta un nodo hoja. Se utilizó un árbol específico que permite verificar una profundidad de exactamente 4, tal como lo pide la guía.

**Ejemplo:**
```
    4
   2 7
  1 3
8
```
**Resultado:** `4`

---

## 🖥️ Salida en Consola

```
👤 Estudiante: Mateo Molina
✉️  Correo: mmolinac10@est.ups.edu.ec

🔧 EJERCICIO 01 - Árbol Binario de Búsqueda (Insertar nodos)
🌿 Árbol BST (InOrder): 2, 3, 4, 5, 6, 7, 8,

🔄 EJERCICIO 02 - Árbol Binario Invertido
🪞 Árbol Invertido (InOrder): 9, 7, 6, 4, 3, 2, 1,

📋 EJERCICIO 03 - Niveles del Árbol (Listas enlazadas simuladas)
Nivel 1: 4  
Nivel 2: 2 -> 7  
Nivel 3: 1 -> 3 -> 6 -> 9

📏 EJERCICIO 04 - Profundidad máxima del árbol  
🔢 Profundidad máxima: 4
```

---

## 📈 Rendimiento y Análisis

| Algoritmo                           RE| Tiempo  | Tiempo (Peor caso) | Espacio     |
|---------------------------|-------------------|---------------------|-------------|
| Inserción BST             | O(log n)          | O(n)                | O(h)        |
| Inversión de árbol        | O(n)              | O(n)                | O(h)        |
| Listado por niveles (BFS) | O(n)              | O(n)                | O(n)        |
| Profundidad máxima        | O(n)              | O(n)                | O(h)        |



## ✅ Reflexiones Finales

Esta práctica permitió reforzar los conceptos de árboles binarios mediante problemas de aplicación directa. Al realizar la inserción, inversión, recorrido y análisis de profundidad, se desarrolló una comprensión sólida de cómo manipular estas estructuras jerárquicas.

Cada solución fue pensada para mejorar la lógica recursiva, el manejo de estructuras auxiliares como colas, y para representar la información de forma ordenada en consola. La correcta estructuración del código por carpetas también facilitó la reutilización de clases y métodos.

En conjunto, estos ejercicios son clave para comprender cómo se almacena y procesa información de forma no lineal, lo cual es esencial en muchas aplicaciones reales de la computación.

---

## 🧩 Requisitos Técnicos

- Java JDK 11 o superior  
- (Opcional) JUnit 5 para realizar pruebas automatizadas  
- No se utilizó ninguna librería externa adicional
