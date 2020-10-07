## Crítica: Inspectability and Control in Social Recommenders

En este paper se centra en sistemas recomendadores sociales, pero en especifíco se toma en cuenta al usuario que controla que tanto influye en la recomendación sus amigos o sus vecinos cercanos. Además de esto se realiza un experimento con usuarios con un recomendador de mpusica de Facebook.

Respecto al usuarios, se presenta que aprecian que el sistema sea explicativo al momento de recomendar, al haber mayor transparencia. Además aprecian tener el control al momento de interactuar con el recomendador, dado que esto permite dar distintas valoraciones a los items y/o a sus amigos.

El recomendadodor social que se presenta tiene de nombre TasteWights modificado. Consiste en un grafo ordenado en 3 columnas en la primera se encuentran distintos grupos músicales, en la segunda están los usuarios de Facebook y en la tercera esta la recomendación, entre cada columna están las aristas que conectan los nodos que están en cada grafo. El sistema consiste en recomendar nuevos artistas al usuario según sus gustos y los de sus amigos. Para ver la similaridad y peso entre amigos se realiza a través de la correlación de Pearson, luego de calcular los pesos de todos los amigos, se realiza la recomendación mediante la asignación de pesos a todos los items de los amigos del usuario. 

Con los experimentos realizados se obtuvo que en general que dar la posisilidad de inspeccionar y de control al usuario, realiza que sea más fácil el entender como funciona el sistema recomendador. Lo que se concluye en que esto permite mejorar la experiencia de los usuarios y que se tomen un mayor tiempo usando el recomendador.


Encontre muy interesante la idea que se propone y como se fue llevando en el paper, dado que esta forma de plantear al usuario el sistema recomendador permite mejor en varios sentidos la perspectiva que se tiene como puede ser la novedad, la credibilidad, etc... 

Respecto a los aspectos que no me gustaron del paper, es la presentación de los datos del experimento, dado que los encontre ciertamente confusos, al no tener un orden claro.

Sería interesante ver un trabajo en donde se mezcle está idea de utilizar usuarios foreanos y no solamente amigos, dado que quizas los amigos no tienen gustos tan cercanos y que los usuarios foreanos pueden agregar mayor valor a la hora de recomendar.