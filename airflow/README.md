# Proyecto #1 Flujos de ejecución
## Descripción
Client: Ministerio de Educación de la Nación
Situación inicial
📍
Somos un equipo de desarrollo y data analytics, que trabajamos para la consultora “MyData”
y nuestro líder técnico nos comparte un pedido comercial directamente del Consejo Nacional
de Calidad de la Educación (por sus siglas, CNCE).
El CNCE es un grupo deliberante que pertenece al Ministerio de Educación de la Nación
Argentina. 
Este se encuentra analizando opciones universitarias disponibles en los últimos 10
años para comparar datos extraídos de universidades de todo el país, públicas y privadas,
con el fin de tener una muestra representativa que facilite el análisis.
Para esto, compartieron a “MyData” información disponible de más de 15 universidades y
centros educativos con gran volumen de datos sensibles sobre las inscripciones de alumnos.
El CNCE requiere que preparemos el set de datos para que puedan analizar la información
relevante y tomar directrices en cuanto a qué carreras universitarias requieren programa de
becas, qué planes de estudios tienen adhesión, entre otros.
Tu objetivo
📋 Como parte de un equipo de desarrollo y data analytics de “MyData”, deberás analizar y
preparar flujos de ejecución del set de datos recibido para obtener las comparaciones y
mediciones requeridas por el CNCE.

Requerimientos 🔧

● El Ministerio necesita que ordenemos los datos para obtener un archivo con sólo la
información necesaria de cierto periodo de tiempo y de determinados lugares
geográficos de una base de datos SQL (las especificaciones serán vistas en la primera
reunión de equipo). Será necesario generar un diagrama de base de datos para que se
comprenda la estructura.

● Los datos deben ser procesados de manera que se puedan ejecutar consultas a dos
universidades del total disponible para hacer análisis parciales. Para esto será
necesario realizar DAGs con Airflow que permitan procesar datos con Python y
consultas SQL.

● Calcular, evaluar y ajustar formatos de determinados datos como fechas, nombres,
códigos postales según requerimientos normalizados que se especifican para cada
grupo de universidades, utilizando Pandas.
Assets 🎨


## Requerimientos:
- Apache-Airflow 2.2.2
- Python 3.6
## Modulos utilizados en Python
- pathlib
- logging
- pandas
- datetime
- os
- sqlalchemy

## Estructura y flujo de ejecución
  Se generaron archivos ".sql" con las consultas correspondientes a cada centro educativo, normalizando las columnas tenidas en cuenta
  Mediante operadores disponibles en apache airflow (Python operators y postgre operators, se toman las consultas ".sql" para obtener los datos de la       base de datos provista. Estos datos se transorman mediante la libreria pandas, y se almacenan en forma local como archivos ".txt".
  Finalmete, a traves de las herramientas provistas por AWS (operadores y hooks S3), los datos almacenados como ".txt" son transformados a strings, y       almacenados en el servicio S3.

