Analyse Python — Portefeuille Clients Assurances

Contexte du projet

Une compagnie d'assurances française couvrant les segments Automobile, Habitation et Santé souhaitait analyser son portefeuille clients afin de :


Mieux comprendre la sinistralité par type de contrat et par région
Identifier les clients déficitaires (coûtant plus qu'ils ne rapportent)
Évaluer la performance de ses conseillers
Optimiser sa stratégie de gestion des risques


Objectifs analytiques

Axe d'analyse

Question métier : 

Sinistralité : Quel type de contrat génère le plus de sinistres ? 

Risque géographique : Quelle région concentre le plus de sinistres ? 

Rentabilité : Combien de clients ont un ratio sinistres/primes > 1 ? 

Performance : Quel est le classement des conseillers par satisfaction ?


Démarche analytique

1 - Audit du dataset


Analyse des dimensions (608 lignes × 12 colonnes)
Détection des valeurs manquantes par colonne
Identification des doublons
Analyse des types de variables et valeurs uniques


2 - Nettoyage des données


Suppression des doublons

Imputation des valeurs manquantes :

prime_annuelle → médiane par type de contrat
score_satisfaction → moyenne par conseiller
conseiller → remplacement par "Non assigné"
age → médiane globale

Extraction des variables temporelles depuis date_souscription :

Année de souscription
Mois de souscription
Ancienneté en jours



3 - Analyse de la sinistralité


Calcul du ratio sinistres/primes par client
Identification des contrats déficitaires (ratio > 1)
Analyse du type de contrat dominant chez les clients déficitaires
Classement des régions par volume de sinistres


4 - Performance des conseillers


Tableau de bord multi-métriques par conseiller :

Nombre de contrats gérés
Prime annuelle moyenne
Score de satisfaction moyen
Nombre total de sinistres
Taux de résiliation (%)



Classement par score de satisfaction décroissant
