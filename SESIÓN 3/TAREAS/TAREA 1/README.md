# Tarea: Modelado de Datos y Relaciones en Power BI - Caso "Ciclo Vida"

Esta tarea se enfoca en el modelado de datos y la manipulación de relaciones entre tablas en Power BI, utilizando el caso de estudio "Ciclo Vida". Se requiere ejecutar los siguientes pasos de manera detallada y ordenada para reforzar la comprensión sobre la estructura de modelos de datos.

## 1. Eliminar todas las relaciones existentes

Como primer paso crucial, deben asegurarse de que el modelo de datos esté completamente limpio de cualquier relación previamente establecida.

* **Acceder al panel de relaciones y eliminar manualmente cada conexión existente entre las tablas.**

    *Este proceso es fundamental para evitar conflictos o inconsistencias al establecer las nuevas estructuras de datos propuestas.*

## 2. Crear un esquema Estrella

Una vez que el modelo esté limpio, el siguiente paso consiste en configurar un esquema Estrella.

* **Conectar las tablas de `ventas`, `calendario`, `clientes`, `productos` y `territorio` de tal manera que la tabla de `ventas` funcione como tabla de hechos central.**
* **El resto de tablas (`calendario`, `clientes`, `productos`, `territorio`) actuarán como tablas de dimensiones.**

    *Este esquema facilita análisis complejos al centralizar los datos transaccionales y relacionarlos con diversas dimensiones.*

## 3. Establecer un esquema Copo de Nieve

Posteriormente, deberán avanzar hacia la creación de un esquema Copo de Nieve. Este esquema se caracteriza por su capacidad de detallar aún más la estructura de datos al vincular las tres tablas de dimensiones de productos (`producto`, `subcategoría de producto` y `categoría de producto`) entre sí.

* **Vincular las tablas `producto`, `subcategoría de producto` y `categoría de producto` entre sí.**

    *Este paso permite una segmentación más fina de los datos, optimizando el análisis específico de los productos.*

    **(Nota: Construya el esquema de Copo de Nieve a partir del esquema de Estrella elaborado en el paso anterior; el entregable final no deben de ser dos esquemas aislados sino uno sólo).**

## 4. Utilizar la vista de informe para la verificación

Finalmente, para confirmar la correcta implementación y funcionalidad de los esquemas establecidos, implementarán un filtro en la vista de informe.

* **Implementar un filtro que filtre la Suma de `CantidadOrden` a partir de diferentes campos de las tablas de dimensiones.**

    *Con este último paso, verificarán que es posible filtrar las cantidades de pedidos utilizando campos de cada una de las tablas de dimensiones. Esto es crucial para asegurar que las relaciones entre tablas se han configurado correctamente y que el modelo de datos refleja de manera precisa las interacciones entre las diferentes dimensiones y los hechos.*

    ## Entregable

Como parte de la culminación de esta tarea, se solicita compartir una imagen de su **esquema final**. Esta imagen debe reflejar claramente las relaciones establecidas entre las tablas, evidenciando tanto el esquema Estrella como el esquema Copo de Nieve implementados (una sola imagen). Esta visualización servirá como prueba de su capacidad para manejar y estructurar modelos de datos complejos dentro de Power BI.

Les insto a abordar esta tarea con la seriedad y el rigor que requiere, aprovechando la oportunidad para profundizar en sus habilidades analíticas y técnicas en el manejo de Power BI. Estoy seguro de que esta experiencia contribuirá significativamente a su desarrollo profesional en el ámbito del análisis de datos.

## Preguntas de esta tarea

1.  Comparta una imagen de tu esquema: