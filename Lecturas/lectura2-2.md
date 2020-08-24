## Crítica: BPR: Bayesian Personalized Ranking from Implicit Feedback

En este papaer el enfoque es de encontrar un metodo que sea mejor al descenso de gradiente estandar. Por lo que se propone el uso de el algoritmo de aprendizaje LearnBPR.

Antes de empezar a analizar la implementación se propone una organización de de los datos que consiste en ir comparando los items con los items respecto a los distintos usuarios. Con el operador ">u" que nos dice que si es que para el respectivo usuario el item i tiene mejor ranking que el item j. Para la data de practica se forman tuplas de 3 donde la primera es un usuario, los otros son items i , j que cumplen con i >u j.

Para el caso del LearnBPR, primero se debe obtener un estimador de siendo los passos a seguir calcular la función de probabilidad, realizar logaritmo natural de la función y por último derivar según el estimador. Al momento de realizar la función de ln a la probabilidad se tiene a BPR-Opt. Con esto calculado se tiene cuanto va avanzando el algoritmo de descenso en cada iteración según lo que se obtiene de la derivada de BPR-Opt, siendo este descenso LearnBPR. La reorganización de los datos se realiza, porque al momento de calcular la función de probabilidad se deben tomar a todos los usuarios, pero con algunos cambios queda con solamente el conjunto de las tuplas de 3 de usuario e items.

Se observa claramente que el los resultados de este formato de descenso son realmente buenos al resto de implementaciones. 

El paper lo encontre un poco denso, debido a que tiene mucha estadística y a un nivel alto. Que a su vez se combina con elementos de matemáticas discretas, que realmente considero raro al ser mi primera vez enfrentandome a algo de este estilo.

Por otro lado considero que realizaron un muy buen trabajo, dado que realizaron una buena comparación respecto a las otras opciones posibles y se observa que mejoro la predicción de ratings.