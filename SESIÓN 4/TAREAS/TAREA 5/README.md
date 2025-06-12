# Análisis de Devoluciones por Categoría de Producto en Power BI

Este proyecto demuestra la aplicación de conceptos avanzados de DAX (Data Analysis Expressions) en Power BI para analizar el comportamiento de las devoluciones de productos dentro de una empresa, con un enfoque en la contribución porcentual de cada categoría de producto al total de devoluciones.

## Objetivo de la Tarea

Utilizar funciones DAX como `CALCULATE`, `ALL`, y `DIVIDE` para:
1. Calcular el total global de devoluciones.
2. Estimar el porcentaje de devoluciones que cada categoría de producto representa sobre el total global.
3. Visualizar estos porcentajes en una matriz para identificar categorías con un impacto significativo en las devoluciones.

---

## Pasos para el Análisis

Sigue las siguientes instrucciones paso a paso para replicar el análisis:

### 1. Calcular el Total de Todas las Devoluciones

Esta medida actuará como el denominador para calcular el porcentaje de devoluciones por categoría, asegurando que se consideren todas las devoluciones sin importar los filtros de categoría aplicados en el informe.

**Instrucciones:**
* Crea una nueva medida en Power BI.
* Utiliza la función `CALCULATE` para sumar el `[Total Devoluciones]`.
* Emplea `ALL(Devoluciones)` como modificador de filtro dentro de `CALCULATE` para ignorar cualquier filtro aplicado a la tabla `Devoluciones` y considerar todas las devoluciones existentes.
* Nombra esta medida como `Todas las Devoluciones`.

**Código DAX:**

```dax
Todas las Devoluciones =
CALCULATE (
    [Total Devoluciones],
    ALL ( Devoluciones ) // Asume que 'Devoluciones' es el nombre de tu tabla de hechos de devoluciones o una tabla relevante. Si 'Total Devoluciones' ya es una medida, 'ALL(Devoluciones)' eliminaría los filtros de columna sobre 'Devoluciones'. Si 'Total Devoluciones' se basa en otra tabla (ej. Ventas), ajusta 'ALL' a esa tabla.
)