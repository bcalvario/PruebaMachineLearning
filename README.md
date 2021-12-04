# PruebaMachineLearning

## Pregunta 1: Regresión lineal
* Utiliza la base de datos Pregunta1.csv para construir un código reutilizable que; primero filtre las filas cuya columna Publisher sea igual a “Nintendo”. Con esta sub-base calcule la regresion de la columna Global_Sales como variable objetivo a predecir ‘Y’ contra las demas columnas numéricas (es decir de Action a Strategy). Después se deberá obtener la serie de predicciónes de “Global_Sales” Y^ y con esta calucular el error medio absoluto.

Por favor muestra el valor del Error medio absoluto aqui: 38.05918286986965.

* Utiliza el codigo anterior ( o modifícalo si asi lo consideras) para correr ese mismo ejercicio para cada uno de los niveles de la variable “Publisher”. En este ejercicio lo que buscamos es una lista de 5 elementos numericos donde cada uno contenga el valor del error medio absoluto del la venta del Publisher “i” vs la prediccion de esa venta por elmodelo “i”.

Por favor muestra el diccionario aqui: 

{'Activision': 16.095832298653903,
 'Nintendo': 38.05918286986965,
 'Electronic Arts': 25.341617283393997,
 'Sony Computer Entertainment': 20.229998446907125,
 'Ubisoft': 16.184825864930872}

## Pregunta 2 : Red Neuronal
Por favor para esta pregunta considera unicamente las filas de la tabla cuyo Publisher sea Nintendo.
Utiliza esta base y tensorflow / pythorch (puedes tambien usar API’s como keras para interactuar con ellos) para construir una red neuronal con una única capa oculta totalmente conexa (de 10 neuronas) . La red neuronal tendra que predecir el valor de la variable Global_Sales para cada año dados las columnas: (Action Platform Adsventure Puzzle Shooter Misc Sports Racing Simulation Fighting Role-Playing Strategy)

Ajusta el modelo y obten Y. Despues calcula el error absoluto promedio de este modelo.

Por favor escribe el error absoluto promedio del modelo aqui:

## Pregunta 3 : Random Forest with extreme boosting
Por favor para esta pregunta considera unicamente las filas de la tabla cuyo Publisher sea Nintendo.

Por favor, construye un modelo de bosque aleatorio a partir de muestras bootstrap de la tabla. Si gustas usa los siguientes hiperparametros -o propon los propios:

* profundidad maxima de cada arbol 7 niveles
* numero de arboles 1000
* sub_muestra (para bootstrap) .9
* numero de caracteristicas por arbol 7

El bosque aleatorio tendrá que predecir el valor de la variable Global_Sales ‘Y’ para cada año dados las columnas: (Action Platform Adventure Puzzle Shooter Misc Sports Racing Simulation Fighting Role-Playing Strategy)

Ajusta el modelo y obten Y. Despues calcula el error absoluto promedio de este modelo.

Por favor escribe el error absoluto promedio del modelo aqui:

# Pregunta 4 : ARIMA’s

Ajusta un modelo de serie de tiempo clasico (ARIMA) para la variable Global_Sales.

El modelo propuesto tendrá que predecir el valor de la serie de tiempo Global_Sales ‘Y’ para cada año.

Ajusta el modelo y obten Y. Despues calcula el error absoluto promedio de este modelo.

Por favor escribe el error absoluto promedio del modelo aqui:

## Pregunta 5 : Resultados

Presenta una tabla con el resultado del error absoluto promedio para cada uno de los modelos implementados en la parte 1 a 4,

* Si solo un modelo se pudiera implementar en produccion , ¿Cuál recomendarias? ¿Porqué?

* ¿Qué mejorarías en los modelos para que se ajusten mejor al data set utlizado? (por ejemplo para tomar en cuenta la correlación entre observaciones)
