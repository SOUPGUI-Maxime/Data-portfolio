# Analyse des Accidents de la Route à New York (2020) — Excel

## 1. Présentation du projet
Ce projet consiste à analyser les accidents de la route survenus à New York en 2020 à partir du jeu de données brut `NYC Accidents 2020.csv`. L'objectif est de nettoyer et structurer un volume important d'enregistrements afin d'identifier la temporalité des collisions, les zones géographiques les plus touchées, la gravité des accidents ainsi que leurs causes principales.

## 2. Technologies utilisées
* **Microsoft Excel** : création de tableaux croisés dynamiques (TCD), formules de calcul et graphiques analytiques.
* **Power Query** : nettoyage des données, renommage des champs et normalisation des attributs multi-valeurs par dépivotage.

## 3. Démarche et réalisations
* **Préparation et modélisation des données** : nettoyage de la table principale (`NYC Accidents 2020`, 74 881 lignes) et séparation des colonnes multi-valeurs en deux tables normalisées distinctes (`Type de véhicule` et `Facteurs explicatifs`) pour fiabiliser les agrégations.
* **Exploration thématique (4 onglets dédiés)** :
  * *Analyse macro* : synthèse des indicateurs clés et étude de la distribution temporelle (par mois, jour de la semaine et heure).
  * *Analyse géographique* : répartition des accidents par arrondissement (borough) et par type de voie.
  * *Analyse gravité accident* : calcul du ratio de blessés par accident et comparaison entre arrondissements.
  * *Analyse type d'accident* : identification et classement des facteurs explicatifs des collisions.

## 4. Résultats obtenus
* **Bilan global** : **74 881 accidents** recensés sur la période étudiée, causant **27 448 blessés** et **144 décès**.
* **Répartition géographique** : **Brooklyn** (16 907 accidents) et le **Queens** (14 017 accidents) enregistrent le plus grand nombre de collisions parmi les arrondissements renseignés, avec une proportion de blessés par accident stable d'un quartier à l'autre.
* **Tendances et causes** : recul notable des accidents en avril suivi d'une hausse progressive jusqu'en été ; l'inattention au volant ressort comme la première cause de collision.