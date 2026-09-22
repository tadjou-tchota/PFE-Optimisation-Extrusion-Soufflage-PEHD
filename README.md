# Optimisation expérimentale des paramètres opératoires d’un procédé d’extrusion-soufflage de flacons en PEHD

## Présentation

Ce dépôt présente les travaux réalisés dans le cadre de mon **Projet de Fin d’Études (PFE)** du **Master 2 Risques Industriels et Maintenance** de l’**Université du Littoral Côte d’Opale (ULCO)**.

L’étude a été réalisée au sein de la **Smart Factory Connected (SFC) de HESTIM**, sur une machine d’**extrusion-soufflage de flacons en polyéthylène haute densité (PEHD)** alimentant deux stations de moulage : **AUTO2 et AUTO3**.

Le travail porte sur le **diagnostic de la variabilité du procédé** et sur l’**optimisation expérimentale de ses paramètres opératoires** à l’aide d’un plan d’expériences.

---

## 🎯 Problématique

L’analyse de l’historique de production a mis en évidence une variabilité importante de la matière extrudée, notamment au niveau de la **masse brute YM des produits finis**.

Sur 147 mesures, la masse brute présente une moyenne de **19,233 g** et un écart-type de **1,600 g**. Le test d’Anderson-Darling donne une p-value de **0,010**, indiquant que la distribution observée n'est pas normale. Les cartes de contrôle mettent également en évidence des causes spéciales de variation.
L'étude de la relation entre la masse brute **YM** et la masse de carotte **YC** montre par ailleurs que les variations de matière extrudée sont fortement associées aux variations de la carotte.

La problématique du projet est ainsi formulée autour de la maîtrise des paramètres opératoires afin de **stabiliser le procédé d'extrusion-soufflage et de mieux maîtriser la formation de la paraison**.

---

## 🎯 Objectifs du projet

Les principaux objectifs sont :

* diagnostiquer le fonctionnement actuel du procédé d'extrusion-soufflage ;
* caractériser et quantifier la variabilité du procédé à partir des données de production ;
* analyser la variabilité de la **masse brute extrudée YM** ;
* étudier la relation entre la masse brute **YM** et la masse de carotte **YC** ;
* identifier les facteurs susceptibles d'expliquer la variabilité du procédé ;
* construire un plan d'expériences permettant d'étudier simultanément plusieurs paramètres ;
* identifier les facteurs ayant une influence significative sur la réponse étudiée ;
* quantifier l'influence des paramètres opératoires sur la **longueur de la paraison** ;
* déterminer une combinaison théorique de réglages permettant d'atteindre une longueur cible de paraison ;
* proposer une **fenêtre de réglage opérationnelle**.

---

# 🔬 Démarche expérimentale

La démarche adoptée peut être résumée comme suit :

```text
Analyse du procédé
        ↓
Collecte et analyse des données historiques
        ↓
Diagnostic de la variabilité
        ↓
Analyse de la masse brute YM
        ↓
Étude de la relation YM / YC
        ↓
Identification des causes potentielles
        ↓
Sélection des facteurs opératoires
        ↓
Plan d'expériences fractionnaire
        ↓
Réalisation des essais
        ↓
Mesure de la longueur de la paraison
        ↓
Analyse statistique sous Minitab
        ↓
Identification des facteurs influents
        ↓
Modélisation
        ↓
Optimisation par fonction de désirabilité
        ↓
Détermination d'une fenêtre de réglage
```

---

# 📊 1. Diagnostic de la variabilité

La première partie de l'étude repose sur l'exploitation de **147 observations issues de la production**.

La grandeur principalement utilisée pour caractériser la variabilité du procédé est la **masse brute extrudée YM**, correspondant à la masse totale du flacon brut avec sa carotte.

L'analyse comprend notamment :

* statistiques descriptives ;
* analyse de la dispersion ;
* carte de contrôle I-MR ;
* test de normalité d'Anderson-Darling ;
* analyse comparative des stations AUTO2 et AUTO3 ;
* étude de corrélation entre la masse brute YM et la masse de carotte YC ;
* régression de la masse de carotte en fonction de la masse brute.

Les résultats montrent une dispersion importante de la masse brute et un procédé qui n'est pas statistiquement maîtrisé dans les conditions initiales étudiées.

---

# 🔎 2. Relation entre masse brute et masse de carotte

Une analyse de corrélation et de régression a été réalisée entre :

* **YM** : masse totale du flacon brut avec carotte ;
* **YC** : masse de la carotte inférieure ;
* **YN** : masse du flacon net ébavuré.

La relation physique utilisée est :

```text
YM = YC + YN
```

L'analyse montre notamment que les variations de la masse brute sont fortement associées aux variations de la masse de carotte. Les modèles de régression donnent des pentes de **0,48 g/g pour AUTO2** et **0,80 g/g pour AUTO3**.

Cette analyse permet de caractériser le transfert de la variabilité de la matière extrudée vers la carotte.

---

# 🧪 3. Plan d'expériences

Afin d'identifier les paramètres opératoires responsables des variations observées, un **plan factoriel fractionnaire de résolution IV** a été mis en œuvre.

### Facteurs étudiés

Six facteurs opératoires ont été retenus :

| Facteur | Description                                                 |
| ------- | ----------------------------------------------------------- |
| P       | Pression de maintien de la paraison                         |
| T1      | Température de la zone 1 du fourreau                        |
| T2      | Température de la zone 2 du fourreau                        |
| T3      | Température de la zone 3 du fourreau                        |
| V       | Vitesse d'extrusion                                         |
| Tc      | Niveau de réglage du temps de chauffe de la tête de filière |

