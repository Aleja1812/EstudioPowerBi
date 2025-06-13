# SESIÓN 4 - CALCULANDO CAMPOS CON DAX

---

Esta carpeta contiene las **tareas** proporcionadas por el instructor, específicamente para las clases correspondientes a la **SESIÓN 4 - CALCULANDO CAMPOS CON DAX**.

---

## ¿Qué hay en cada carpeta?

* 📁 **TAREA 1**:

# Tarea: Tasa de Devoluciones en Power BI (DAX)

Esta tarea te guiará en la creación de una medida de **Tasa de Devoluciones de Ciclo de Vida en Power BI** usando dos métodos DAX distintos: el operador de división (`/`) y la función `DIVIDE`.

---

## Objetivos Clave

El objetivo es aprender a calcular y manejar errores en medidas DAX:

1.  **Crear medidas de Tasa de Devoluciones**:
    * Una con el **operador de división** (`[Cantidad Devuelta] / [Cantidad Vendida]`).
    * Otra con la **función `DIVIDE`** (`DIVIDE([Cantidad Devuelta], [Cantidad Vendida], 0)`) para manejar la división por cero.
2.  **Comparar resultados**: Observar cómo cada método gestiona los escenarios de división por cero en una matriz.
3.  **Reflexionar sobre manejo de errores**: Comprender la importancia de la función `DIVIDE` para la robustez y fiabilidad de los informes.

---

## Entregable (Opcional)

* Una imagen de tu matriz comparando los resultados de ambas medidas.

---

Esta tarea es fundamental para **crear medidas DAX robustas y evitar errores en tus análisis** de Power BI.

* 📁 **TAREA 2**:

# Tarea: Segmentación de Clientes con DAX en Power BI

Esta tarea se enfoca en **segmentar la base de clientes de Power BI utilizando funciones DAX** para categorizarlos según su prioridad, nivel de ingresos y grado universitario.

---

## Objetivos Clave

El objetivo es aplicar DAX para crear nuevas columnas de segmentación en la tabla `Clientes`:

1.  **Prioridad del Cliente**: Clasificar clientes como "Alta" o "Normal" según si son profesionales, solteros y su ingreso anual (ej. >$18K).
2.  **Clasificación de Ingresos**: Asignar categorías de ingreso (ej. "Muy Alto", "Alto", "Promedio", "Bajo") basándose en umbrales definidos (ej. $30K, $24K, $18K).
3.  **Asignación de Grado Universitario**: Etiquetar el nivel educativo máximo (ej. "Sin Grado", "Grado", "Postgrado").

---

## Entregable

* El código DAX utilizado para cada uno de los tres ejercicios.

---

Esta tarea es fundamental para **personalizar estrategias de marketing y servicio al cliente** al comprender mejor las características de la base de clientes.

* 📁 **TAREA 3**:

# Tarea: Extracción de Segmentos de SKU en Power BI con DAX

Esta tarea se enfoca en **extraer la porción de texto a la derecha del primer guión de los SKUs** en Power BI, utilizando DAX para manejar la variabilidad en la longitud y posición del guión.

---

## Objetivo Clave

El objetivo es **manipular cadenas de texto con DAX** para:

1.  **Encontrar dinámicamente** la posición del primer guión (`-`) en la columna `SKU`.
2.  **Calcular la longitud** del segmento de texto a extraer a la derecha del guión.
3.  **Extraer** dicho segmento para crear una nueva columna en la tabla `Productos`.

---

## El Reto

El desafío principal es la **variabilidad de los SKUs**, lo que requiere una solución DAX flexible que no dependa de posiciones fijas.

---

## Pistas DAX

Considera funciones que te permitan:
* **Identificar** la posición de un carácter.
* **Calcular** longitudes de texto.
* **Extraer** partes de una cadena desde el final.

---

## Entregable

* El código DAX utilizado para la solución.

---

Esta tarea es fundamental para **afinar tus habilidades en la manipulación avanzada de cadenas de texto en DAX**, crucial para la preparación de datos.


* 📁 **TAREA 4**:

