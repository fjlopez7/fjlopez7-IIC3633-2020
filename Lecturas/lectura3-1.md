## Crítica: Performance of Recommender Algorithmson Top-N Recommendation Tasks

En este paper se discute el uso de metricas al momento de calcular las recomendaciones a usuarios. Lo que se propone es el uso de accuracy metrics, que en español serian metricas de exactitud.

Primero proponen modificar el set de test que solamente va a tener rankings de valoración 5. Para cada uno de los items i, se toman m items que no han sido evaluados por el usuario. Luego se rankea y se toman los top-N items obtenidos. Si el item i esta en la recomendación del top-N se cuenta como un hit. Para las metricas propuestas se toma la cantidad de hits para cada item y se calcula el recall y la precision.

Despues se mencionan los distintos algoritmos recomendadores con los que se van a ocupar esta metrica que se serian más popular, mejor promedio, kNN, NNCosNgbr, SVD, PureSVD. Siendo este ultimo una modificación propuesta por ellos que se basa en relajar los especificaciones, dado que estamos ante un problema de obtener los top-N, en vez de obtener el valor del posible rating. Para esto asumen que todos los valores faltantes de los rating por usuarios son ceros. Donde el valor que se obtiene del rating es cercano, pero dejando un margen de error.

Por ultimo se muestran las graficas de comparación de los algoritmos según las metricas y según distintos valores de N. Se observa 
que las versiones de PureSVD muetran un notable desmpeño en la tarea de obtener los top-N.

Encuentro muy interesante el paper, dado que la forma en que haciendo una pequeña modificación al problema de recomendar items surgen 
una buena opción para otras metricas y otros algoritmos que podrian realizar mejor el trabajo. La forma del relato es muy amena y en general esta bien trabajado el paper. Quizas pudieron realizar un poco de comparación usando la metrica de error, para una mejor interpretación de los resultados. Me parecio interesante el ánalisis respecto a long-tail y all items, porque verdaderamente se observa grandes diferencias entre los resultados, que se deben principalmente al sesgo de los datos. 