# L'Arène des Algos — HELALI Yanis

## Objectif
Ce dépôt contient mon travail de la semaine sur le Machine Learning, dans le cadre du fil rouge **L'Arène des Algos**.

L'objectif est de comparer plusieurs algorithmes de Machine Learning sur différents jeux de données, puis de justifier le choix du meilleur modèle selon plusieurs critères :
- performance,
- simplicité,
- explicabilité,
- robustesse.

## Contenu prévu du repo
Ce repo contiendra :
- les notebooks du jour 1 à jour 5,
- les expérimentations sur les datasets,
- les comparaisons d'algorithmes,
- les visualisations,
- les résultats et analyses,
- un résumé des choix effectués.

## Organisation
- `notebooks/` : notebooks de travail
- `src/` : éventuels scripts Python
- `data/` : jeux de données locaux si nécessaire
- `images/` : captures, graphiques et figures

## Jour 1
Phase 0 : mise en route du projet
- création du repo GitHub,
- initialisation du dépôt local,
- création de l'arborescence,
- ajout du README.

## Avancement

### Jour 1
- [x] Phase 0 : setup du repo
- [x] Phase 1 : chargement et exploration du dataset `load_breast_cancer`
- [x] Phase 2 : pipeline supervisé complet
- [x] Phase 3 : arène des algorithmes
- [x] Phase 4 : clustering non supervisé
- [x] Phase 5 : changement de dataset
- [x] Phase 6 : visualisations
- [x] Phase 7 : scaling et data leakage
- [ ] Phase 8 : synthèse finale


## Jour 2 — Collecte et preprocessing

### ✅ Phase 0 — Chargement des données
- dataset Telco Customer Churn récupéré depuis Kaggle
- chargement du CSV
- vérification des dimensions et types

### ✅ Phase 1 — Audit qualité
- analyse des dimensions du dataset
- étude des types de variables
- détection des valeurs manquantes
- analyse du déséquilibre de la cible (Churn)

### ✅ Phase 2 — Nettoyage de TotalCharges
- détection de valeurs non numériques (espaces)
- conversion en float
- révélation de valeurs manquantes
- imputation par la médiane

### ✅ Phase 3 — Encodage des variables
- transformation des variables Yes/No en 0/1
- application du One-Hot Encoding
- suppression de customerID
- dataset entièrement numérique

### ✅ Phase 4 — Outliers
- détection avec boxplot et IQR
- analyse des valeurs extrêmes
- décision métier : conservation des outliers

### ✅ Phase 5 — Corrélations et multicolinéarité
- visualisation des corrélations (heatmap)
- détection des variables fortement corrélées
- calcul du VIF
- suppression de TotalCharges

### ✅ Phase 6 — Variables discriminantes
- classement des features par corrélation
- analyse avec Random Forest
- identification des facteurs principaux du churn


## Jour 3 — Algorithmes de Machine Learning

### ✅ Phase 0 — Setup
- reprise du dataset Telco nettoyé
- preprocessing réappliqué
- données prêtes pour l’entraînement des modèles

### ✅ Phase A — Arène des algorithmes
- comparaison de plusieurs modèles :
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - KNN
- classement basé sur l'accuracy
- visualisation des performances
- identification du meilleur modèle

### ✅ Phase B — Optimisation
- tuning des hyperparamètres
- amélioration des performances
- comparaison des meilleurs modèles

### ✅ Phase C — Pipeline et Data Leakage
- création d'un pipeline sklearn
- scaling et entraînement propre
- démonstration d’un cas de data leakage
- bonnes pratiques pour éviter les erreurs

### ✅ Phase D — Évaluation avancée
- matrice de confusion
- classification report (precision, recall, F1-score)
- analyse des erreurs
- interprétation métier du churn


### ✅ Phase E — Bilan
- comparaison finale des modèles
- sélection du meilleur modèle
- analyse des performances
- conclusion métier



## Conclusion

Ce projet a permis de mettre en œuvre un pipeline complet de Machine Learning :

- préparation et nettoyage des données
- comparaison de plusieurs modèles
- optimisation des performances
- analyse approfondie des résultats

Le modèle le plus performant est le Random Forest, offrant
le meilleur compromis entre performance et robustesse.

Ce travail illustre l’importance du preprocessing et du choix
des modèles dans un contexte réel.


## Auteur
Yanis HELALI