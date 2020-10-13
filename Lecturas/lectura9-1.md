## Crítica: Multi-Armed Recommender System Bandit Ensembles

En este paper se enfoca en los ensembles de sistemas recomendadores, 
que consisten en una forma de construir una recomendador híbrido. La idea principal a implementar 
sería la de un proceso cíclico, en donde en cada reacción del usuario el ensemble observa 
y aprende la efectividad de lo algoritmos v¿combinados, para luego configurar el ensemble. Esto lo realizarían a traves de una adaptación de multi-armed bandit, donde en cada iteración el ensamble elige sistemas combinados para producir la siguiente recomendación.

Por el lado de los elementos presentes en este trabajo se tiene los ensembles de sistemas recomendadores, se presentan como sistemas híbridos, que en general generan solamente una recomendación, la idea sería realizar recomendaciones de forma iterativativa de tal forma de ir computando los mejores parámetros de configuración, siendo una contra al momento de escalar al ser demasiado costosa. Por otro lado se tiene a Bandit, que el funcionamiento que se menciona es similar al A/B testing, donde método de bandit decide entre los algoritmos según la performance que presenten.

En este trabajo se presenta una adaptación de un recomendador bandit, que consiste en 4 partes, el context, arms, reward y updated. Context consiste en el usuario. Arms son los algortimos de recomendación que son combinados en el ensamble. Reward es un variable binaria que dice si el usuario esta satisfecho con la recomendación. Por último updated consiste en que cada arms se va actualizando al realizar una recomendación individual o cierta cantidad de recomendaciones. La selección de cada arms puede ser distintas formas, por lo que acá se ocupan 2 formas E-greedy y Thompson. E-greedy selecciona al que el mejor promedio como puede ser en precision, que es seleccionada con un probabilidad de 1-E. Thompson modela cada arms como un faunción Beta donde los parametros son las recommendaciones exitosas y no exitosas, se calcula un valor p para cada cada arm, donde se elige el que tiene   tiene mayor valor.

Para realizar los experimentos se ocupa el dataset de MovieLens y se ocupan 3 algotimos de recommendación que son kNN, factorización de matriz y most-popular. 

Sobre los resultados se obtienen que los algoritmos de CF no superan en recall a most-popular. Se obtiene que en general los ensamble de bandits tienen una mejora performance que el resto de algoritmos. Por lo encontrado en los resultado se menciona que bandits puede caer en overfitting, pero no en el sesgo de feedback loop. 

Encontre el paper no muy bueno, lo positivo fue la forma en que se realizo la experimentación y como se mostraron de forma clara los resultados. Por otro lado lo negativo del paper fue que solamente se enfocaba en definir las cosas que ocupaban, pero no describir de forma detallada como se realizaba, como lo seria una descripción clara de como Thompson obtiene el valor de p, además encuentro que se pudo agregar más forma de evaluar los sistemas más que solamente con el recall. 


Como paper a futuro ofrece la idea de ocupar bandits en varios algoritmos de recommendación y ver con cual se obtiene un mejor resultado. A su vez poder evaluar el rendimiento de bandits, como también podria mejorar bandits de tal forma de evitar el overfitting. 

