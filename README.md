# Impact des fluctuations du taux de change sur le commerce extérieur — Zone UEMOA

**[Voir le dashboard en direct →](https://mahatouf.github.io/impact-taux-change-uemoa/)**

## Contexte
Étude économétrique reliant les variations du taux de change (FCFA/USD) à l'évolution de la balance commerciale des 8 pays de la zone UEMOA.

## Objectif
Quantifier rigoureusement la relation entre taux de change et commerce extérieur, et en tirer des implications économiques honnêtes — y compris quand le résultat ne confirme pas l'hypothèse de départ.

## Données
- Source : Banque Mondiale (API World Bank Open Data)
- Indicateurs : `NE.EXP.GNFS.CD` (exportations), `NE.IMP.GNFS.CD` (importations), `PA.NUS.FCRF` (taux de change)
- Zone : 8 pays UEMOA (Bénin, Burkina Faso, Côte d'Ivoire, Guinée-Bissau, Mali, Niger, Sénégal, Togo), données agrégées
- Période : 2000–2023 (24 années)

## Méthodologie
1. Extraction des séries via l'API World Bank, agrégation au niveau zone (somme exports/imports, moyenne du taux de change)
2. Calcul de la balance commerciale et de son ratio aux exportations
3. Tests de stationnarité (ADF — Augmented Dickey-Fuller) sur les séries en niveau et en différence
4. Régression OLS : effet de la variation (%) du taux de change sur la variation (%) de la balance commerciale l'année suivante (effet retardé)
5. Interprétation économique des résultats, y compris leurs limites

## Résultats clés
- La zone UEMOA affiche un **déficit commercial structurel** sur toute la période, atteignant **-18,7 milliards $** en 2023
- Le taux de change en niveau n'est **pas stationnaire** (p = 0,23), mais le devient après différenciation (p = 0,015) — comportement typique d'une marche aléatoire
- La régression ne détecte **aucun effet statistiquement significatif** du taux de change sur la balance commerciale l'année suivante (**p = 0,45**, R² = 0,03)
- Corrélation contemporanée faible (**0,17**)

## Interprétation
Ce résultat, bien que non significatif, est économiquement cohérent : le FCFA étant arrimé à l'euro à taux fixe, ses variations face au dollar reflètent les fluctuations EUR/USD — elles ne résultent pas d'une politique de change délibérée visant à améliorer la compétitivité des exportations. Le mécanisme classique de dévaluation compétitive ne s'applique donc pas directement dans ce contexte d'arrimage monétaire. Le déficit commercial structurel de la zone s'explique plus probablement par des facteurs structurels (dépendance aux importations de biens manufacturés, prix des matières premières exportées) que par le taux de change lui-même.

## Limites
- Corrélation ne signifie pas causalité
- D'autres variables macroéconomiques non contrôlées (prix des matières premières, croissance mondiale, politiques commerciales) influencent probablement la balance commerciale
- L'agrégation au niveau zone masque des dynamiques nationales potentiellement différentes

## Outils
Python — pandas, statsmodels ; dashboard HTML/JavaScript (Chart.js)

## Comment reproduire
1. Cloner ce repo
2. Ouvrir `index.html` dans un navigateur — aucune dépendance à installer

## Auteur
Mahatouf ALASSANI — Data Analyst & Économiste en finances internationales
[mahatoufalassani@gmail.com](mailto:mahatoufalassani@gmail.com) · [LinkedIn](https://www.linkedin.com/in/mahatouf-alassani) · [Portfolio](https://mahatouf.github.io/portfolio/)

