# Descarga de Datos de Reanálisis desde Climate Engine

## Descripción
Este proyecto tiene como objetivo descargar información de reanálisis disponible en [Climate Engine](https://app.climateengine.org/climateEngine), en puntos de coordenadas específicas. Para este ejemplo, se utilizó el dataset **ERA5_AG** con una resolución de 9.6 km a escala diaria.

El reanálisis combina datos de modelos con observaciones de todo el mundo para crear un conjunto de datos globalmente completo y sin vacíos. Esta es una ventaja importante frente a los datos proporcionados por IDEAM. El proceso de reanálisis, denominado **asimilación de datos**, se basa en el método empleado por los centros de predicción meteorológica numérica, donde cada cierto número de horas (por ejemplo, 12 horas en el ECMWF) se integran datos para mejorar la calidad del conjunto de información.

## Requisitos
- Un archivo de coordenadas guardado en formato CSV, separado por punto y coma (`;`).
- Las coordenadas de los puntos deben estar en el sistema **WGS84 EPSG:32638** y expresadas en grados decimales, separadas en columnas de **longitud** y **latitud**.
- El archivo debe contener una columna llamada `OBJECTID`, que será utilizada como identificador para cada punto descargado (puede ser el nombre de una estación IDEAM, por ejemplo).

## Versatilidad del Código
Este código es versátil y puede usarse para cualquier dataset disponible en Climate Engine. Además de **ERA5**, también es compatible con otros productos como **NDVI** o **CHIRPS**, entre otros.

## Características
- Descarga archivos temporales por cada año de consulta.
- No descarga archivos raster, evitando el consumo excesivo de espacio en disco.
- No requiere instalar librerías adicionales, ya que está diseñado para ejecutarse en Google Colab.
- Requiere una cuenta de Google activa para iniciar sesión y almacenar los datos en Google Drive.
- Es recomendable utilizar Google Drive cuando se descargan grandes volúmenes de datos (por ejemplo, más de 20 años de datos diarios).

## Uso
1. Cargar el archivo de coordenadas en el entorno de ejecución.
2. Ejecutar el código en Google Colab.
3. Guardar los resultados en Google Drive si se trata de grandes volúmenes de datos.

## Contacto
Si tienes preguntas o necesitas soporte, puedes abrir un **Issue** en este repositorio.

