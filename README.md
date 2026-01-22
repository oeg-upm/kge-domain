# kge-domain
Repository to create a formalization of tasks, categories and domains in KGE

## Tasks
### Proceso
La etiqueta de las clases la hemos minado directamente de Papers with Code, pero en muchos casos se observan duplicidades en etiquetas que representan lmismo, por ejemplo, en un paper se han identificado las siguientes tres tareas de acuerdo a Papers with Code:

    ['Graph Embedding'], ['Knowledge Graph Embeddings'], ['Knowledge Graph Embedding']

Las tres etiquetas se pueden homogeneizar en una sola (y de hecho tendría más sentido). Hemos probado con lógica borrosa, con jerarquías cuando aún existía la API de PwC (⚰️) y nati. Al final la solución más sencilla resultó ser la más eficiente: hicimos un clústering con las etiquetas y homogeneizamos las etiquetas. Estas tareas ya homogeneizadas son las que se describen en la tabla.
### Definición
|TASK  | DESCRIPTION | REFERENCE |
|--|--|--|
|Knowledge Graph Embedding| Embedding entities and relationships of multi-relational data in low-dimensional vector spaces  | Duda, las referencias tienen que ser a algo en concreto? Tipo a otra cosa de W3C o como? La primera definición que se dio fue en el paper de TransE|
|Information Retrieval|A process through which rant information is obtained and delivered based on specific information needs | #REF|
|Reinforcement Learning|Learning paradigm concerned about how an intelligent agent takes actions in a dynamic environment in order to maximize a reward function.|#REF|
|Question Answering|Automatically answering questions posed by humans in natural language |#REF|
|Link Prediction|Predicting the existence of a potential link between two nodes in a graph|#REF|
|Knowledge Graph Completion|**SUELE USARSE EN CONJUNTO CON LOS KGEs, pero no siempre** Predicting missing elements in incomplete knowledge graphs (triples, relations, or entities)|#REF|
|Representation Learning|Learning useful features automatically from data|#REF|
|Recommendation systems|System aimed to learn a filtering criteria to predict the preference hat a user would give to an element |#REF|
