# Clustering multimodal des restaurants Yelp

*Identifier les ambiances et types d’expérience des restaurants à partir des données Yelp*

**Auteur :** Tania ADMANE, Ndoumbé BAYO, Tea TOSCAN DU PLANTIER 
**Date :** Janvier 2026

![Python](https://img.shields.io/badge/Python-3.10.15-blue)

---

## Objectif du projet

Ce projet vise à identifier les **ambiances** et **types d’expérience** proposés par les restaurants à partir des données Yelp, en allant au-delà de la simple note globale.

Lorsqu’on visite une ville pour la première fois, il est souvent difficile de choisir un restaurant uniquement sur la base de sa note moyenne. Une note élevée ne garantit pas nécessairement une expérience correspondant à ses attentes, et peut conduire à une déception. Deux restaurants très bien notés peuvent en réalité proposer des expériences radicalement différentes.

L’objectif est donc de **segmenter les restaurants selon l’expérience vécue**, en exploitant conjointement plusieurs sources d’information.

---

## Approche

Nous adoptons une approche de **clustering multimodal**, basée sur :

- les **avis textuels** (analyse sémantique),
- les **images** publiées sur Yelp,
- les **notes et variables numériques**,

Cette approche permet de regrouper les restaurants en catégories plus interprétables pour l’utilisateur final, telles que :
- restaurants attrape-touristes,
- restaurants authentiques,
- bonnes adresses méconnues,
- lieux festifs ect 

---

## Méthodologie

- **Textes** :  
  Encodage des avis clients à l’aide de **SBERT**, afin de capturer les nuances sémantiques et les différents aspects de l’expérience décrite dans les avis.

- **Images** :  
  Extraction d’embeddings visuels via **CLIP**, permettant de représenter l’ambiance visuelle des restaurants (décor, plats, atmosphère).

- **Fusion multimodale** :  
  Combinaison des embeddings textuels, visuels et des variables numériques dans un espace commun.

- **Réduction de dimension** :  
  Utilisation de **UMAP** pour projeter les représentations dans un espace de dimension réduite tout en conservant la structure locale des données.

- **Clustering** :  
  Application de **HDBSCAN**, un algorithme de clustering hiérarchique dense, permettant d’identifier automatiquement le nombre de clusters et de gérer le bruit.

---

## Structure du projet

├── main.ipynb
│ └── Clustering basé sur les avis textuels + features numériques
│
├── main_avec_photos.ipynb
│ └── Clustering multimodal (texte + images + features numériques)
│
├── traitement_donnees_features et analyse_descriptive.ipynb
│ └── Prétraitement des variables numériques et analyse descriptive
│
├── traitement_NLP.ipynb
│ └── Prétraitement des avis textuels et génération des embeddings
│
├── exploration_clip_embedding.ipynb
│ └── Traitement des images et extraction des embeddings visuels




## Données

Les données utilisées concernent exclusivement les **restaurants de la ville de Philadelphie**, préalablement filtrés à partir de la base Yelp.

Accès aux données :  
https://drive.google.com/drive/folders/1TGKSyMR1O96ClNZo47HqJ_w3h1SAo8lZ?usp=sharing

