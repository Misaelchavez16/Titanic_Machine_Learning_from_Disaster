# Titanic_Machine_Learning_from_Disaster

## Contexto del problema:

Este desafío se enfoca en el análisis de datos de los pasajeros a bordo del Titanic, con el objetivo de realizar ingeniería de características, limpieza y transformación de datos para entrenar un modelo de aprendizaje automático y predecir la supervivencia de los pasajeros.

## Propuesta de la solución:

### Herramientas utilizadas:

Para abordar este problema, empleamos diversas bibliotecas, siendo las más destacadas las siguientes:

  - Scikit-Learn
  - Numpy
  - Seaborn
  - Pandas

### Exploración y preprocesamiento de los datos:

El primer paso crítico fue la exploración exhaustiva de los atributos en el conjunto de datos. Esta fase es fundamental para tratar datos faltantes, equilibrar la distribución de clases, identificar relaciones entre atributos para crear nuevas características y gestionar valores atípicos que podrían sesgar nuestros resultados.

### Clasificadores:

Para resolver este problema, implementamos varios clasificadores con el objetivo de determinar cuál de ellos ofrecía el mejor rendimiento en términos de precisión. Los clasificadores que evaluamos incluyen:

  - Random Forest
  - LDA (Análisis Discriminante Lineal)
  - Stratified K-fold Cross Validation
  - K-Nearest Neighbors (KNN)
  - PyTorch
  - Gaussian Naive Bayes

## Problemas encontrados:

### Balance del dataframe:
Identificamos un desequilibrio en el número de sobrevivientes y fallecidos en el conjunto de datos. Había más pasajeros fallecidos que sobrevivientes, lo que podría llevar a una mejor clasificación de las personas fallecidas. Para abordar esto, aplicamos técnicas de sobremuestreo para igualar el número de muestras de ambas clases y mejorar nuestros resultados.

### Gran cantidad de datos faltantes:
Varios atributos presentaban valores faltantes, y para abordar esta problemática, empleamos el método K-Vecinos Más Cercanos (KNN) para imputar los datos faltantes. Este enfoque utilizó datos similares de otras muestras para llenar los valores faltantes, garantizando una imputación más precisa y variada.

### Eliminación de atributos con datos mayoritariamente faltantes:
Encontramos un atributo en el que el 77.9% de sus valores eran faltantes. Dada la gran proporción de datos faltantes, decidimos eliminar esta columna, ya que llenarla con métodos tradicionales generaría una gran cantidad de datos repetidos que no serían útiles para una clasificación precisa.

### Manejo de valores atípicos (outliers):
Observamos que algunos datos se alejaban significativamente de la media de otros datos. Estos valores atípicos podrían afectar negativamente el rendimiento de nuestros clasificadores. Como solución, optamos por eliminar estos valores atípicos para mantener un conjunto de datos más cercano a la media.

### Falta de True Labels:
Una limitación importante fue la falta de etiquetas verdaderas (True Labels) al momento de la clasificación. Esto generó desafíos, ya que los valores de nuestro conjunto de prueba (X_test) podrían diferir de los de nuestro conjunto de entrenamiento (X_train), lo que afectó negativamente la precisión de nuestros modelos.
