# Tasa de Devoluciones de Ciclo de Vida en Power BI

Este README te guiará en la creación de una medida en Power BI para calcular la **Tasa de Devoluciones de Ciclo de Vida** usando dos métodos diferentes en DAX: el operador de división (`/`) y la función `DIVIDE`.

---
## Método 1: Operador de División `/`

Este método es el más directo y utiliza el operador de división estándar.

### Pasos:

1.  **Abre tu reporte de Power BI:** Asegúrate de tener el reporte con tus datos de ventas abierto.
2.  **Crea una nueva medida:**
    * Ve a la pestaña **Modelado**.
    * Selecciona **"Nueva medida"**.
3.  **Nombra la medida:** Asígnale el nombre `Tasa de Devoluciones Op/`.
4.  **Ingresa la fórmula DAX:**
    ```dax
    Tasa de Devoluciones Op/ = [Cantidad Devuelta] / [Cantidad Vendida]
    ```
    * Asegúrate de que `[Cantidad Devuelta]` y `[Cantidad Vendida]` sean medidas o columnas ya existentes en tu modelo de datos.
5.  **Valida la fórmula:** Verifica que no haya errores de sintaxis y que la fórmula se calcule correctamente.

---
## Método 2: Función `DIVIDE`

La función `DIVIDE` es una opción preferible para cálculos de división, ya que te permite manejar el caso de división por cero de manera elegante, evitando errores.

### Pasos:

1.  **Crea otra nueva medida:**
    * En la misma pestaña **Modelado**, selecciona **"Nueva medida"** nuevamente.
2.  **Asigna un nombre a esta medida:** Nómbrala `Tasa de Devoluciones DIVIDE`.
3.  **Ingresa la fórmula DAX:**
    ```dax
    Tasa de Devoluciones DIVIDE = DIVIDE([Cantidad Devuelta], [Cantidad Vendida], 0)
    ```
    * En esta fórmula, el `0` es el valor que se devolverá si `[Cantidad Vendida]` es cero, previniendo así un error de división por cero.
4.  **Valida la medida:** Confirma que la medida se calcule correctamente, incluso cuando `[Cantidad Vendida]` sea cero.

---
## Requisitos y Comparación

### Comparación de resultados

Para comparar los resultados de ambos métodos:

1.  **Utiliza una matriz:** En la **Vista de Informe**, arrastra ambas medidas (`Tasa de Devoluciones Op/` y `Tasa de Devoluciones DIVIDE`) a una matriz. Incluye también las dimensiones de tus datos (como fecha, producto, etc.) con las que trabajaste en la sesión anterior.
2.  **Observa las diferencias:** Presta especial atención a las celdas donde `[Cantidad Vendida]` sea cero o nula. Es probable que `Tasa de Devoluciones Op/` muestre un error (como `Infinity` o un espacio en blanco), mientras que `Tasa de Devoluciones DIVIDE` mostrará el valor que definiste para el caso de división por cero (en este caso, `0`).

### Reflexión sobre el manejo de errores en DAX

Es fundamental manejar los errores en las fórmulas DAX, especialmente las divisiones por cero, porque:

* **Impacto en la interpretación de datos:** Un cálculo incorrecto o un error en una medida puede llevar a:
    * **Datos engañosos:** Si no se gestiona una división por cero, los valores resultantes pueden ser incorrectos y distorsionar la Tasa de Devoluciones real.
    * **Informes rotos:** Los errores pueden propagarse y causar que visualizaciones enteras fallen o muestren datos incompletos.
    * **Decisiones erróneas:** Basarse en datos que contienen errores puede conducir a decisiones de negocio equivocadas.
* **Ventaja de `DIVIDE`:** La función `DIVIDE` no solo hace que tus cálculos sean más robustos al prevenir errores de división por cero, sino que también facilita la creación de informes más limpios y confiables, ya que no se mostrarán errores en tus visualizaciones.

---
## Preguntas de esta tarea

Si lo deseas, puedes compartir una imagen de la Vista de Informe donde se muestren las medidas calculadas en la matriz. Esto será de gran ayuda para visualizar la diferencia en el manejo de errores entre ambos métodos.

---