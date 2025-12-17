#  Analyse des Ventes, Promotions & Pertes – Dashboard Power BI

##  Auteur

**Donatien Fofana**
Étudiant en L3 MIAGE – Université Grenoble Alpes
Projet personnel orienté **Data Analyst / Business Intelligence** 


##  Objectif du projet

Ce projet vise à analyser la performance commerciale d’un supermarché à travers un dashboard Power BI interactif, afin d’aider à la prise de décision stratégique.

Les objectifs principaux sont :

* Identifier les produits les plus rentables
* Mesurer l’impact réel des promotions sur la marge
* Détecter et quantifier les pertes financières
* Proposer des recommandations business basées sur les données

## Données utilisées

* Données de ventes (2020 – 2023)
* Données produits et catégories
* Données de promotions
* Données de pertes (retours, invendus, anomalies par magasin)

📌 *Les données sont issues d’un jeu de données type Kaggle et ont été nettoyées et modélisées dans Power BI.*


##  Outils & Compétences mobilisées

* **Power BI** (modélisation, DAX, visualisation)
* **DAX** : mesures personnalisées (marge, ROI promotion, taux de perte)
* **Data cleaning & transformation** (Power Query)
* **Analyse business & recommandations stratégiques**


##  Résultats clés (Insights chiffrés)

###  Performance globale (2020 – 2023)

*  Chiffre d’affaires total : 3,37 M€
*  Croissance des ventes : +20,6 %
*  Marge brute moyenne : 36,91 %
*  Unités vendues : 470 980
*  Taux de pertes global : 9,97 %


###  Produits les plus rentables

*  Brocoli

  * CA : 0,27 M€
  * Marge brute : +33,4 %

*  Lotus Roots

  * CA : 0,21 M€
  * Marge nette : 42,8 %

*  Xivia Mushroom

  * CA : 0,21 M€

📌 **Les 10 produits les plus performants génèrent 65 % de la marge totale**, démontrant une forte concentration de la rentabilité.


###  Analyse des promotions

*   45 % des promotions ne permettent pas d’améliorer la rentabilité, malgré une hausse des volumes
*  Coût total des promotions : 2,1 M€ (2024)
*  60 % des promotions concernent des produits à faible rotation


###  Analyse des pertes

 Taux de pertes global : ≈ 10 % du chiffre d’affaires

 Les pertes sont concentrées sur un nombre limité de produits (logique de Top 10)

 Produits avec les taux de pertes les plus élevés (Top Loss)

Les produits suivants présentent des taux de pertes élevés, parfois supérieurs à 25 % :

High Melon (~29 %)

Dongmenkou (~28 %)

Foreign Garland (~26 %)

Purple Cabbage (~25 %)

Honghu Lotus Root (~24 %)

Kuaicai (~20 %)

Spinach / Amaranth (~19 %)

 Ces produits sont majoritairement des produits frais, sensibles à la péremption et à la sur‑gestion des stocks.

##  Recommandations business

##  Mieux cibler les promotions

  Éviter les promotions sur les produits peu rentables
  
  Privilégier les produits avec une bonne marge

##  Réduire les pertes liées aux stocks

  Ajuster les quantités commandées pour limiter les invendus


##  Former le personnel

 Sensibilisation à la gestion des retours et des pertes

## mesures DAX utilisées

```DAX
Chiffre d’Affaires = 
SUM(Ventes[Montant_Vente])
```

```DAX
Marge Brute (%) = 
DIVIDE([Marge Brute], [Chiffre d’Affaires])
```

```DAX
ROI Promotion = 
DIVIDE([Ventes avec Promotion] - [Coût Promotion], [Coût Promotion])
```

```DAX
Taux de Pertes (%) = 
DIVIDE([Montant des Pertes], [Chiffre d’Affaires])
```

```DAX
Contribution Top Produits (%) = 
DIVIDE([Marge Top Produits], [Marge Totale])
```

📌 *Ces mesures ont permis d’identifier les produits créateurs de valeur, les promotions non rentables et les zones de pertes prioritaires.*
