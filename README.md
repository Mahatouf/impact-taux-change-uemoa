# Impact des fluctuations du taux de change sur le commerce extérieur — Zone UEMOA

## Contexte
Étude économétrique reliant les variations du taux de change (FCFA/USD, FCFA/EUR) à l'évolution de la balance commerciale des pays de la zone UEMOA.

## Objectif
Quantifier la relation entre taux de change et commerce extérieur, et en tirer des implications économiques.

## Données
- Source : BCEAO (statistiques régionales), Banque Mondiale
- Séries : taux de change nominal, exportations, importations, balance commerciale
- Période : séries temporelles annuelles ou trimestrielles, 15-20 ans

## Méthodologie
1. Constitution des séries temporelles (nettoyage, mise en fréquence homogène)
2. Analyse de stationnarité (test ADF)
3. Régression linéaire / modèle à correction d'erreur si séries non stationnaires
4. Test de corrélation et interprétation des coefficients
5. Visualisation des séries et de la relation estimée

## Outils
Python — pandas, statsmodels, matplotlib

## Résultat
- Notebook : `analyse_econometrique.ipynb`
- Rapport de synthèse : `rapport.pdf`
- Conclusion principale : *(à compléter après analyse — ex : une dépréciation du FCFA améliore la balance commerciale avec un décalage de X mois)*

## Comment reproduire
```bash
pip install -r requirements.txt
jupyter notebook analyse_econometrique.ipynb
```

## Auteur
Mahatouf ALASSANI — Data Analyst & Économiste en finances internationales
[mahatoufalassani@gmail.com](mailto:mahatoufalassani@gmail.com) · [LinkedIn](https://www.linkedin.com/in/mahatouf-alassani)

