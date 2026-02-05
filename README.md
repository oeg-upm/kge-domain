
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
|Knowledge Graph Embedding| Embed components of a KG including entities and relations into continuous vector spaces  | [Wang et al. (2017)](https://doi.org/10.1109/TKDE.2017.2754499)|
|Information Retrieval|Finding material of unstructured nature that satisfies an information need from within large collections | [Manning et al. (2009)](https://nlp.stanford.edu/IR-book/information-retrieval-book.html)|
|Reinforcement Learning|Learning what a system should do -how to map situations to actions- so as to maximize a numerical reward signal.|[Sutton&Barto (2014)](https://web.stanford.edu/class/psych209/Readings/SuttonBartoIPRLBook2ndEd.pdf)|
|Question Answering|Task that aims to answer natural language questions with a KB acting as its knowledge source|[Lan et al. (2022)](https://doi.org/10.1109/TKDE.2022.3223858)|
|Link Prediction|Predicting whether two nodes in a network are likely to have a link|[Zhang&Chen (2018)](https://proceedings.neurips.cc/paper_files/paper/2018/file/53f0d7c537d99b3824f0f99d62ea2428-Paper.pdf)|
|Knowledge Graph Completion|Predict and replenish the missing part of triples within a Knowledge Graph|[Shen et al. (2022)](https://doi.org/10.1016/j.knosys.2022.109597)|
|Representation Learning|A set of techniques that allow a system to discover different representations of the data|[Sakhnini et al. (2021)](https://doi.org/10.1016/j.knosys.2022.109597)|
|Recommendation systems|Information filtering systems that deal with the problem of information overload by filtering vital information fragments out of large amount of dinamically generated information according to user's preferences, interest or observed behavior. |[Isinkaye et al. (2015)](https://doi.org/10.1016/j.eij.2015.06.005)|

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
En [PyKeen](https://github.com/pykeen/pykeen?tab=readme-ov-file) se listan varios datasets, pero en los papers analizados no aparecen todos ellos. En esta tabla se recogen sólo los que aparecen en los papers estudiados:
| DATASET | REFERENCE |
| -- | -- |
| DBpedia50 | [Shi et al. (2017)](https://arxiv.org/abs/1711.03438) |
| FB15k | [Bordes et al. (2013)](http://papers.nips.cc/paper/5071-translating-embeddings-for-modeling-multi-relational-data.pdf) |
| FB15k-237 | [Toutanova et al. (2015)](https://www.aclweb.org/anthology/W15-4007/)|
| Freebase | [Bollacker et al. (2008)](https://research.google/pubs/freebase-a-collaboratively-created-graph-database-for-structuring-human-knowledge/)
| WN18 | [Bordes et al. (2014)](https://arxiv.org/abs/1301.3485)
| WN18-RR | [Toutanova et al. (2015)](https://www.aclweb.org/anthology/W15-4007/)
| NELL | [Mitchell et al. (2010)](http://rtw.ml.cmu.edu/rtw/)
| YAGO3-10 | [Mahdisoltani et al. (2015)](http://service.tsi.telecom-paristech.fr/cgi-bin//valipub_download.cgi?dId=284)

# Métricas
(Esta es la parte con la que estoy ahora)




