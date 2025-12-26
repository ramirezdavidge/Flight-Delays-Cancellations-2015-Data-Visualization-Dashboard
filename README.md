# ✈️ Reporte de Operaciones Aéreas – Dashboard Analítico

## 📌 Resumen del Proyecto
Este proyecto consiste en el desarrollo de un **dashboard interactivo** enfocado en el monitoreo de la **eficiencia operativa de una red de vuelos en Norteamérica**.  
Permite a los tomadores de decisiones identificar patrones de **cancelación**, **cumplimiento de itinerarios** y **distribución geográfica del tráfico aéreo**.
<p align="center">
  <img src="images/dashboard.png" width="800">
</p>
## 📌 Dataset Empleado:
El dataset Flight Delays, publicado en Kaggle por el Departamento de Transporte de los Estados Unidos (US Department of Transportation), contiene información detallada sobre los vuelos domésticos realizados en 2015 dentro de los Estados Unidos. 
Medium
+1
Este conjunto de datos incluye tres archivos principales en formato CSV:
flights.csv: el archivo principal con registros de cada vuelo, que contiene datos como fechas (año, mes, día), aerolíneas operadoras, aeropuertos de origen y destino, horarios programados y reales de salida y llegada, tiempos de retraso (en minutos), y marcas de vuelos cancelados o desviados. 
Medium
+1
airlines.csv: información sobre las aerolíneas presentes en el conjunto de datos (p. ej., código y nombre de la aerolínea). 
Medium
airports.csv: datos de los aeropuertos incluidos en el dataset, como códigos y localizaciones geográficas. 
Medium
El dataset proporciona millones de registros de vuelos, con múltiples atributos que permiten estudiar patrones de retrasos y cancelaciones, analizar el rendimiento operativo de las aerolíneas, y explorar tendencias temporales o geográficas en la puntualidad de los vuelos. 
cnblogs.com
No incluye información personal de pasajeros y es ampliamente utilizado para análisis exploratorio de datos, visualización, modelado predictivo y proyectos de machine learning relacionados con la eficiencia del transporte aéreo.



## 📊 Métricas Clave (KPIs)
Para este modelo se desarrollaron métricas principales utilizando **DAX**, orientadas a medir volumen, eficiencia y confiabilidad operativa.

- **✈️ Volumen de Operación**
  - Más de **1 millón de vuelos**
  - **842 millones de millas** recorridas

- **❌ Tasa de Cancelación**
  - **3.86%** del total de vuelos  
  - Indicador crítico de **pérdida de ingresos** y **experiencia del cliente**

- **⏱️ Eficiencia de Puntualidad (OTP)**
  - **57.93%**
  - Oportunidad significativa de mejora en **gestión de tiempos en tierra** y **asignación de slots**

- **✅ Tasa de Operación**
  - **96.14%** de los vuelos programados lograron despegar

---

## 🔍 Hallazgos y Análisis de Datos

### 🌦️ Estacionalidad Crítica
- **Febrero** registra el mayor volumen de cancelaciones (**20.5K**), a pesar de no ser el mes con mayor distancia recorrida.
- **Enero** lidera en millas voladas (**0.38B**).
- Esto sugiere que **factores externos**, como el clima invernal, impactan la operación más que el volumen de tráfico.

### 📅 Pico Semanal de Incidencias
- **Lunes** es el día con mayor número de cancelaciones (**9.8K**).
- Existe un **descenso progresivo** a lo largo de la semana, alcanzando el mínimo el **viernes (2.9K)**.
- Posible efecto de acumulación operativa tras el fin de semana.

### 🗺️ Concentración Geográfica
- Alta densidad de operaciones en la **costa este y región central de Estados Unidos**.
- Identificación clara de **hubs estratégicos** que requieren mayor atención logística.

---

## 🧠 Relevancia Técnica y UX/UI

### 🧩 Modelo de Datos
- Implementación de **filtrado cruzado** por **Aeropuerto** y **Aerolínea**.
- Facilita análisis de **causa-raíz** (por ejemplo, identificar si las cancelaciones del lunes se concentran en una aerolínea específica).

### 🎨 Jerarquía Visual
- Diseño de lectura **top-down**:
  - KPIs globales para contexto inmediato
  - Análisis temporal
  - Análisis geográfico detallado

### 🛠️ Uso de Herramientas y Visualizaciones
- **Gráficos de barras** para comparativas mensuales
- **Gráficos de área** para tendencias diarias
- **Mapas de calor / burbujas** para distribución espacial de operaciones

---

📌 *Este proyecto demuestra cómo el análisis de datos y el diseño visual pueden integrarse para transformar grandes volúmenes de información en insights accionables.*
