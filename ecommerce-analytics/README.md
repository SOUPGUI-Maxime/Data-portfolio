# Analyse des ventes E-commerce — Tableau de bord Power BI

## 1. Présentation du projet
Ce projet consiste à concevoir un rapport décisionnel interactif sous Power BI à partir d'un jeu de données de transactions e-commerce (`sales_2.csv`). L'objectif est de structurer un modèle de données relationnel fiable afin de piloter la performance commerciale globale et d'identifier les facteurs d'annulation des commandes par région, période et catégorie de produits.

## 2. Technologies utilisées
* **Power BI Desktop & Power BI Service** : modélisation, création de visualisations interactives, configuration mobile et publication en ligne.
* **Power Query** : nettoyage, contrôle de la qualité des données et normalisation en schéma en étoile.
* **DAX (Data Analysis Expressions)** : création d'une table dédiée et développement d'indicateurs clés (KPI) dynamiques.
* **JSON** : intégration d'un thème graphique personnalisé et utilisation d'un visuel personnalisé (`PayPal KPI Donut Chart`).

## 3. Démarche et réalisations
* **Préparation et modélisation** : audit de qualité sous Power Query, renommage des colonnes, puis normalisation des données brutes en une table de faits (`Ventes`) reliée à trois tables de dimensions (`Clients`, `Produits`, `Régions`).
* **Calculs métiers (DAX)** : création des mesures principales (chiffre d'affaires, volume de commandes, quantité vendue, panier moyen) et des indicateurs d'annulation (volume, montant, taux).
* **Conception du rapport (2 pages)** :
  * *Suivi des ventes* : KPI globaux avec jauge de filtrage dynamique, évolution temporelle, répartition par région et catégorie, et tableau détaillé des commandes.
  * *Suivi des commandes annulées* : analyse de l'évolution mensuelle et trimestrielle (graphique en ruban), répartition géographique et par produit (treemap).
* **Expérience utilisateur et sécurité** : ajout d'un menu de navigation, de signets de filtrage rapide (*Mobiles*, *Bureautique*, *Réinitialisation*), d'info-bulles personnalisées au survol, d'une vue mobile et de règles de sécurité au niveau des lignes (Row-Level Security par client et région).

## 4. Résultats obtenus
* **Performance globale (2023)** : **2 M€** de chiffre d'affaires générés sur **500 commandes** (**3 109 unités** vendues), pour un panier moyen de **771 €**.
* **Répartition produit** : la catégorie *Electronics* représente **62,26 %** du chiffre d'affaires (1,5 M€) contre **37,74 %** pour *Accessories* (0,9 M€).
* **Analyse des annulations** : **123 commandes** annulées sur la période, représentant un taux d'annulation de **25 %** et un manque à gagner de **550 K€**.
