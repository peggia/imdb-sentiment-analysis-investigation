# imdb-sentiment-analysis-investigation

Ce projet s’inscrit dans le cadre du cours CNAM RCP209 Apprentissage statistique 2 : modélisation décisionnelle et apprentissage profond.
## Objectif
L’objectif du projet est d'explorer des modèles d’apprentissage statistique (Machine Learning) permettant de classer des critiques de films comme étant positives ou négatives, en analysant le texte de la critique.

Il s'agit d'un exemple d’analyse de sentiments des textes dont le résultat est une classification binaire (1 ou 0) qui indique l’appartenance à la classe “positive” ou pas (donc négative sinon).


Le domaine de l’analyse des sentiments, ainsi que les classifications sont des problèmes d'apprentissage automatique largement répandus et avec des nombreuses applications.
## Définition de l’Analyse des sentiments
“En informatique, l'opinion mining (aussi appelé sentiment analysis) est l'analyse des sentiments à partir de sources textuelles dématérialisées sur de grandes quantités de données (big data)...

L'objectif de l’opinion mining est d'analyser une grande quantité de données afin d'en déduire les différents sentiments qui y sont exprimés. Les sentiments extraits peuvent ensuite faire l'objet de statistiques sur le ressenti général d'une communauté.”
https://fr.wikipedia.org/wiki/Opinion_mining
## Jeu de Données
Nous allons utiliser l'ensemble de données IMDB “Large Movie Review Database”. 

Le lien vers le dataset :
https://ai.stanford.edu/~amaas/data/sentiment/

## Approche
Pour accomplir la tâche de classification demandée, nous allons explorer deux algorithmes de Machine Learning traditionnel et trois architectures Deep Learning.
### Machine Learning Traditionnel
Dans la catégorie Machine Learning traditionnel, deux méthodes considérées comme étant efficaces pour les tâches de classification binaire, comme celle qui nous concerne (critique positive ou négative), seront explorées :
- Un modèle de Régression Logistique
- Un modèle basé sur des Forêts Aléatoires.
### Deep Learning: Réseaux de Neurones Récurrents
Dans la catégorie Deep learning, nous allons d’abord tester deux exemples de Réseaux de Neurones Récurrents (RNNs) avec des types de cellules améliorées:
- Une architecture basée sur une couche Gated Récurrent Unit (GRU)
- Une architecture avec une couche Long Short-Term Memory (LSTM)
### Deep Learning: Transfer Learning (module pré-entrainé)
Et pour finir, nous regarderons un exemple de “Transfer Learning” qui réutilise un module pré-entrainé d’Embedding (vectorisation) des mots, disponible de la librairie TFHub de Tensorflow.
## Méthode d’évaluation des modèles
Nous allons utiliser l’exactitude (accuracy) en entrainement et en test pour évaluer et comparer les différents modèles de classification. 
Dans notre cas, le jeu de données IMDB utilisé contient deux classes qui sont équilibrées (25000 critiques positives, 25000 critiques négatives).
Donc c’est une métrique adaptée pour comparer les différents modèles.
L’Accuracy (exactitude) mesure la proportion de critiques correctement classées.

