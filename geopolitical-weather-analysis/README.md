# Carte Géopolitique et Météorologique Mondiale — Power BI

## 1. Présentation du projet
Ce projet consiste à développer un rapport cartographique interactif sous Power BI combinant des données géopolitiques, socio-démographiques et météorologiques mondiales[cite: 12, 13, 22]. L'objectif est d'agréger plusieurs sources de données externes via API REST afin de visualiser et comparer dynamiquement les indicateurs clés de chaque pays (population, superficie, température, vitesse du vent) tout en fournissant une fiche détaillée au survol[cite: 13, 15, 17, 18, 22, 23, 24, 25, 26].

## 2. Technologies utilisées
* **Power BI Desktop & Power BI Service** : modélisation relationnelle, carte choroplèthe interactive, info-bulles personnalisées et publication en ligne.
* **Power Query (Langage M)** : ingestion d'API REST, création d'une fonction personnalisée dynamique, dépivotage et normalisation des données.
* **DAX (Data Analysis Expressions)** : création d'une table de paramètres (`Metrics Table`), sélection dynamique d'indicateurs (`SWITCH`, `SELECTEDVALUE`) et agrégation textuelle (`CONCATENATEX`).
* **API externes** : *REST Countries* (données pays), *Open-Meteo* (météo en temps réel), *Flagpedia* (drapeaux) et *OpenWeatherMap* (icônes météo)[cite: 12, 13, 15, 17, 18, 19, 21].

## 3. Démarche et réalisations
* **Ingestion et préparation (ETL)** : extraction des données JSON depuis l'API *REST Countries*, typage, séparation des coordonnées géographiques et création de tables de dimensions dédiées (*Continents*, *Langues*, *Monnaies*) par dépivotage pour éviter la duplication des lignes[cite: 13, 14, 15, 16].
* **Enrichissement dynamique par API** : développement d'une fonction personnalisée en langage M interrogeant l'API *Open-Meteo* à partir des coordonnées GPS de chaque pays, couplée à une table de correspondance des codes météo (`weather_code.txt`) et aux URL des drapeaux[cite: 15, 16, 21].
* **Visualisation cartographique dynamique** : conception d'une carte choroplèthe avec échelle colorimétrique pilotée par un sélecteur de métrique DAX (*Population*, *Superficie*, *Température*, *Vitesse du vent*) et filtres multicritères (*Continents*, *Langue*, *Météo*)[cite: 16, 17, 18, 22, 23, 24, 25].
* **Info-bulle personnalisée (Tooltip)** : création d'une fiche pays affichant au survol les indicateurs démographiques, les données météo actuelles, le drapeau national et l'icône météo via le visuel personnalisé *Simple Image*[cite: 12, 18, 19, 26].

## 4. Résultats obtenus
* **Centralisation multi-sources** : modèle relationnel automatisé croisant données structurelles des pays et relevés météorologiques actualisables en temps réel[cite: 15, 16, 19, 20].
* **Exploration interactive** : bascule instantanée entre quatre indicateurs mondiaux sur une seule carte et affichage détaillé par pays sans surcharger l'interface principale[cite: 18, 22, 23, 24, 25, 26].