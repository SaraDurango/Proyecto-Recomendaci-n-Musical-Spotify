# Proyecto-Recomendación-Musical-Spotify

Este repositorio contiene el proyecto “Técnicas de Agrupamiento Aplicadas a Sistemas de Recomendación Musical: Un Estudio Académico Basado en el Reto de Spotify “Million Playlist Dataset Challenge” que busca aplicar técnicas de clusterización para generar un sistema de recomendación musical personalizado, de acuerdo con los gustos de los usuarios. 

Los datos crudos corresponden al dataset proporcionado por Spotify en su reto “Million Playlist Dataset Challenge” y se encuentran en un archivo de extensión .ZIP llamado "spotify_million_playlist_dataset.zip (5.39 GB)" disponible en el link de acceso público https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge/dataset_files. Se recomienda descargarlo, pues dado su gran tamaño, no es posible incluirlo en este repositorio.

Estos datos son proporcionados directamente por Spotify y constituyen una muestra de un millón de playlist, abarcando alrededor de dos millones de pistas. Cada playlist está representada como un archivo JSON, el cual incluye información detallada como nombre, duración, pistas, número de seguidores, entre otros.

# Contenido del Repositorio

## *Notebook de Google Colab con el desarrollo del Modelo*

Se proporciona un notebook de Google Colab que incluye todo el desarrollo del proyecto, abarcando desde la limpieza y preparación de datos hasta la generación y evaluación de recomendaciones musicales. Las etapas clave incluyen análisis de componentes principales, determinación y comparación de clusters, evaluación de diferentes configuraciones de Kernel PCA, y visualización en 2D y 3D de las recomendaciones generadas. Se destaca la selección del mejor modelo, un Kmeans con 6 clusters aplicando Kernel PCA con gamma:0.9, seguido por el reentrenamiento con datos balanceados y la mejora de recomendaciones basadas en métricas detalladas.

## *Notebook de Google Colab con Preprocesamiento de Datos*

Se proporciona un archivo de Google Colab que contiene el código necesario para transformar los datos crudos en un archivo CSV llamado “combined_data_Converted2", en el cual se incluye el procedimiento necesario para extraer un slice de mil canciones del dataset original, agregar nuevas variables mediante consulta en la API para desarrolladores de Spotify, y procesar la playlist de un usuario con 100 canciones. Antes de ejecutar el código, se debe descargar previamente el archivo . ZIP mencionado anteriormente. 

Al ejecutar este código se generan los dos siguientes archivos CSV (los cuales se dispondrán en este repositorio para facilidad del lector): 

## *Archivo “combined_data_converted2” en fortmato CSV*

Contiene el dataset correspondiente al slice de mil canciones de la data original, con las variables originales del reto y las variables adicionales consultadas en la API, las cuales corresponden a características musicales de las canciones procesadas. 

## *Archivo “fav_songs_feats_df” en formato CSV*

Contiene la información de las canciones contenidas en la playlist del usuario con las variables correspondientes a éstas. 

## *Documento PDF con monografía*

Se incluye un documento en PDF llamado "DurangoSara_CaballeroCristian_2024_RecomendaciónMusicalSpotify.pdf", correspondiente al desarrollo y análisis escrito del proyecto

# Instrucciones de Uso

## *Para Ejecutar el Notebook del proyecto. Modelo de Recomendación Musical*

- Subir los archivos CSV combined_data_converted2 y fav_songs_feats_df a Google Colab. Estos fueron generados mediante el notebook de preprocesamiento, o también se encuentran disponibles parea descarga en este repositorio. 

- Ejecutar el notebook Modelo de Recomendación Musical

## *Para Ejecutar el Notebook de Preprocesamiento*

- Descargar el archivo ZIP "spotify_million_playlist_dataset.zip (5.39 GB)" desde el enlace de Google Drive https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge/dataset_files

- Subir la carpeta ZIP a Google Colab.

- Descargar el archivo CSV combined_data_converted2 que se genera en el código

- Descargar el archivo CSV fav_songs_feats_df que se genera en el código

