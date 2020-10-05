## Crítica: See What You Want to See: Visual User-Driven Approachfor Hybrid Recommendation

En este paper se presenta Set-Fusion que consiste en una interface visual donde el usuario puede interactuar
con un sistema recomendador híbrido. Lo que principalmente se busca es que las interfaces presenten transparencia, 
explicabilidad y controlabilidad al usuario, a traves de la HCI (Human-Computer Interaction).
visual user-controllable inter-face for hybrid recommender system. Respecto a la visualización se tiene un sistema similar a Set-Fusion 
llamado TalkExplorer, que se diferencia en complejidad y la forma de presentar las entidades e intersecciones, el primero lo realiza a través de un diagrama de Venn y el otro a traveés de clustermaps.
Respecto al uso de un sistema hibrido de recomendación entre CB(content-based) y CF(collaborative filtering), dado que en especial para artículos técnicos CF es más apropiado para recomendar paper nuevos y CB es más apropiado para papers relacionados(por temática).

A continuación en el paper se menciona y se muestran imágenes del funcionamiento de la interfaz de Set-Fusion. Se definen 3 áreas de interaccion, lista de talks recomendadas, sliders donde se modifica la importancia de cada metodo de recomendación y el diagrama de Venn con los distintos conjuntos de las tlaks.

Respecto a los algoritmos usados son 3, el primero es el CB que a través del vector de representación del usuario según su perfil, se realiza cosine similarity con cada vector de documentos. El segundo recomendador es Author-Based Popularity que se basa en rankear todos los papers basado en la popularidad del autor según la cantidad de citaciones. Por último se tiene el recomendador de Bookmark Popularity, que se trata de recomendador no personalizado basado en la popularidad según la cantidad de personas que marcaron la charla.

Por último se muestra resultados de testeo de la interfaz según que elementos fueron clickeados, junto al feedback que se entregó.


En general me gusto la temática que se abordo en este paper, dado que encuentro interesante lo que es la interacción del usuario 
y el sistema recomendador, además que en general las explicaciones son cortas y claras. Por otro lado, algo negativo del paper es que falto explicar como era el funcionamiento de la importancia de cada método en la interfaz. 

Encuentro que la investigación esta muy encasillada en solamente un público y dataset en específico, sería interesante ver una inteerfaz de un estilo más custom en la que se pueda cambiar los sistemas recomendadores a elección, junto al dataset, pero manteniendo la idea de esta interacción usuario-recomendador. 
