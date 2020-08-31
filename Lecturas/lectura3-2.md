## Evaluating Recommendation Systems

El tema que se maneja en el paper es como dice en el título evaluar los sistemas recomendadores, esto se compara a traves de tres experimentos: uno offline, estudios de usuarios y expermientos online.

Respecto a offline se explica que a traves de la data de los ratings de los usuarios se pueden testear los distintos algoritmos y afinar ciertos parametros del algoritmo. Se debe tener un cuidado especial con la data, debido al posible sesgo que pueda tener, que puede implicar que el desempeño de algoritmo se modifique debido a esto.

Sobre user-studies se menciona que a traves de distintas pruebas y preguntas se evalue la interacción del usuario con el sistema recoemendador. De las ventajas de este tipo de experimentos es que podemos evaluar el comportamiento del usuario y la influencia que cause en el usuario las recomendaciones. Lo que implica en obtener información cualitiva que permite evaluar de forma critica los datos cuantitivos presentes en los ratings. Una desventaja es que los user-test son caros de conducir, dado al alto consumo de tiempo al tener que repetir muchas veces ciertas acciones. Algo a tener en cuenta es que los usuarios de testeo deben ser lo más cercano al público objetivo del sistema.

En el caso de la evaluación online, se explica que el principal foco es medir en cuanto cambio el comportamiento del usuario, debido a ala interacción con sistemas recomendadores. Este tipo de experemientos es la que tiene más valor, porque realiza la tarea de recomendar a un usario de forma real. 

En el paper a su vez se ven distintas propiedades de sistemas recomendadores, como lo son las distintas metricas para evaluar el resultado del algoritmo como lo serian las de error y las de exactitud. Se mencionan lo que son los conceptos de cold-start, confianza en las recomendaciones, utilidad, riesgo, robustez, etc... 

En general no me gusto mucho esta lectura, la encontre muy densa, dado que trataba de abarcar muchos tópicos, pero no se detenia a explicar un poco las cosas. Se siente que a veces se pierde el foco principal y no siguen una linea principal de la temática del paper. Por lo que, podria decir que es un muy mal paper. 