# Análisis Estadístico del Comportamiento Climático (ODS 13) 🌍

Este proyecto desarrolla un proceso **ETL (Extract, Transform, Load)** robusto para analizar datos meteorológicos de la NOAA, enfocándose en la identificación de anomalías climáticas y eventos extremos en apoyo al **Objetivo de Desarrollo Sostenible 13: Acción por el Clima**.

## 🚀 Descripción del Proyecto
El sistema procesa datos locales (estación de Pereira) para transformar registros complejos y ruidosos en información estructurada. El objetivo es proporcionar una base sólida para el monitoreo de anomalías y la adaptación climática basada en datos.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Entorno:** Google Colab / Jupyter Notebooks
* **Librerías Principales:**
    * `Pandas`: Manipulación y análisis de estructuras de datos.
    * `Numpy`: Soporte para cálculos matemáticos y gestión de valores nulos.
    * `Matplotlib / Seaborn`: Visualización de transformaciones y eventos climáticos.
    * `Logging`: Registro de eventos por cada fase del proceso.

## 🔄 Funcionamiento del Proceso ETL

### 1. Extracción (Extract)
* Obtención de datos desde la base de datos de la NOAA (Local Climatological Data - LCD).
* Generación de logs de trazabilidad para asegurar que el origen de los datos es consistente.

### 2. Transformación (Transform)
Es el núcleo del proyecto e incluye:
* **Limpieza de Datos:** Eliminación de caracteres especiales en variables como `HourlyPrecipitation` y conversión a tipos numéricos (`float`).
* **Manejo de Series Temporales:** Desglose de la columna `DATE` en Año, Mes, Día y Hora para análisis estacional.
* **Tratamiento de Nulos:** Implementación de reglas de negocio como interpolación lineal e imputación por media histórica.
* **Normalización:** Conversión de unidades del sistema imperial al Sistema Internacional (Celsius, Km/h).
* **Deduplicación:** Lógica de llave única basada en `STATION + DATE`.
* **Mapeo Climático:** Uso de tablas de búsqueda para traducir códigos complejos (ej. `||13`) a etiquetas de texto legibles.

### 3. Carga (Load)
* Almacenamiento de los datos limpios y agregados.
* Creación de variables específicas para el ODS 13, como indicadores de "Eventos Extremos".

## 📊 Impacto (ODS 13)
El proyecto permite:
* **Monitoreo de Anomalías:** Identificar patrones de cambio climático local.
* **Resiliencia:** Ayudar en la planificación urbana ante olas de calor o riesgos de inundación mediante el análisis de percentiles de temperatura y precipitación.

## 👥 Autores
* **Bryan Andrés Herrera** - 2244008
* **Alessandro Yusty Ceballos** - 2240248
* *Universidad Autónoma de Occidente - Ingeniería en Datos e IA*