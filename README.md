# Titanic_Machine_Learning_from_Disaster

## Contexto del problema
Este reto trata de analizar los datos de los pasajeros que se encontraban en el titanic con el objetivo de realizar feature engineering, limpieza y transformacion de datos con el objetivo de entrenar un modelo de Machine Learning y predecir la supervivencia de los pasajeros.

## Propuesta de la solución

### Herramientas utilziadas
Se utilizaron diferentes liberiras para la solucion, principalmente utilizamos las siguientes librerias:

  -  Scikit Learn
  -  Numpy
  -  Swaborn
  -  Pandas

### Exploración y preprocesamiento de los datos
El primer paso fue la exploración, para ello se deben de explorar cada uno de los atributos del dataframe, esto con el objetivo de llenar los datos faltantes en caso de que existan, observar la distribucion para realizar el balanceo y finalmente identificamos los posibles atrivutos que esten relacionados para generar nuevos atributos y finalmente manejando los outlayers para evitar posibles desviaciones de nuestro resultado

### Clasificadores
Para la solución decidimos utilizar diferentes clasificadores, esto con el objetivo de identificar el clasificador que despues de entrenar los datos obtendria el mejor accuracy, los clasificadores que decidimos utilizar fueron:

  - Random Forest
  - LDA
  - Stratified K-fold Cross Validation
  - Knearest Neighbors
  - PyTorch
  - Gaussian Naive Bayes

## Problemas encontrados

### Balance del dataframe
Nos percatamos de que en el dataframe existia un desbalance entre el numero de sobrevivientes y el numero de fallecidos, existian un mayor numero de pasajeros fallecidos que de sobrevivientes, lo cual podria causar una mejor clasificacion para las personas fallecidas, por ello decidimos aumentar el numero sobrevivientes para tener el mismo numero y obtener mejores resultados.

### Gran cantidad de datos faltantes
Varios atributos poseian datos faltantes, existen diferentes metodos para llenar estos datos como la moda, media y mediana, la manera en la cual nosotros llenamos estos datos fue con el metodo de KNN, este metodo llena los datos faltantes utilizando como referencia datos similares de otros datos, con esto aseguramos que todos los datos faltantes no tendran el mismo resultado siempre.

De igual forma nuestro dataframe contenia un atributo que el 77.9% de sus datos eran faltantes, decidimos eliminar esta columna ya que al utilizar metodos para llenar estos datos como la media, moda, mediana o uncluso el metodo de KNN llegariamos a tener una gran cantidad de datos repetidos los cuales no nos servirian para una buena clasificación

### Outlayers
Existian algunos datos que se salian mucho del promedio de los demas datos, esto podria afectar el resultado de nuestros clasificadores y por ello mismo decidismo eliminarlos para evitarlos y quedarnos simplemente con los datos fueran cercanos a la media.

### Falta de TrueLabels
Al momento de clasificar nuestro dataframe, no contabamos con las TrueLabels provenientes de la plataforma de Kaggle, esto genero problemas debido a que puede que los valores de nuestra X_test sean diferentes a nuestras X_train, lo cual disminuyo nuestro accuaracy de nuestros modelos.





