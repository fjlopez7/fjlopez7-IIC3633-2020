## Crítica: Deep Learning based Recommender System: A Survey and New Perspectives

En esta primera parte del paper se habla principalmente en que consiste los métodos
de deep learning, su importancia en la actualidad y el estado del arte en torno a lo que es uso desde el lado de 
sistemas recomendadores. Junto a eso se mencionan las problematicas de implementar
estos tipos de métodos. 

Como se menciona en el punto 2, deep learning consiste en un sub-campo de machine learning, que en su misión es aprender a realizar una deep representation, que seria lograr a través de múltiples niveles de representación y abtracción de la información. Se considera que cualquier método con arquitectura neuronal diferenciable es deep learning. Algunas de la que se presentan son: multilayer perceptron, autoencoder, convolutional neural network, recurrent neural network, etc.

La razón del uso de deep learning en sistemas recomendadores se debe a 4 aspectos según el texto. Primero esta la transformación no lineal, que dado que las funcions de activación, deep learning permite modelar la no linealidad de los datos. Segundo la representación de aprendizaje, que sería que deep learning permite obtener los factores importantes e útiles de representación de los datos de input. Tercero es Sequence modelling, que se enfoca en el deep learning tiene muy buenos resultados en este tipo de modelamiento, que serian procesamiento de lenguaje natural, reconocimiento del habla,etc... Por último estaría la flexibilidad, dada la tan alta cantidad de frameworks qe ofrecen métodos de deep learning.

Por otro lado se presnetan los disitntos problemas que puede tener el uso de deep learning que serian la interpretabilidad al ser un método de caja negra y sería díficil explicar la predición. Otro problema es la cantidad de información de necesaria al ser necesario dataset muy grandes. El tuneo de hiperparametros sería otro problema al ser de forma muy extensa. 


Respecto al estado del arte se presentan algunos métodos de deep learning. En un principio se muestran las categorias de los modelos de recomendación en base a deep learning, que serian los modelos de bloques de deep learning como MLP o CNN y los modelos híbridos que juntan 2 o más métodos de deep learning. Se presentan distintos modelos en base a MLP. Luego en base a los autoencode. Por último para esta lectura serian el caso de CNN. En este último me llamo la atención el uso de grafos con CNN, sería interesante leer un poco más sobre esta temática. 


Respecto a lectura la encuentro un poco densa, dado que es cierto que da un buena pincelada de introducción a deep learning, pero por otro lado cuando se empieza a hablar sobre los distintos métodos la dificultad de la lectura aumenta, dada a que en general se asume un conocimiento previo de los tópicos que se presentan. 

Me hubiera gustado una mejor explicación en especial en la parte 3, donde todo esta muy denso al requerir un mayor conocicmiento de los tópicos que se hablan. 
