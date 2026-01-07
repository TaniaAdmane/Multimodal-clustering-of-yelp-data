# Identifier les ambiances et types d’expérience des restaurants grâce à une analyse multimodale des données Yelp

L’objectif de ce projet est d’identifier, à partir des avis Yelp, les différentes ambiances et types d’expérience proposés par les restaurants.

L’idée de départ est la suivante : lorsqu’on visite une ville pour la première fois, il est souvent difficile de choisir un restaurant en se basant uniquement sur la note globale. Une bonne note ne garantit pas forcément une expérience adaptée à ce que l’on recherche, et peut parfois mener à une déception.

L’objectif est donc d’analyser les différentes données disponibles dans la base :

- les avis textuels,

- les photos,

- les notes,

- le type de clientèle, etc.,

Afin de regrouper les restaurants en catégories plus parlantes pour les utilisateurs, comme par exemple : restaurants attrape-touristes, restaurants authentiques, bonnes adresses méconnues, lieux festifs, restaurants familiaux, etc.

## Organisation du projet

Le premier traitement des données numériques se trouve dans le fichier traitement_donnees_features.

Le traitement des images est réalisé dans exploration_clip_embedding.ipynb.

Le traitement des textes est effectué dans traitement_NLP.ipynb.

La génération et l’analyse des clusters sont réalisées dans main.ipynb.

Les données des restaurants de la ville de Philadelphie sont disponibles ici :
https://drive.google.com/drive/folders/1TGKSyMR1O96ClNZo47HqJ_w3h1SAo8lZ?usp=sharing