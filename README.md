# Proyecto_Analisis_Taxis
Análisis exploratorio de negocio y manejo de bases de datos con SQL

Este proyecto analiza datos de viajes compartidos en Chicago para Zuber, una nueva empresa del sector.

## Problema
Zuber, al lanzarse en Chicago, necesita comprender el mercado local de viajes compartidos, identificar patrones en el comportamiento de los pasajeros y evaluar cómo las condiciones climáticas impactan la duración de los viajes. El objetivo es obtener información valiosa para la toma de decisiones estratégicas.

## Datos
Se utilizaron tres conjuntos de datos provenientes de archivos CSV:

moved_project_sql_result_01.csv: Información sobre compañías de taxis y la cantidad de viajes realizados.
moved_project_sql_result_04.csv: Datos sobre ubicaciones de destino y el promedio de viajes.
moved_project_sql_result_07.csv: Información sobre condiciones climáticas y la duración de los viajes.

## Método
El análisis se realizó utilizando Python y las librerías pandas, matplotlib y seaborn. Los pasos incluyeron:

Carga e inspección de datos: Carga de los archivos CSV y exploración inicial de la estructura y tipos de datos de cada DataFrame.
Limpieza de datos: Eliminación de filas duplicadas en el DataFrame de datos climáticos (weather_df) y conversión de la columna de fecha y hora (start_ts) al tipo de dato datetime.
Exploración de datos (EDA): Análisis descriptivo para comprender la distribución de los datos, identificar valores faltantes y duplicados. Se identificaron las 10 ubicaciones de destino con mayor promedio de viajes y se calculó la duración promedio de los viajes por condición climática.
Visualización de datos: Creación de gráficos de barras para visualizar la cantidad de viajes por compañía de taxi, el promedio de viajes por ubicación de destino (Top 10) y la duración promedio de los viajes por condición climática.
Prueba de Hipótesis: Se realizó una prueba t de Student para medias independientes para probar la hipótesis: "La duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare cambia los sábados lluviosos".

## Resultados / KPIs
Los hallazgos clave del análisis son:

El mercado de taxis en Chicago está dominado por unas pocas grandes empresas, lo que sugiere un mercado concentrado.
Las áreas con mayor demanda de viajes son el Loop, River North y Streeterville.
Las condiciones climáticas adversas (clasificadas como 'Bad' en los datos) están asociadas con una mayor duración promedio de los viajes en comparación con las condiciones climáticas favorables ('Good').
La prueba de hipótesis confirmó estadísticamente que la duración promedio de los viajes en sábados cambia significativamente bajo condiciones climáticas adversas para la ruta específica del Loop al Aeropuerto Internacional O'Hare.
Estos resultados son fundamentales para Zuber al planificar su estrategia operativa, asignar recursos a las áreas de alta demanda y prepararse para las fluctuaciones en la duración de los viajes debido al clima.

## Cómo correr
Clonar el repositorio de GitHub.
Asegurarse de tener Python instalado y las librerías pandas, matplotlib y seaborn.
Los archivos de datos (moved_project_sql_result_01.csv, moved_project_sql_result_04.csv, moved_project_sql_result_07.csv) deben estar en el mismo directorio o la ruta especificada en el código.
Ejecutar el script o el notebook de Python que contiene el código del análisis.
