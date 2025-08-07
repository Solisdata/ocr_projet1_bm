# OCR - Projet 2 
## Analyse data-driven des opportunités d’extension de l’activité d’une école en ligne  

Projet réalisé dans le cadre de la formation **Data Engineer** d’OpenClassrooms.

---

## Contexte du projet (situation fictive)

Une start-up de la EdTech nommée *Academy* propose des contenus de formation en ligne à destination d’un public de niveau lycée et universitaire.

Forte de son succès sur le marché de l’éducation en ligne en France, Academy ambitionne désormais de s’étendre à l’international en se développant dans d’autres pays.

Dans le cadre de ce projet d’expansion, notre manager nous a confié une première mission d’analyse exploratoire. L’objectif est de déterminer si les données sur l’éducation fournies par la Banque mondiale peuvent guider les décisions stratégiques de l’entreprise.

Academy souhaite identifier les pays les plus prometteurs pour la formation en ligne, en se basant notamment sur :
- la taille de la population ;
- les besoins en compétences numériques.

En tant que Data Scientist, notre mission est donc d’identifier les pays les plus adaptés à un développement commercial, et d’évaluer dans quelle mesure les données disponibles peuvent alimenter cette réflexion.

L’objectif de cette pré-analyse est de produire des résultats clairs et utiles afin d’orienter le Board dans le choix des pays à cibler.

---

## Problématiques

- Quels sont les pays prioritaires pour l’expansion de l’entreprise ?
- Comment exploiter les données de la Banque mondiale pour guider cette expansion ?
- Sur quels critères s’appuyer pour identifier les meilleures opportunités ?


---

## Travail réalisé

1. **Chargement et exploration des jeux de données**  

2. **Nettoyage des données**  
   - Suppression des doublons  
   - Traitement des valeurs manquantes  

3. **Sélection des indicateurs pertinents**  
   - Identification des indicateurs les plus représentatifs du potentiel de développement (ex. taux de scolarisation, population jeune, accès au numérique)

4. **Normalisation des données et création d’un score composite pondéré par pays**  
   - Mise à l’échelle des indicateurs  
   - Pondération selon leur importance stratégique  
   - Agrégation pour obtenir un score global par pays

5. **Visualisations**  
   - Représentations graphiques des distributions et des tendances (histogrammes, boxplots, etc.)  
   - Visualisation géographique du score par pays via une carte interactive

6. **Interprétation des résultats**  


---

## Données sources

Les données utilisées proviennent de la base publique de la **Banque mondiale** et portent sur les indicateurs liés à l’éducation.

Elles sont structurées en 5 tables principales :

- `country_serie_df` : Informations sur les indicateurs disponibles par pays / indicateur — 613 lignes × 4 colonnes
- `data_df` : Données annuelles par couple pays / indicateur (de 1970 à 2100), incluant des projections — 418 208 lignes × 68 colonnes
- `country_df` : Informations générales sur les pays — 241 lignes × 32 colonnes
- `serie_df` : Métadonnées des indicateurs (définitions, sources, unités, etc.) — 3 665 lignes × 21 colonnes
- `footnote` : Notes méthodologiques et commentaires par année / pays / indicateur — 643 638 lignes × 5 colonnes

---

## Outils et librairies

**Environnement** : Jupyter Notebook  
**Langage** : Python  
**Librairies utilisées** :  
- `pandas`  
- `numpy`  
- `missingno`  
- `matplotlib`  
- `seaborn`  
- `plotly.express`
