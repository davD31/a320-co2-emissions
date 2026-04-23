# A320neo vs A320ceo — L'impact réel de la nouvelle génération sur les émissions CO₂

## Problématique

> Dans quelle mesure le passage à l'A320neo réduit-il concrètement les émissions CO₂ ? Sur quelles routes et pour quelles compagnies l'impact serait-il le plus significatif ?

L'A320neo est présenté par Airbus comme une avancée majeure en matière d'efficacité énergétique. Ce projet analyse les données réelles de trafic aérien mondial pour quantifier cette réduction et simuler l'impact d'un remplacement total de la flotte.

## Données

| Source | Description |
|--------|-------------|
| [AeroSCOPE](https://zenodo.org/records/10143773) | Dataset global du trafic aérien : routes, type d'appareil, CO₂, distance, nombre de vols |
| [Our World in Data](https://github.com/owid/co2-data) | Contexte macro : évolution des émissions CO₂ dans l'aviation par pays |

- **36 496 routes** A320 analysées après nettoyage
- **12 variables** : type d'appareil, compagnie, aéroports, distance, CO₂, sièges, nombre de vols…

## Structure du projet

```
a320neo-vs-ceo-co2/
│
├── Data/
│   ├── AeroSCOPE_global_aviation_traffic_dataset.csv
│   ├── owid-co2-data.csv
│   └── a320_clean.csv
│
├── Notebook/
│   ├── 01_import_nettoyage.ipynb
│   ├── 02_analyse_exploratoire.ipynb
│   └── 03_simulation_neo.ipynb
│
└── README.md
```

## Résultats clés

### Analyse exploratoire

- **CO₂ moyen par route** : A320ceo → 1 410 tonnes | A320neo → 963 tonnes
- **Réduction observée** : le neo émet **33.1% de CO₂ en moins** par km que le ceo
- **Part du neo** : seulement **15.7%** de la flotte A320 mondiale — 84.3% est encore en ceo
- **Routes courtes (< 3 000 km)** : concentrent le plus de trafic et d'émissions → plus fort potentiel d'impact
- **Compagnies dominantes** : easyJet, Frontier, Wizz Air — le low-cost est le principal opérateur d'A320

### Simulation d'impact

| Scénario | CO₂ total |
|----------|-----------|
| Flotte actuelle (ceo) | 43.4 Mt |
| Simulation (tout en neo) | 29.0 Mt |
| **CO₂ économisé** | **14.3 Mt** |
| **Réduction** | **33.1%** |

> Si l'ensemble de la flotte A320ceo était remplacée par des A320neo, on estime une économie de **14.3 millions de tonnes de CO₂**.

## Stack technique

- **Python** : Pandas, NumPy, Matplotlib
- **Environnement** : Jupyter Notebook, VS Code
- **Versioning** : Git / GitHub

## Auteur

**David Dinh** — Étudiant L3 MIAGE, Université de Toulouse
- GitHub : [github.com/davD31](https://github.com/davD31)
- Email : daviddinh31@gmail.com
