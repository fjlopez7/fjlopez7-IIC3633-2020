## Crítica:  Carousel Personalization in Music Streaming Apps with Contextual Bandits

En este paper se presenta el problema de mostrar las recomendaciones personalizadas de un carrusel, que es muy común en plataformas de música. Por lo que se presenta un modelo carrusel personalizado, que se presenta como u problema de contextual multi-armed bandit con múltiples plays. 

Multi-armed bandits consiste en primero entidades llamadas arms, junto a un forecaster donde este tiene que elegir del conjunto disponible de arms un subconjunto L. Donde el forecaster recibe una recompesa por seleccionar un respectivo arm (esta recompesa puede estar dada por una Bernoulli). El objetivo del forecaster es 
maximizar el valor de recompesa de elegir los arms.

Para la problematica que se presenta se tiene que las arms del bandit serian los items de la aplicación. El carrusel en este caso corresponse al subconjunto. Por lo que una opción sería tener para cada usuario un bandit recomendando, pero estoy sería muy costoso al ser del tamaño de item x user. Por lo que se propone realizar clustering de usuarios y contextual multi-armed bandits que consistría en que se posee un vector que representa las preferencias del usuario se evalua junto a unos pesos en una función sigmoidal, de tal forma de tener aprender los pesos, y el resultado de la función que sea la probabilidad del user con el item.

Para la experimentación se ocupa un dataset de la app Dezzer, donde se obtiene 862 playlist y  974960 usuarios. Para el ambiente offline se ocupa python para simular las interacciones, donde se ocupo que los vectores de usuarios están dados por una dimensión de tamaño 97 y para los clusters una cantidad de 100.

Respecto a los algoritmos ocupados para ejecutar bandit se presentan las siguientes random, e-greedy, Thompson, Upper confidence bound, explore than commit y una extension de Thompson.

Respecto a los experimentos en los casos de semi-personalizado y personalizado se obtiene un mejor resultado al momento de generar el carrusel para el caso semi-personalizado, que seria el de clusters. Se menciona que hay que tener cuidado al delimitar cada cluster.

Respectoa a los algoritmos se obtuvo que para semi-personalization, tiende a ocupar estocásticos, como por ejemplo Thompson y e-greedy. Además se observa que upper confidence bound tiende a recomendar el mismo conjunto de playlists. Mientras que los estocásticos presentan una amyor exploración al momento de realizar una nueva recomendación del carrousel.


Encontre el paper bueno, especialmente por como se aborda este problema que consiste en recomendar un carrusel y la forma que presentan para resolver a través de Bandit. Además me gusto la forma en que se plantea las soluciones y como llegaron a un resultado que solcuón es más factible. Otro punto a favor es que la forma que presentan todo no se encasilla solamente en música, sino que se podría ocupar en otras apps. Lo que menos me gusto del paper es que se necesitaba tener un conocimiento previo de los tópicos presentes en el paper como por ejemplo en que consiste Bandit, y lo otro es que se arrojan muchos conceptos y a veces no se da una explicación clara de lo que es.


Para un futuro trabajo me gustaría ver quizas el rendimineto de las distintas soluciones presentadas. Otra opción podría ser modificar los datasets y observar sis existen cambios, como pueden películas, productos, parejas, etc.