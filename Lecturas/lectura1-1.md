## Crítica: Item-based collaborative filtering recommendation algorithms.

El enfoque del paper es realizar una modificación a un algortimo de recomendación. Primero se presenta que la gran problematica de los algoritmos de filtrado colaborativo tiene dificultades al encontrar vecinos de un usuario, donde la cantidad de usuarios es muy alta. Para evitar este problema del buscar los vecinos similares al usuario, se propone realizar una recomendación según los items(películas, compras, etc...). En este caso se toman 3 funciones de similaridad una basada en el coseno, otra en la correlación de Pearson-r y por último una versión ajustada de la correlación de Pearson en que se cambia el promedio de los items por el promedio de ratings del respectivo usuario. De los resultados de experimentación se obtiene que la vesrión ajustada es la que tiene un mejor desempeño al momento de predecir, dado que logro casi un 10% menos de MAE que las otras funciones de similaridad. Finaliza con una comparación de rendimiento con distintos tamaños del modelo. 

Respecto del contenido de este articulo lo encuentro regular, porque por un parte la demostración de resultados es buena, pero en varios casos no se explica bien algunos términos y ciertos tópicos que solamente se le arroja al lector con una pequeña explicación.

Me resulta realmente raro los resultados obtenidos al final en la comparación de rendimientos, dado que a mayor cantidad de items se obtiene un peor rendimiento, lo que podría implicar en un problema de escalabilidad a futuro. A su vez que se estaría tomando el caso de un modelo de tamaño pequeño, si se observa la figura 7, se obtiene que el MAE de este caso es mayor respecto a los x más grandes. Por lo que a los autores les falto un poco de discusión respecto a esta relación entre el rendimiento y el MAE. 

En general es articulo regular, pero que ofrece una gran oportunidad de mejorar este nuevo algoritmo de recomendación

