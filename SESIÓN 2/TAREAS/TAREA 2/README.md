## Objetivo:

Practicar la habilidad de extracción de datos web utilizando Power BI, enfocándonos en los precios mensuales de las acciones de Tesla (TSLA) durante los últimos 5 años.

## Instrucciones:

### Acceso a los Datos:

1.  Abre Power BI y selecciona "Obtener Datos" > "Web".
2.  Ingresa la URL de investing.com donde se muestran los precios históricos de Tesla, o la página web de tu elección que contenga una tabla.
3.  Utiliza el conector Web para navegar y seleccionar la tabla de precios mensuales de las acciones.

### Asegurar Encabezados Correctos:

4.  Verifica los encabezados: Una vez que los datos estén cargados en el Editor de Power Query, verifica si la primera fila se utiliza como encabezados de columnas. Si no es así, selecciona "Usar Primera Fila Como Encabezados" en la pestaña "Inicio".

### Asignación de Tipos de Datos:

5.  Asigna el tipo de dato correcto: Para cada columna, asegúrate de asignar el tipo de dato correcto (por ejemplo, fecha, número entero, decimal para precios, texto para identificadores). Esto se hace seleccionando la columna, luego en la pestaña "Transformar", elige "Tipo de Dato" y selecciona el tipo correspondiente.

### Remover Filas con Splits:

6.  Agregar una columna de índice: Si tu conjunto de datos incluye filas que indican eventos de "splits" de acciones y deseas excluirlos, primero agrega una columna de índice: Ve a "Agregar Columna" > "Índice de Columna" > "Desde 1".
7.  Filtra las filas no deseadas: Utiliza esta columna para identificar y filtrar las filas que no necesitas. Esto se hace seleccionando el filtro en la cabecera de la columna de índice y excluyendo los índices correspondientes a eventos de split.

### Filtrado de Datos No Deseados:

8.  Crea una columna ID si es necesario para identificar de manera única cada fila. Utiliza esta columna para filtrar cualquier dato que no sea relevante para tu análisis, incluyendo las filas de splits mencionadas anteriormente.

### Filtrado de Datos No Deseados:

8.  Crea una columna ID si es necesario para identificar de manera única cada fila. Utiliza esta columna para filtrar cualquier dato que no sea relevante para tu análisis, incluyendo las filas de splits mencionadas anteriormente.

### Aplicar Cambios:

9.  Aplica los cambios: Una vez completadas las transformaciones, aplica los cambios y carga los datos a Power BI para su análisis.

### Consejos Adicionales:

* Si te encuentras con dificultades para extraer directamente los datos de investing.com, recuerda que el objetivo es practicar la extracción web. Puedes elegir otra tabla web que sea más accesible.
* Aprovecha los recursos en línea y la documentación de Power BI para explorar más detalles sobre la extracción de datos y las transformaciones en Power Query.

### Recordatorio:

Las tareas son completamente opcionales y están diseñadas para tu aprendizaje. No tienen calificación ni influyen para obtener el certificado de participación. Para futuras preguntas, por favor usa el foro de preguntas y respuestas del curso. Así, cumplimos con las políticas de la plataforma y otros estudiantes también pueden beneficiarse de las respuestas.
Espero que esta información te sea de ayuda. ¡Mucho éxito en tu aprendizaje!

## Preguntas de esta tarea

1.  Comparte una imagen de la Vista de Tabla TESLA en Power BI