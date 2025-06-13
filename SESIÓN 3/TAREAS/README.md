# SESIÓN 3 - CREANDO UN MÓDELO DE DATOS

---

Esta carpeta contiene las **tareas** proporcionadas por el instructor, específicamente para las clases correspondientes a la **SESIÓN 3 - CREANDO UN MÓDELO DE DATOS**.

---

## ¿Qué hay en cada carpeta?

# * 📁 **TAREA 1**:

### Tarea: Modelado de Datos en Power BI (Caso "Ciclo Vida")

Esta tarea te guiará en la **creación y verificación de un modelo de datos robusto en Power BI** usando el caso "Ciclo Vida".

---

## Objetivos Clave

El objetivo es dominar el modelado de datos en Power BI mediante estos pasos:

1.  **Limpiar el modelo**: Elimina todas las relaciones existentes para empezar de cero.
2.  **Crear un esquema Estrella**: Conecta la tabla central de hechos (`ventas`) con tablas de dimensiones (`calendario`, `clientes`, `productos`, `territorio`).
3.  **Establecer un esquema Copo de Nieve**: Expande la dimensión de `productos` vinculando `producto`, `subcategoría de producto` y `categoría de producto`. ¡Este se construye sobre el esquema Estrella, no es separado!
4.  **Verificar la funcionalidad**: Comprueba que las relaciones funcionan correctamente filtrando datos (como la `CantidadOrden`) desde las tablas de dimensiones en el informe.

---

## Entregable

* Una imagen de tu **esquema final** que muestre claramente la combinación de los esquemas Estrella y Copo de Nieve.

---

Esta tarea es clave para afianzar tus habilidades en la estructuración de datos para análisis en Power BI.

---

En resumen, el objetivo principal es que el estudiante **domine el modelado de datos en Power BI construyendo y verificando un esquema combinado de Estrella y Copo de Nieve**, asegurando así la precisión de las relaciones de datos para un análisis robusto.

# * 📁 **TAREA 2**:

### Tarea: Resolver Anomalías en Power BI (IDTerritorio)

Esta tarea se enfoca en **diagnosticar y solucionar la ausencia de datos en una matriz de Power BI**, específicamente la falta de `IDTerritorio` y totales inconsistentes.

---

## Objetivo Principal

El objetivo es **garantizar la precisión de los datos en los informes de Power BI** mediante:

1.  **Análisis de la situación**: Identificar la causa de los datos faltantes y las sumas incoherentes (posibles filtros, datos ausentes o uso incorrecto de campos).
2.  **Propuesta de solución a largo plazo**: Implementar un **modelado de datos robusto (esquema Estrella)** y, crucialmente, **ocultar las claves foráneas** de las tablas de hechos en la vista de informe. Esto fuerza el uso de las claves principales de las tablas de dimensión, asegurando que todos los territorios se muestren correctamente y que los cálculos sean precisos.

---

En resumen, la tarea busca que **domines la corrección y prevención de inconsistencias en informes de Power BI** mediante la aplicación de buenas prácticas de modelado de datos y gestión de la visibilidad de los campos.

# * 📁 **TAREA 3**:

### Tarea: Creación y Aplicación de Jerarquías de Fechas en Power BI

Esta tarea te guiará en la **creación de una jerarquía de fechas personalizada en Power BI** y su uso para analizar tendencias temporales en un visual de matriz.

---

## Objetivos Clave

El objetivo es dominar la creación y aplicación de jerarquías de fecha:

1.  **Preparar campos**: Genera campos de `Año`, `Trimestre` y `Nombre del Mes` en el editor de consultas.
2.  **Crear jerarquía personalizada**: Forma una jerarquía llamada "Jerarquía de Fecha" usando estos campos en el orden lógico (Año > Trimestre > Mes).
3.  **Implementar en informe**: Usa la jerarquía en las filas de una matriz con `CantidadOrden` y `CantidadDevuelta` en las columnas. Practica el "drilling" para explorar los niveles temporales.

---

## Entregable

* Una imagen de tu matriz mostrando la jerarquía de fechas aplicada con `CantidadOrden` y `CantidadDevuelta`.

---

Esta tarea es fundamental para el **análisis de series temporales** y para revelar *insights* significativos a través de la estructuración lógica de los datos.
