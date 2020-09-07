## Crítica: Content-Based Recommendation Systems 

En este paper se nos habla primero de distintas formas de representar items y luego distintos 
algoritmos recomendadores basados en contenidos.

La forma de representar datos serían los estructurados y los no estructurados. 
Entre los estructurados se encontraria la información en tablas de bases de datos.
Un ejemplo de dato no estructurado sería un artículo de noticia. Siendo el principal problema de este último 
es que no existe informacipon directa para generar una recomendación, por lo que se nos presenta una forma de obtener más 
información sobre el texto, esto sería el tf*idf weight que corresponde a una función que calcula la frecuencia de 
términos en un documento. un problema de esto es que se pierde el valor del contexto de las parabras.

Entre los algoritmos que son ocupados acá varios son de machiine learning , pero para lagunos de ellos se tiene que relizar 
un preporcesamiento de los datos para ocuparlo. Los algoritmos son: Decision Trees and Rue induction, Nearest Neighbor Methods, 
Relevance Feedback and Rocchio'ss Algorithm, Linear Classifiers y por último Naïve Bayes.

Encuentro que el más importante de mencionar sus características es el de Relevance Feedback and Rocchio'ss Algorithm, dao que es 
el algoritmo que no he visto anteriormente en algún ramo de machine learning.  Relevance feedback consiste en que el usuario den rate a los documentos
segpun la información que necesitaban, enofecandose en lo que son las queries de palabras claves para las búsquedas . 
Rocchio's algorithm usa esta idea para generar un algoritmo iterativo incremental con las queries se buscan documentos relevantes y no relevantes.

Encuentro que la lectura fue muy introductoria, dado que en general se muestra el estado del arte de recomendación 
basada en contenido. Me hubiera gustado que indagaran más en los algoritmos y explicar de una forma más aclarativa.
