# Creación de Tarjetas y Gráficos de Línea

En esta tarea, pondrás en práctica lo aprendido en relación a la creación de tarjetas y gráficos de línea en Power BI.

---

## 1. Creación de Medidas

Para comenzar, necesitarás crear dos medidas clave en Power BI utilizando DAX:

* **Clientes Únicos**: Utilizando el campo `IDCliente` de la tabla `Ventas 2024-2026`, crea una medida que calcule el número de clientes únicos. Puedes usar la función `DISTINCTCOUNT()` para esto. La fórmula debería ser algo así:

    ```dax
    Clientes Únicos = DISTINCTCOUNT('Ventas 2024-2026'[IDCliente])
    ```

* **Ingresos por Cliente**: Una vez establecida la medida de **Clientes Únicos**, crea otra medida que divida el `Total de Ingresos` por los **Clientes Únicos** para obtener los ingresos promedio por cliente. Utiliza la función `DIVIDE()` para garantizar el manejo adecuado de divisiones por cero:

    ```dax
    Ingresos por Cliente = DIVIDE([Total Ingresos], [Clientes Únicos])
    ```

---

## 2. Creación de Tarjetas de KPIs

En la página **Clientes** de tu informe en Power BI, debes incorporar dos tarjetas de KPIs:

* **Primera Tarjeta de KPI**: Muestra la medida de **Clientes Únicos**. Si lo prefieres, puedes reutilizar las tarjetas de KPI que creamos en sesiones anteriores y simplemente actualizar la medida utilizada.

* **Segunda Tarjeta de KPI**: Muestra la medida de **Ingresos por Cliente**. Al igual que con la primera tarjeta, puedes modificar una tarjeta existente para reflejar esta nueva medida.

---

## 3. Generación de Gráfico de Línea

Finalmente, deberás crear o actualizar un gráfico de línea para mostrar la evolución de los **Clientes Únicos** por mes:

* **Gráfico de Línea de Clientes Únicos por Mes**: Utiliza los datos de la medida **Clientes Únicos** y configura el eje X para representar los meses. Este gráfico ayudará a visualizar cómo ha cambiado la cantidad de clientes a lo largo del tiempo. Si ya tienes un gráfico similar de sesiones anteriores, puedes ajustarlo para reflejar esta nueva medida.

---

## Pregunta de esta tarea

Comparte tu gráfico de Clientes Únicos por Mes.