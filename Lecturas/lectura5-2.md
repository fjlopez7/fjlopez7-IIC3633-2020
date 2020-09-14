## Crítica: Combining Predictions for Accurate RecommenderSystems

En este paper se estudia una forma de mezclar las distintas recomendaciones realizadas por distintos algoritmos de collaborative filtering, esto en búsqueda de un mejor rendimiento. Se presentan distintos algoritmos de collaborative filtering y de ensamble methods para mezclar las predicciones. La datos ocupados son los de Netflix Prize contest.


Entre los algoritmos de CF se nos presentan KNN, SVD, AFM, RBM y GE.
Siendo los 2 primeros algo común en lo visto en otros paper es bueno explicar en que consiste el resto. AFM consiste en una forma similar de SVD,pero que solamente se tiene item features y que los usuarios son represntados por los items que califican. RBM consiste en una red neuronal con una capa de input y otra capa oculta, se basa en modelos de generación estocástico. GE consiste en algo similar SVD solamente en que las features estas realizadas en base a la información que se tiene por ejemplo el promedio de los ratings, números de votos, etc...

Para evaluar el rendimiento de los distintos blendings se ocupa la métrica de RMSE que en este caso se busca minimizar. La primera opción para montar como el caso base de blending sería una regresión lineal, que se resuelve a traves de mínimos cuadrados. Otra opción sería la de ocupar una red neuronal a traves de descenso de gradiente estocástico. Una opción interesante es la de ocupar decision tree, pero se agregan otroa metodos como serian los de bagging(combinar los resultados de varios test aleatorios) y gradient boosting(Se combinan los modelos que se van obteniendo de forma incremental y se agrega el peso del learning rate en cada iteración, de tal forma de obtener una preddiccón final en base a boosting). 

Entre los resultados se obtuvo que el mejor despeño tuvo fue el blending en el caso de redes neuronales. En algunos de los métodos de blendings no se pudo lograr obtener un resultado y se puede observar que en general los timepos de entrenamientos en varios casos son muy altos. 


Encuentro que la idea principal del paper es muy buena, dado que muestra una nueva forma de obtener un método de recomendar que sería en base a la combinación de las distintas recomendaciones obtenidas de los distintos metodos. No me gusto que se necesecitara tanto  conocimiento previo en sistemas recomendadores y machine learning, dado que no se explica mucho como funcionan algunos métodos y a veces es díficil seguir la lectura por los términos que se ocupan.

Me genera una gran duda respecto a los resultados, ya que entra la duda si es que vale la pena mejorar una milesima del valor de RMSE, pero aumentando significativamente el tiempo de entrenamiento y el tiempo de realizar las predicciones. Dado que en este caso se obtiene una mejora con el resultado obtenido en redes neuronales, pero con tiempos de entrenamiento que pueden llegar a las 65 horas.