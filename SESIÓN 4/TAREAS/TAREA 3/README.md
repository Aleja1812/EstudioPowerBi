# Extracción de Segmentos de SKU en Power BI con DAX

---

## Objetivo de la Tarea

La tarea consiste en **extraer y aislar la porción de texto que se encuentra a la derecha del primer guión** en los SKUs de productos almacenados en la columna `SKU` de nuestra tabla `Productos` en Power BI. Este ejercicio desafía tu habilidad para manipular cadenas de texto en DAX, aplicando una solución que se ajuste a variaciones en la longitud del SKU y en la posición del guión.

---

## El Reto

El principal reto en esta tarea es la **variabilidad**. Los SKUs de nuestros productos no siguen un patrón fijo; la cantidad de caracteres antes y después del guión puede variar significativamente de un SKU a otro. Además, la posición del guión dentro del SKU no es constante, lo que impide el uso directo de funciones como `RIGHT` sin un cálculo previo que determine dónde cortar la cadena de texto.

---

## Hints para Abordar el Problema

1.  **Identificación del Guión:**
    Necesitarás encontrar la posición exacta del guión (`-`) dentro de cada SKU. Reflexiona sobre qué función DAX te permite buscar un carácter específico dentro de una cadena de texto y devuelve su posición.

2.  **Cálculo Dinámico de la Longitud:**
    Una vez conocida la posición del guión, el siguiente paso es determinar cuántos caracteres necesitas extraer a partir de este punto. Piensa en cómo puedes utilizar la longitud total del SKU para calcular dinámicamente el número de caracteres a extraer.

3.  **Extracción del Texto:**
    Con la posición del guión y la cantidad necesaria de caracteres a extraer claras, considera qué función te permite seleccionar una porción específica de texto de una cadena, comenzando desde el final hacia el inicio.

---

## Directrices Generales

* La solución debe ser **flexible** y adaptarse a cualquier longitud de SKU, así como a cualquier posición del guión dentro de este.
* Considera las funciones de DAX que has aprendido hasta ahora que te permiten **manipular cadenas de texto y buscar dentro de ellas**.
* Asegúrate de **probar tu solución con varios SKUs de ejemplo** para validar su efectividad.

---

## Preguntas de esta Tarea

* **Comparte tu código en DAX:**