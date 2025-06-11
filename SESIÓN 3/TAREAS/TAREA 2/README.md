# Tarea: Análisis y Solución de Registros Faltantes en Power BI

En esta tarea, deberás analizar la falta de algunos registros `IDTerritorio` en la matriz de Power BI y proponer una solución a largo plazo. La solución debe implicar **ocultar claves foráneas para asegurar el uso correcto de las claves principales**.

# Análisis y Propuesta de Solución para Anomalías en Matriz Power BI

Se les presenta la siguiente imagen de una Matriz en la Vista de Informe de Power BI, donde se observan anomalías en los datos mostrados:

| IDTerritorio | Suma de CantidadOrden | Suma de CantidadDevuelta |
| :----------- | :-------------------- | :------------------------ |
| 1            | 77211                 | 270                       |
| 4            | 79528                 | 362                       |
| 5            | 795                   | 1                         |
| 6            | 74631                 | 238                       |
| 7            | 75370                 | 186                       |
| 8            | 71830                 | 163                       |
| 9            | 81250                 | 404                       |
| 10           | 76402                 | 204                       |
| **Total** | **84174** | **1828** |

Su tarea consistirá en dos partes fundamentales:

## 1. Análisis de la situación:

* **Describan qué podría estar causando la ausencia de filas para ciertos IDTerritorio en la matriz (específicamente filas 2 y 3).** Consideren que los pedidos fueron enviados a estos territorios y, por lo tanto, deberían estar reflejados en el informe.
* **Expliquen por qué la Suma de CantidadOrden no parece coherente, especialmente en relación con el total mostrado de 84,174.** Reflexionen sobre la posibilidad de errores en la integración de los datos o en la configuración del modelo de datos que podría estar llevando a una suma incorrecta.

## 2. Propuesta de solución a largo plazo:

* **Basándose en lo aprendido en la sesión "Ocultando Campos de la Vista de Informes", propongan una solución para evitar que tales incongruencias sucedan en el futuro.**
* **Consideren prácticas de modelado de datos como la correcta relación entre tablas, la integridad de las claves foráneas y primarias, y la importancia de ocultar campos que no deben usarse para filtrar en la Vista de Informe.**

**Pista:** Reflexionen sobre la sesión mencionada y cómo ocultar ciertos campos podría prevenir que se filtren utilizando campos incorrectos o inadecuados, lo que podría llevar a resultados no esperados como los vistos en la imagen.

## Preguntas de esta tarea

1.  Describan qué podría estar causando la ausencia de filas para ciertos IDTerritorio en la matriz.
2.  Basándose en lo aprendido en la sesión "Ocultando Campos de la Vista de Informes", propongan una solución para evitar que tales incongruencias sucedan en el futuro.

# SOLUCIÓN DE LA TAREA # 2 - SESIÓN 3

## 1. Describan qué podría estar causando la ausencia de filas para ciertos IDTerritorio en la matriz.

La ausencia de filas para IDTerritorio 2 y 3 en la matriz se debe principalmente a:

* **Filtros Activos:** Hay filtros a nivel de informe, página o visual que excluyen estos territorios (ej., segmentaciones, filtros en panel de filtros).
* **Ausencia de Datos Filtrados:** Bajo el contexto de filtro actual (ej., rango de fechas), no hay registros de `CantidadOrden` o `CantidadDevuelta` para IDTerritorio 2 y 3 en la tabla de hechos. Si no hay datos, no se muestra la fila.
* **Problemas de Relaciones o Datos:** Posibles relaciones incorrectas o inactivas entre tablas, o que los IDTerritorio 2 y 3 no existan o no coincidan correctamente entre la tabla de hechos y la tabla de dimensión.
* **Uso de Campo Incorrecto:** Se está usando el `IDTerritorio` de la tabla de hechos (que solo lista IDs con datos) en lugar del `IDTerritorio` de la tabla de dimensión (que lista todos los IDs posibles).

La **incoherencia del total (84,174)** se debe a que este suma los datos bajo un contexto de filtro más amplio que las filas visibles. El total incluye `CantidadOrden` de territorios no mostrados en la matriz (como el 2 y el 3), por lo que la suma de las filas visibles no coincide con el total general.

## 2. Basándose en lo aprendido en la sesión "Ocultando Campos de la Vista de Informes", propongan una solución para evitar que tales incongruencias sucedan en el futuro.

Para evitar futuras incongruencias, la solución se centra en un modelado de datos robusto y la gestión de la visibilidad de los campos:

### *. Modelado de Datos Estructurado (Esquema Estrella):

* **Separar Hechos y Dimensiones:** Asegurar tablas de hechos (ej., `FactVentas`) con métricas y claves foráneas, y tablas de dimensión (ej., `DimTerritorio`) con atributos descriptivos y claves primarias.
* **Relaciones 1:N Claras:** Establecer relaciones activas de uno a varios desde las tablas de dimensión hacia las tablas de hechos (ej., `DimTerritorio[IDTerritorio]` a `FactVentas[IDTerritorio]`).

### *. Ocultar Claves Foráneas de Tablas de Hechos:

* **Acción:** En la **Vista de Modelo** o **Vista de Datos**, haz clic derecho sobre las columnas de claves foráneas en las tablas de hechos (ej., `FactVentas[IDTerritorio]`) y selecciona "Ocultar en vista de informe".
* **Beneficio:** Esto fuerza a los usuarios a arrastrar y utilizar los campos de los **tablas de dimensión** (ej., `DimTerritorio[IDTerritorio]` o `DimTerritorio[NombreTerritorio]`) en los objetos visuales. Esto garantiza que el objeto visual use el contexto completo de la dimensión, mostrando todos los territorios posibles (incluso si no tienen datos, si así se configura la matriz) y asegurando que los filtros y totales se calculen correctamente a través de las relaciones del modelo.

