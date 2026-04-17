# Proyecto: Análisis del Servicio de Taxis en Chicago (Zuber)

## Descripción del Proyecto
Zuber es una nueva empresa de viajes compartidos que se está lanzando en Chicago. El objetivo de este análisis es encontrar patrones en la información disponible para comprender las preferencias de los pasajeros y el impacto de factores externos (como el clima) en los viajes.

Este proyecto abarca desde el procesamiento de datos SQL (resultados de consultas previas) hasta el análisis exploratorio de datos (EDA) y la verificación de hipótesis estadísticas utilizando Python.

## Estructura de los Datos
El análisis se basa en tres conjuntos de datos principales:

1.  **Resultados de Compañías (`project_sql_result_01.csv`):**
    * `company_name`: Nombre de la empresa de taxis.
    * `trips_amount`: Número de viajes realizados el 15 y 16 de noviembre de 2017.

2.  **Resultados por Barrio (`project_sql_result_04.csv`):**
    * `dropoff_location_name`: Barrios de Chicago donde terminaron los viajes.
    * `average_trips`: Promedio de viajes finalizados en cada barrio durante noviembre de 2017.

3.  **Viajes Loop-O'Hare (`project_sql_result_07.csv`):**
    * `start_ts`: Fecha y hora de recogida.
    * `weather_conditions`: Condiciones climáticas (Good/Bad).
    * `duration_seconds`: Duración del viaje en segundos.

## Pasos del Análisis

### 1. Análisis Exploratorio de Datos (EDA)
* Importación y limpieza de datos (verificación de tipos de datos).
* Identificación de los **10 barrios principales** con mayor volumen de finalización de viajes.
* **Visualización:**
    * Gráfico de barras: Top empresas de taxis vs. número de viajes.
    * Gráfico de barras: Top 10 barrios de destino.
* Conclusiones sobre el dominio del mercado y los puntos calientes de la ciudad.

### 2. Prueba de Hipótesis
Se analizó la siguiente premisa: 
> *"La duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare cambia los sábados lluviosos."*

* **Hipótesis Nula ($H_0$):** La duración promedio de los viajes los sábados lluviosos es igual a la duración promedio los sábados de buen clima.
* **Hipótesis Alternativa ($H_1$):** La duración promedio de los viajes cambia (es diferente) cuando llueve los sábados.
* **Metodología:** Se utilizó una prueba t de Student para muestras independientes con un nivel de significación ($\alpha$) del 0.05.

## Herramientas Utilizadas
* **Lenguaje:** Python 3.x
* **Librerías:** * `pandas` para manipulación de datos.
    * `matplotlib` y `seaborn` para visualización.
    * `scipy.stats` para las pruebas estadísticas.

## Conclusiones Principales
*(Aquí puedes añadir un breve resumen de lo que encontraste, por ejemplo: "Se identificó que el barrio Loop es el destino más frecuente y que existe una diferencia estadísticamente significativa en los tiempos de viaje según el clima.")*
