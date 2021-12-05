# PruebaMachineLearning

## Pregunta 1: Regresión lineal
* Utiliza la base de datos Pregunta1.csv para construir un código reutilizable que; primero filtre las filas cuya columna Publisher sea igual a “Nintendo”. Con esta sub-base calcule la regresion de la columna Global_Sales como variable objetivo a predecir ‘Y’ contra las demas columnas numéricas (es decir de Action a Strategy). Después se deberá obtener la serie de predicciónes de “Global_Sales” Y^ y con esta calucular el error medio absoluto.

Por favor muestra el valor del Error medio absoluto aqui: 16.095832298653903.

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

Por favor escribe el error absoluto promedio del modelo aqui: 24.785614

## Pregunta 3 : Random Forest with extreme boosting
Por favor para esta pregunta considera unicamente las filas de la tabla cuyo Publisher sea Nintendo.

Por favor, construye un modelo de bosque aleatorio a partir de muestras bootstrap de la tabla.

El bosque aleatorio tendrá que predecir el valor de la variable Global_Sales ‘Y’ para cada año dados las columnas: (Action Platform Adventure Puzzle Shooter Misc Sports Racing Simulation Fighting Role-Playing Strategy)

Ajusta el modelo y obten Y. Despues calcula el error absoluto promedio de este modelo.

Por favor escribe el error absoluto promedio del modelo aqui: 24.785614

# Pregunta 4 : ARIMA’s

Ajusta un modelo de serie de tiempo clasico (ARIMA) para la variable Global_Sales.

El modelo propuesto tendrá que predecir el valor de la serie de tiempo Global_Sales ‘Y’ para cada año.

Ajusta el modelo y obten Y. Despues calcula el error absoluto promedio de este modelo.

Por favor escribe el error absoluto promedio del modelo aqui:

## Pregunta 5 : Resultados

Presenta una tabla con el resultado del error absoluto promedio para cada uno de los modelos implementados en la parte 1 a 4:

|                                     |	  RESULTADO	  |
|-------------------------------------|---------------|
|           Regresión lineal          |	{'Activision': 16.095832298653903, 'Nintendo': 38.05918286986965, 'Electronic Arts': 25.341617283393997, 'Sony Computer Entertainment': 20.229998446907125, 'Ubisoft': 16.184825864930872} |
|           Regresión lineal          |	38.05918286986965 |
|             Red Neuronal            | 24.785614 |
| Random Forest with extreme boosting | 21.792384694417315 |
|                ARIMA                | ... |

* Si solo un modelo se pudiera implementar en produccion , ¿Cuál recomendarias? ¿Porqué?

Primero hagamos un pequeño analisis de usar cada uno de los modelos.

Una desventaja el modelo de regresión múltiple generalmente se reduce a los datos que se usan (datos incompletos). Pero es más fácil de implementar, interpretar y eficiente de entrenar.

Las redes neuronales requerirán mucha información para poder entrenarla de mejor manera y que realmente sea efectiva. La red neuronal simplemente diezmará la capacidad de interpretación de sus características hasta el punto en que deje de tener sentido por el bien del rendimiento.

Random Forest es menos costoso que la red neuronal desde el punto de vista computacional. Una de las ventajas es que automatiza los valores perdidos presentes en los datos. 

Algunas de las principales desventajas de los pronósticos ARIMA son que algunas de las técnicas tradicionales de identificación de modelos para identificar el modelo correcto de la clase de modelos posibles son difíciles de comprender y costosas desde el punto de vista computacional.

Tomando en cuenta la dificultad de implementar (a mayor dificultad mayor tiempo para hacer la implementación, claro sin perder de vista lo importante que es los resultados), los resultados obtenidos (el error) y el costo computacional el modelo que recomendaría es Random Forest.

* ¿Qué mejorarías en los modelos para que se ajusten mejor al data set utlizado?
  
   * **Aumentar el tamaño del dataset para poder entrenar de mejor manera cada modelo.**
   * Reducción dimensional el cual reduce el espacio de tiempo y almacenamiento requerido.
   * Regularización (en aprendizaje automático).
   * **Validación cruzada (técnica que se uso para las preguntas dadas).**
   * Ver la distribución de variables en data set para ver la forma de los datos y ver si está sesgada la distribución.
   * Ver las relaciones entre variables.
   * Ver si los datos tienen o no valores atípicos o puntos inusuales que puedan indicar problemas de calidad de los datos.
   * Ver si los datos tienen o no patrones temporales.
   
