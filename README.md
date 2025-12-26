# ✈️ Reporte de Operaciones Aéreas – Dashboard Analítico

## 📌 Resumen del Proyecto
Este proyecto consiste en el desarrollo de un **dashboard interactivo** enfocado en el monitoreo de la **eficiencia operativa de una red de vuelos en Norteamérica**.  
Permite a los tomadores de decisiones identificar patrones de **cancelación**, **cumplimiento de itinerarios** y **distribución geográfica del tráfico aéreo**.

 ![image alt](https://github.com/ramirezdavidge/Flight-Delays-Cancellations-2015-Data-Visualization-Dashboard/blob/37fd9ed4a41ee01cfd04fc8243759bd5338896db/images/dashboard.PNG)

 
</p>

---

## 📌 Dataset Empleado
El análisis se basa en el dataset **Flight Delays**, publicado en **Kaggle** por el **Departamento de Transporte de los Estados Unidos (US Department of Transportation)**.  
Contiene información detallada de los **vuelos domésticos realizados en EE. UU. durante 2015**.

### 📂 Archivos Principales
El conjunto de datos está compuesto por tres archivos en formato CSV:

- **`flights.csv`**  
  Archivo principal con registros por vuelo, incluyendo:
  - Fecha (año, mes, día)
  - Aerolínea operadora
  - Aeropuerto de origen y destino
  - Horarios programados y reales
  - Retrasos (en minutos)
  - Indicadores de vuelos **cancelados** o **desviados**

- **`airlines.csv`**  
  Información descriptiva de las aerolíneas:
  - Código
  - Nombre de la aerolínea

- **`airports.csv`**  
  Datos de los aeropuertos:
  - Código
  - Ubicación geográfica (latitud y longitud)

Este dataset contiene **millones de registros**, lo que permite:
- Analizar patrones de **retrasos y cancelaciones**
- Evaluar el **rendimiento operativo** de las aerolíneas
- Explorar **tendencias temporales y geográficas**

📌 *No incluye información personal de pasajeros y es ampliamente utilizado en proyectos de análisis exploratorio, visualización y modelado predictivo.*

<p align="center">
  <img src="images/dataset.png" width="800">
</p>

---

## 📊 Métricas Clave (KPIs)
Para este modelo se desarrollaron métricas utilizando **DAX**, enfocadas en medir **volumen**, **eficiencia** y **confiabilidad operativa**.

### 📈 Métricas Principales de Rendimiento
Estas métricas proporcionan un resumen ejecutivo del desempeño operativo:

- **✈️ Total de Vuelos (1 millón)**  
  Métrica de volumen absoluto que cuantifica el tamaño del dataset y sirve como base para los indicadores de eficiencia.

- **📏 Distancia Total (842 millones de millas)**  
  Mide la intensidad operativa, permitiendo evaluar desgaste de flota y consumo de recursos a gran escala.

- **✅ % Vuelos Operados (96.14%)**  
  Indicador de fiabilidad del servicio. Representa la proporción de vuelos realizados respecto a los programados.

- **⏱️ % Vuelos Puntuales (57.93%)**  
  Métrica de calidad de servicio (**On-Time Performance**), utilizada para identificar cuellos de botella operativos.

- **❌ % Vuelos Cancelados (3.86%)**  
  Indicador de riesgo operativo y pérdida económica, clave para la gestión de costos y experiencia del cliente.

### 📊 Métricas de Tendencia y Distribución
Estas métricas permiten segmentar los KPIs principales para identificar patrones:

- **Cancelaciones Mensuales**  
  Febrero destaca con **20.5K cancelaciones**, identificando un periodo de alta vulnerabilidad operativa.

- **Distribución Semanal de Incidencias**  
  El **lunes** es el día más crítico (**9.8K cancelaciones**), con una reducción progresiva hacia el viernes.

- **Densidad de Vuelos por Ciudad**  
  Métrica geoespacial que identifica hubs congestionados y cobertura territorial.

- **Intensidad de Distancia Mensual**  
  Aunque **enero** presenta mayor distancia recorrida (**0.38B millas**), febrero muestra más cancelaciones, indicando problemas de eficiencia más que de volumen.

### 🧮 Lógica Técnica de las Métricas
- Uso de **medidas DAX explícitas** (no columnas implícitas), garantizando cálculos dinámicos.
- Interacción con dimensiones:
  - **Calendario (DimDate)**
  - **Aerolíneas**
  - **Aeropuertos**
- Correcto funcionamiento del **filtrado cruzado** en todo el modelo.

---

## 🔍 Hallazgos y Análisis de Datos

### 🌦️ Estacionalidad Crítica
- **Febrero** registra el mayor volumen de cancelaciones (**20.5K**).
- **Enero** lidera en millas voladas (**0.38B**).
- El impacto operativo se ve más influenciado por **factores externos (clima)** que por el volumen de tráfico.

### 📅 Pico Semanal de Incidencias
- **Lunes** es el día con más cancelaciones (**9.8K**).
- Mínimo operativo el **viernes (2.9K)**.
- Posible acumulación operativa tras el fin de semana.

### 🗺️ Concentración Geográfica
- Alta densidad de operaciones en la **costa este** y **región central de EE. UU.**
- Identificación clara de **hubs estratégicos** que requieren mayor atención logística.

---

## 🧠 Relevancia Técnica y UX/UI

### 🧩 Modelo de Datos
- Filtros cruzados por **Aeropuerto** y **Aerolínea**.
- Facilita análisis de **causa-raíz** y segmentación detallada.

### 🎨 Jerarquía Visual
- Lectura **top-down**:
  - KPIs globales
  - Análisis temporal
  - Análisis geográfico

### 🛠️ Visualizaciones Utilizadas
- **Gráficos de barras** → comparativas mensuales
- **Gráficos de área** → tendencias diarias
- **Mapas de calor / burbujas** → distribución espacial

---

📌 *Este proyecto demuestra cómo el análisis de datos y el diseño visual pueden integrarse para transformar grandes volúmenes de información en insights accionables.*

