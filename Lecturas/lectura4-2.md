## Crítica: Document clustering based on non-negative matrix factorization.

En este paper nos muestran un método para una mejor búsqueda de documentos a traves de clustering. 
Los métodos para realizar este trabajo se han categorizado en dos tipos agglomerative y document partitioning.  
El primero consiste en un constrir un árbol jerarquico, el que se forma a través de la unión iterativa de pequeños 
clusters que cumplan con ser similares. Siendo una de las problematicas de este método su complejidad que es de O(n^2*log n). 
Por otro lado, document partitioning como su nombre lo dice se enfoca en ir particionando el cluster según los criterios de alguna función.
En esta categoría están los métodos de K-means, probalibidad con Naive Bayes, probabilidad gaussiana. Otra forma de realizar el clustering es LSI, 
que consiste en proyectar el documento al espacio de vectores singulares a traves de SVD, pero el problema de este es que los vectores propios no necesariamente
corresponden a algún cluster, implicando en tener que utilizar a su vez otro método de clustering.


Ante la problematica de LSI se propone el uso de NMF, que cumple primero en que los vectores no necesariamente tienen que ser ortogonales como lo son en SVD y 
que los vectores de NMF indican las particiones de los clusters. NMF para funcionar primero se forma el espacio de vectores que es a través de la frecuencia 
de palabras presentes en el corpus. De esta forma para queda una matriz X donde los documentos son las columnas y las filas son las frecuencias de las palabras.
El objetivo de NMF es factorizar X en una matriz U y V que cumplen con ser no negativas, lo que se realiza a través de una función de minimización con estas tres matrices. 

El problema de factorizar X se resuelve con multiplicadores de lagrange, de la que se obtienen formulas de actualización para cada elemento de las matrices u y v.
Luego de obtener U y V falta normalizar. Por último, se ocupa la matriz V para obtener el cluster al que pertenecen cada uno de los documentos. 

De los resultados comparativos entre NMF y LSI se observa que sus espacios son totalmente distintos. en especial se de observa que en el espacio de NMF que 
cada eje corresponde a un eje y que el mismo cluster est presente en el mismo eje. En cambio, para LSI no existe relación entre los ejes y clusters. 

Por último en el paper se comparan dos corpus, juntos a distintas metricas que se mencionan en el paper. 
Donde luego se compara la performance de NMF en estos dos corpus, según las metricas.

Encontre el paper muy interesante, dado a la temática del paper y a la forma en que se va relatando. Siendo un punto fuerte que ofrece una buena explicación del tema, 
pero por otro lado un punto débil sería la necesidad de conocimiento previo en tópicos de probabilidad y optimización. 

Me hubiera gustado ver un poco la comparación en rendimiento y tiempo entre SVD y NMF, para ver si vale la pena tener que ocupar este método de clustering.
