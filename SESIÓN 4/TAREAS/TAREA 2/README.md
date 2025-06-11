# Segmentación de Clientes con DAX en Power BI

---

## Objetivo de la Tarea

El objetivo de esta tarea es **utilizar funciones DAX en Power BI para segmentar nuestra base de clientes** según criterios específicos. Esto nos permitirá entender mejor sus necesidades y priorizar nuestras acciones de marketing y servicio al cliente.

---

## Instrucciones para la Tarea

### Ejercicio 1: Determinar la Prioridad de los Clientes

En este ejercicio, crearemos una nueva columna en la tabla `Clientes` que indique la prioridad de atención que requiere cada cliente. La prioridad se determinará en base a dos criterios: si el cliente es profesional y soltero, y su nivel de ingreso anual.

**Criterios para Prioridad Alta:**

* El cliente es profesional y soltero.
* El ingreso anual del cliente supera un umbral específico (sugerido **$18K**).

**Resultado esperado:** Una nueva columna que clasifique a cada cliente como de "**Alta**" o "**Normal**" prioridad según los criterios mencionados.

---

### Ejercicio 2: Clasificación del Nivel de Ingresos

El segundo ejercicio consiste en clasificar a los clientes según su nivel de ingresos anuales en categorías predefinidas. Deberán evaluar el ingreso anual de cada cliente y asignar una categoría correspondiente.

**Criterios de Clasificación:**

* Establecer umbrales de ingreso anual para determinar qué constituye un ingreso "**Muy Alto**", "**Alto**", "**Promedio**" y "**Bajo**". Como sugerencia, pueden utilizar **$30K**, **$24K** y **$18K**.

**Resultado esperado:** Una columna adicional en la tabla `Clientes` que muestre la clasificación de ingresos para cada cliente.

---

### Ejercicio 3: Asignación del Grado Universitario

Para el tercer ejercicio, trabajaremos en identificar el nivel educativo máximo alcanzado por cada cliente y asignaremos una etiqueta adecuada.

**Criterios para la Asignación:**

* Basándose en la información educativa proporcionada, clasificarán a los clientes en categorías tales como "**Sin Grado**", "**Grado**" y "**Postgrado**".

**Resultado esperado:** Una columna nueva que refleje el grado universitario máximo identificado para cada cliente en la tabla `Clientes`.

---

## Directrices Generales

* Utilicen **funciones lógicas y de comparación en DAX** para realizar las clasificaciones. Aunque no les proporcionamos el código exacto, recuerden que funciones como `IF` y `SWITCH` serán sus aliadas en estos ejercicios.
* Asegúrense de **validar los resultados** para confirmar que las clasificaciones son lógicas y consistentes con los criterios establecidos.
* Preparen una **breve explicación sobre cómo abordaron cada ejercicio**, incluyendo las decisiones clave que tomaron y cualquier desafío que encontraron.

---

## Preguntas de esta Tarea

* **Comparte tu código DAX para el ejercicio 1:**
* **Comparte tu código DAX para el ejercicio 2:**
* **Comparte tu código DAX para el ejercicio 3:**