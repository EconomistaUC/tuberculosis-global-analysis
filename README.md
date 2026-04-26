# Análisis de Tuberculosis Global — OMS & Población Mundial

## Descripción

Este proyecto corresponde a un caso práctico desarrollado en Python 
para la Organización Mundial de la Salud (OMS), cuyo objetivo es 
preparar, limpiar y analizar los datos más recientes de casos de 
tuberculosis a nivel mundial con miras a presentar la situación 
actual ante el consejo directivo de la organización.

## Notebook

[Ver análisis completo](./Análisis_de_Tuberculosis_Global_—_OMS_&_Población_Mundial.ipynb)

## ¿Qué se hizo?

Se trabajó con dos conjuntos de datos oficiales: `who.csv`, que 
contiene registros de casos nuevos de tuberculosis por país, año, 
tipo de diagnóstico, sexo y grupo de edad reportados a la OMS entre 
1980 y 2013; y `population.csv`, que registra la población total 
por país y año entre 1995 y 2013. En la primera etapa se realizó 
una exploración diagnóstica de ambos datasets para comprender su 
estructura, tipos de variables, dimensiones y presencia de valores 
nulos. En la segunda etapa se aplicó el principio de *tidy data*: 
las 56 columnas de casos del dataset WHO fueron transformadas a 
formato largo (una observación por fila), se descompuso la clave de 
cada variable para extraer el tipo de diagnóstico (`sp`, `sn`, `ep`, 
`rel`), el sexo y el grupo de edad, y se eliminaron registros sin 
información. Posteriormente ambas tablas se unieron por país y año, 
lo que permitió calcular la **tasa de incidencia por 100,000 
habitantes** como métrica normalizada. Finalmente se construyó un 
análisis visual completo que incluye tendencias globales, países con 
mayor carga absoluta y relativa, evolución temporal de los cinco 
países más afectados, distribución por sexo, grupo de edad 
(heatmap) y tipo de diagnóstico, con el fin de identificar 
tendencias, casos de éxito y países que requieren mayor apoyo, 
alineando el análisis con las metas de la ONU de reducir la 
incidencia en un 50% y las muertes en un 75% para el año 2025.

## Archivos

| Archivo | Descripción |
|---|---|
| `who_tb_analysis.ipynb` | Notebook principal con todo el código |
| `population.csv` | Dataset de población mundial |
| `who.csv` | Dataset de tuberculosis OMS |

## Tecnologías

- Python 3 · Pandas · NumPy · Matplotlib · Seaborn
- Google Colab

## Fuente de datos

[tidyr R documentation — WHO dataset](https://tidyr.tidyverse.org/reference/who.html)
