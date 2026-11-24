# Analyse Exploratoire et Modélisation du Catalogue Netflix — Python

## 1. Présentation du projet
Ce projet porte sur le nettoyage, la structuration et l'analyse exploratoire d'un jeu de données recensant le catalogue de films et séries Netflix (`netflix_titles.csv`)[cite: 27, 28]. L'objectif est de fiabiliser des données brutes hétérogènes, de normaliser les attributs multi-valeurs et d'en extraire des indicateurs clés sur la composition éditoriale, la temporalité des ajouts et la répartition géographique des contenus.

## 2. Technologies utilisées
* **Python 3** : environnement de développement principal.
* **Pandas & NumPy** : nettoyage des données, gestion des types, manipulation de chaînes de caractères, explosion de colonnes multi-valeurs (`explode`), jointures et agrégations statistiques.
* **Jupyter Notebook** : structuration et documentation interactive de l'analyse.

## 3. Démarche et réalisations
* **Nettoyage et typage (Data Cleaning)** : importation avec gestion de l'encodage (`latin1`), suppression des colonnes vides (`Unnamed`), indexation par identifiant unique (`show_id`), conversion des dates (`date_added`) et extraction des composantes temporelles (année, mois, jour de la semaine).
* **Normalisation des données** : séparation de la colonne `duration` en deux variables numériques distinctes (durée des films en minutes et nombre de saisons des séries) et création de tables annexes normalisées pour les pays, les genres et les acteurs (`to_csv`).
* **Analyse exploratoire (EDA)** : requêtage statistique, filtrage textuel et croisements relationnels (`merge`) pour répondre à 10 problématiques métiers.

## 4. Résultats obtenus
* **Volume et formats** : **8 809 titres** analysés, répartis entre **6 132 films** (69,6 %) et **2 677 séries TV** (30,4 %).
* **Durée et format des contenus** : les films durent en moyenne **99,6 minutes** (médiane à 98 min) et les séries comptent en moyenne **1,76 saison**[cite: 27].
* **Dynamique d'ajout** : pic d'ajouts enregistré en **2019** (2 016 titres) et forte concentration des publications le **vendredi** (2 500 titres).
* **Tendances éditoriales et géographiques** : dominance des *International Movies* (2 752 titres) et des *Dramas* (2 427 titres), prépondérance des États-Unis dans la production de documentaires (511 titres) et identification de **158 titres** abordant la thématique de la drogue.