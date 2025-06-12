# Power BI: Análisis de Medidas y Matrices

Este proyecto tiene como objetivo construir seis medidas DAX cruciales y dos matrices específicas en Power BI para visualizar el rendimiento empresarial.

---

## 1. Desarrollo de Medidas DAX

A continuación, se detallan las medidas DAX que deberán crear:

* **Devoluciones del Mes Anterior:** Calcula el total de devoluciones registradas en el mes inmediatamente anterior.
    * *Función clave:* `CALCULATE`
* **Órdenes del Mes Anterior:** Determina el total de órdenes recibidas durante el mes anterior.
    * *Funciones clave:* `CALCULATE`, `DATEADD`
* **Utilidad Bruta del Mes Anterior:** Estima la utilidad bruta generada en el mes anterior.
    * *Funciones clave:* `CALCULATE`, `DATEADD`
* **Meta de Órdenes:** Establece una meta de órdenes incrementando las órdenes del mes anterior en un 5%.
* **Meta de Utilidad Bruta:** Fija una meta de utilidad bruta aumentando la utilidad bruta del mes anterior en un 5%.
* **Utilidad Bruta de los Últimos 90 Días:** Calcula la utilidad bruta acumulada durante los últimos 90 días, utilizando la fecha más reciente como punto de partida.
    * *Funciones clave:* `CALCULATE`, `DATESINPERIOD`, `MAX`

---

## 2. Creación de Matrices en Power BI

Deberán configurar dos matrices para visualizar las medidas desarrolladas:

### a. Primera Matriz

Esta matriz mostrará las primeras cinco medidas y permitirá comparar las metas establecidas con los resultados reales a lo largo del tiempo.

* **Filas:** Inicio de Mes
* **Columnas:**
    * Devoluciones del Mes Anterior
    * Órdenes del Mes Anterior
    * Utilidad Bruta del Mes Anterior
    * Meta de Órdenes
    * Meta de Utilidad Bruta

### b. Segunda Matriz

Esta matriz se enfocará en el análisis del rendimiento a corto plazo y la detección de tendencias.

* **Filas:** Utilidad Bruta de los Últimos 90 Días
* **Columnas:** Fechas Diarias

---

**Nota:** Es fundamental revisar cada medida y matriz para asegurar su precisión y coherencia. Este ejercicio no solo fortalecerá sus habilidades en DAX y Power BI, sino que también proporcionará información valiosa para el análisis del rendimiento empresarial y la toma de decisiones estratégicas.

¡Manos a la obra!

---

**Preguntas de esta tarea:**

1.  Comparta una captura de pantalla de la **primera matriz** (la que tiene 5 medidas).
2.  Comparta el código DAX de la medida **"Utilidad Bruta de los Últimos 90 Días"**.