# Tarea: Análisis de la Tasa de Devoluciones de Accesorios (DAX)

Esta tarea se enfoca en **analizar la tasa de devoluciones para la categoría de accesorios en Estados Unidos** usando la función `CALCULATE` en Power BI.

---

## Objetivos Clave

El objetivo es calcular y analizar métricas específicas con DAX:

1.  **Calcular Total de Devoluciones de Accesorios**: Crea una medida para sumar devoluciones solo para la categoría "Accesorios" y el mercado de "Estados Unidos".
2.  **Calcular Total de Ventas de Accesorios**: Crea una medida similar para sumar las ventas bajo los mismos filtros.
3.  **Calcular Tasa de Devoluciones**: Divide las devoluciones entre las ventas de accesorios y formatea el resultado como porcentaje.

---

## Contexto y Entregables

* El análisis busca entender la alta tasa de devoluciones de accesorios en EE. UU.
* **Entregables**: Una imagen de la matriz de resultados en Power BI y un breve análisis con hallazgos y recomendaciones para el departamento de finanzas.

---

Esta tarea es fundamental para **aplicar `CALCULATE` en DAX para análisis de contexto específicos** y generar *insights* accionables.

* 📁 **TAREA 5**:

# Tarea: Análisis de Devoluciones por Categoría de Producto en Power BI

Este proyecto demuestra el uso de **DAX avanzado en Power BI** para analizar el comportamiento de las devoluciones, enfocándose en la **contribución porcentual de cada categoría de producto** al total global de devoluciones.

---

## Objetivos Clave

El objetivo es utilizar funciones DAX como `CALCULATE`, `ALL` y `DIVIDE` para:

1.  **Calcular el total global de devoluciones**: Obtener la suma total de devoluciones sin considerar filtros de categoría.
2.  **Estimar el porcentaje de devoluciones por categoría**: Determinar qué porcentaje del total de devoluciones representa cada categoría de producto.
3.  **Visualizar los porcentajes**: Mostrar estos porcentajes en una matriz para identificar las categorías con mayor impacto en las devoluciones.

---

## Pasos del Análisis (Ejemplo de Código DAX)

## 1. Calcular el Total de Todas las Devoluciones

Esta medida (`Todas las Devoluciones`) es crucial porque nos permite obtener el total de devoluciones **sin importar los filtros** que se apliquen en el informe (por ejemplo, si estamos viendo devoluciones por una categoría específica, esta medida seguirá mostrando el total global). Actuará como el denominador para calcular porcentajes más adelante.

**Código DAX:**

**```dax
Todas las Devoluciones =
CALCULATE (
    [Total Devoluciones], // Suma el total de devoluciones.
    ALL ( Devoluciones )  // Elimina cualquier filtro de la tabla 'Devoluciones' para obtener el total general.
)

---

* 📁 **TAREA 6**:

# Tarea: Análisis de Medidas y Matrices en Power BI

Esta tarea se enfoca en **crear medidas DAX clave y dos matrices en Power BI** para analizar el rendimiento empresarial, incluyendo el cálculo de metas y tendencias recientes.

---

## Objetivos Clave

El objetivo es desarrollar habilidades en DAX y visualización con matrices:

1.  **Crear Medidas DAX**:
    * Calcular **Devoluciones, Órdenes y Utilidad Bruta del Mes Anterior**.
    * Establecer **Metas de Órdenes y Utilidad Bruta** (5% de incremento sobre el mes anterior).
    * Calcular la **Utilidad Bruta de los Últimos 90 Días**.
2.  **Construir Matrices**:
    * **Primera Matriz**: Muestra métricas del mes anterior y sus metas por "Inicio de Mes".
    * **Segunda Matriz**: Visualiza la "Utilidad Bruta de los Últimos 90 Días" por "Fechas Diarias".

---

## Entregables

* Una captura de pantalla de la **primera matriz**.
* El **código DAX** para la medida "Utilidad Bruta de los Últimos 90 Días".

---

Esta tarea es fundamental para **analizar el rendimiento empresarial, establecer metas y detectar tendencias** usando las potentes capacidades de DAX y Power BI.