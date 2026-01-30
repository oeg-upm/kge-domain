# KGE Domain FAIR4ML
Repository to create a formalization of tasks, categories and domains in KGE
## Comparativa de técnicas por campo
En [este enlace](https://docs.google.com/spreadsheets/d/1aU-pKB7QewB-RVnyqguNmcOd31Lt4PS3nFkFHWeHmn8/edit?usp=sharing) se recoge la hoja de GoogleSheets con el resumen de los resultados obtenidos por campo y por modelo.

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

# Taxonomía
## Proceso
La referencia utilizada para modelar la taxonomía es la planteada en el paper de [Shen et al. (2022)](https://doi.org/10.1016/j.knosys.2022.109597)
En esta taxonomía, se plantea una jerarquía de tres niveles. En el nivel principal, se distinguen tres tipos: *Structural information-based KGC Technologies*, *Additional information-based KGC technologies* y *Other KGC Technologies*. Dentro de las dos primeras se plantean dos subgrupos, y de ellos cuelgan los nodos raíz con los tipos ya específicos. Se muestra en la siguiente figura:
![Taxonomy](https://instasize.com/p/44a3ecda5bfc67e668094d11d1ef7835f836824de187b8048142e87597ef77ae)

De esta categorización, se ha empleado por el momento el segundo nivel de la taxonomía, ya que el nivel raíz es demasiado poco específico. En el futuro se explorará el uso del nivel más bajo. Se distingue por tanto en este punto entre: **Semantic Matching Models**, **Translation Models**,**Internal Side Information Inside KGs**, **External Side Information Outside KGs**, **Other KGE Technologies**.

Las definiciones de estas categorías, de acuerdo con el artículo, son las siguientes
|CATEGORY | DESCRIPTION |
|--|--|
|**Semantic Matching Models**| Kind of models which compute semantic matching-based scoring functions by measuring the semantic similarities of entity or relation embeddings in latent embedding space|
|**Translation Models**| Encode entities as low-dimensional embeddings and relations between entities as translation vectors. Defines a relation-dependent translation scoring function to measure te probability of a triple through a distance metric. |
| **Internal side information inside KGs** | Integrates the inherent rich KG information (i.e. internal information) during training time to capture useful features within the embeddings |
| **External extra information outside KGs**| KGE models that exploit external informatiom, such as rules or third-party auxiliary data during training|
|**Other KGC technologies** | KGC techniques oriented to special domains, such as Temporal Knowledge Graphs, Commonsense Knowledge Grahs or Hyper-relational Knowledge Graphs|

# Datasets
(Los datasets específicos de KGE los he buscado y no aparecen en W3id, por ejemplo WordNet sí aparece, pero WN18 o WN18NN que son los que se emplean para KGE no están. Puedo aportar enlaces y referencias porque están recogidas en PyKeen) 