Le plan comprend **16 conditions expérimentales**, avec **cinq mesures successives de la longueur de paraison pour chaque condition**.

---

# 📏 4. Réponse expérimentale : longueur de la paraison

Pour la phase expérimentale, la **grandeur de réponse choisie est la longueur de la paraison**.

Elle constitue la grandeur physique directement étudiée pour évaluer l'effet des paramètres opératoires.

L'objectif d'optimisation est de déterminer les conditions permettant d'atteindre une **longueur cible de 130 mm**.

La logique de l'étude est donc :

```text
Paramètres opératoires X
        ↓
Procédé d'extrusion-soufflage
        ↓
Longueur de la paraison Y
        ↓
Maîtrise de la formation de la paraison
        ↓
Meilleure maîtrise de la distribution de matière
```

---

# 📈 5. Analyse statistique

Les résultats expérimentaux ont été analysés sous **Minitab**.

Les analyses comprennent notamment :

* estimation des effets ;
* diagramme de Pareto ;
* droite de Henry des effets normalisés ;
* analyse de variance ;
* analyse des résidus ;
* analyse des intervalles ;
* modélisation de la réponse ;
* optimisation par fonction de désirabilité.

Les résultats montrent que la **vitesse d'extrusion V** est le facteur le plus influent sur la longueur de la paraison dans le domaine expérimental étudié. Les températures **T1, T2 et T3** présentent également une influence statistiquement significative. En revanche, **P** et **Tc** ne présentent pas d'effet statistiquement significatif dans ce domaine expérimental.

---

# ⚙️ 6. Optimisation

Une optimisation par **fonction de désirabilité** a été réalisée sous Minitab afin de rechercher les conditions permettant d'atteindre une longueur de paraison cible de **130 mm**.

La condition théorique obtenue comprend notamment :

* **V ≈ 13,15 Hz**
* **T1 ≈ 188,0 °C**
* **T2 ≈ 180,5 °C**
* **T3 ≈ 172,5 °C**

Une fenêtre de réglage opérationnelle a ainsi été proposée.

> **Important :** l'essai physique de confirmation n'a pas pu être réalisé en raison de l'indisponibilité de la machine. Les réglages proposés doivent donc encore être validés expérimentalement en conditions réelles.

---

# 🏭 Procédé étudié

Le procédé étudié est une ligne d'extrusion-soufflage de flacons en PEHD comprenant deux stations de moulage :

* **AUTO2**
* **AUTO3**

La machine produit une paraison en PEHD qui est ensuite conformée dans le moule par soufflage.

Le travail s'est concentré sur la maîtrise de la formation de la paraison et sur l'influence des paramètres opératoires de l'extrudeuse.

---

# 📁 Organisation du dépôt

```text
PFE-Optimisation-Extrusion-Soufflage-PEHD/
│
├── README.md
│
├── 01_Rapport/
│   └── Rapport_PFE.pdf
│
├── 02_Presentation/
│   └── Presentation_PFE.pdf
│
├── 03_Donnees/
│   └── Donnees_experimentales.xlsx
│
├── 04_Analyses/
│   ├── Diagnostic_variabilite/
│   ├── Correlation_YM_YC/
│   ├── DOE/
│   ├── Regression/
│   └── Optimisation/
│
├── 05_Resultats/
│   ├── Graphiques/
│   └── Tableaux/
│
└── 06_Illustrations/
```

---

# 🧰 Outils et méthodes

| Domaine                     | Outils / méthodes         |
| --------------------------- | ------------------------- |
| Traitement des données      | Microsoft Excel           |
| Analyse statistique         | Minitab                   |
| Maîtrise statistique        | Carte I-MR                |
| Normalité                   | Anderson-Darling          |
| Analyse de relations        | Corrélation / régression  |
| Analyse expérimentale       | DOE                       |
| Identification des facteurs | Pareto / ANOVA            |
| Modélisation                | Régression                |
| Optimisation                | Fonction de désirabilité  |
| Analyse des causes          | Diagramme d'Ishikawa – 5M |

---

# 📚 Documents

### Rapport de PFE

📄 [Rapport complet](01_Rapport/Rapport_PFE.pdf)

### Présentation de soutenance

🎓 [Présentation](02_Presentation/Presentation_PFE.pdf)

### Données et analyses

📊 [Données expérimentales](03_Donnees/Donnees_experimentales.xlsx)

> La diffusion des données, des photographies et des documents techniques doit respecter les éventuelles contraintes de confidentialité et d'autorisation de HESTIM.

---

# 🎓 Formation

**Master 2 – Risques Industriels et Maintenance**
Université du Littoral Côte d’Opale (ULCO)
2024–2026

**Projet de Fin d’Études – 2026**

**Thème :**
*Optimisation expérimentale des paramètres opératoires d’un procédé d’extrusion-soufflage de flacons en PEHD*

---

# 👤 Auteur

**Tadjou TCHOTA**

Automatisation industrielle · Maintenance · Analyse statistique · Optimisation des procédés industriels

📍 Casablanca, Maroc

---

## 🔗 À propos du projet

Ce dépôt constitue une synthèse technique et scientifique du Projet de Fin d’Études.

Il présente la démarche adoptée depuis le **diagnostic de la variabilité du procédé** jusqu'à la **détermination théorique d'une fenêtre de réglage**, en passant par la caractérisation statistique, le plan d'expériences, l'analyse des facteurs et l'optimisation.
