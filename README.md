<div align="center">

# 🏃‍♂️ Estimation de la Condition Physique Liée à la Santé : Analyse Statistique et Régression Linéaire Multiple
  
[![R](https://img.shields.io/badge/Language-R-blue.svg)](https://www.r-project.org/)
[![R Markdown](https://img.shields.io/badge/Document-RMarkdown-brightgreen)](https://rmarkdown.rstudio.com/)
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)](#)

*Un projet académique d'analyse de données physiologiques visant à modéliser la condition physique à partir de variables simples, dans l'optique d'un dépistage de masse rapide et économique.*

</div>

<br/>

## 📖 Sommaire
- [Présentation et Problématique](#-présentation-et-problématique)
- [Objectifs](#-objectifs)
- [Jeux de Données](#-jeux-de-données)
- [Méthodologie d'Analyse](#-méthodologie-danalyse)
- [Modélisation Statistique](#-modélisation-statistique)
- [Structure du Projet](#-structure-du-projet)
- [Outils et Technologies](#-outils-et-technologies)
- [Équipe du Projet](#-équipe-du-projet)

---

## 🎯 Présentation et Problématique

La mesure précise de la condition physique repose traditionnellement sur des tests cliniques lourds nécessitant :
- Un équipement coûteux
- Un temps d’évaluation important
- Du personnel qualifié et des espaces dédiés

Ces contraintes rendent difficile toute évaluation à grande échelle. Ce projet propose une alternative en étudiant et en modélisant statistiquement les relations entre des variables anthropométriques simples à mesurer (âge, sexe, IMC, masse grasse) et des indicateurs réels de performance physique.

---

## 🚀 Objectifs

* **Explorer et décrire** des données physiologiques complexes.
* **Vérifier les conditions statistiques** indispensables (normalité, homogénéité des variances).
* **Comparer les performances physiques** selon le sexe et l’âge (tests d'hypothèses).
* **Construire des modèles prédictifs** (Régression Linéaire Multiple) pour estimer la force de préhension et la capacité cardiorespiratoire (VO₂ max).
* **Interpréter et analyser** les résultats dans un contexte de santé publique.

---

## 📊 Jeux de Données

L'échantillon analysé est composé de **2 000 participants** (âgés de 19 à 64 ans).

### 🔍 Variables Explicatives (Faciles à mesurer)
- `sex` : Sexe
- `age` : Âge
- `bmi` : Indice de masse corporelle (IMC)
- `percent_body_fat` : Pourcentage de masse grasse

### 🎯 Variables Cibles (Performances)
- `hand_grip_strength_kg` : Force de préhension
- `sit_and_reach_cm` : Flexibilité
- `sit_ups_count` : Endurance musculaire
- `vo2_estimate_ml_per_kg_min` : Capacité cardiorespiratoire estimée (VO₂)

---

## 🔬 Méthodologie d'Analyse

Le déroulement du projet est scrupuleusement défini par une démarche scientifique rigoureuse :

1. **Préparation des Données** : 
   - Nettoyage des données et suppression des identifiants non pertinents.
   - Détection et traitement des valeurs aberrantes (*boxplots*).
2. **Analyse Exploratoire & Corrélations** : 
   - Histogrammes, courbes de densité, matrices de corrélation (heatmaps).
3. **Tests d'Hypothèses et Statistique Inférentielle** : 
   - Tests de normalité : **Shapiro-Wilk**, **Kolmogorov-Smirnov**, et rééchantillonnage par **Bootstrap**.
   - Comparaison de Groupes : **Tests T**, Analyse de la variance (**ANOVA**), Homogénéité des variances (**Test de Bartlett**).

---

## 📈 Modélisation Statistique

Deux modèles principaux de **Régression Linéaire Multiple** ont été construits en utilisant la méthode de sélection _stepwise_ selon le critère AIC :

| Modèle Prédit | Variables Explicatives Retenues | Performance Finale | Observation |
| :--- | :--- | :--- | :--- |
| **Force de préhension** | Sexe, Âge, IMC, Masse grasse | **R² ajusté ≈ 61 %** | Fortement et positivement influencée par le fait d'être un homme, l'âge et l'IMC. |
| **VO₂ estimée** | Sexe, Âge, IMC, Masse grasse | **R² ajusté ≈ 31 %** | Diminution significative avec l'âge et la hausse de la masse grasse. |

*Une partie de la variance demeure inexpliquée en raison de facteurs non observés (facteurs génétiques, historiques d'entraînement sportif, etc.).*

---

## 📂 Structure du Projet

```text
📁 Health-Related Physical Fitness Estimation
├── 📄 README.md                        <- Ce fichier (Documentation principale)
├── 📄 README.txt                       <- Version originale au format texte brut
├── 📁 data/
│   └── 📊 DATA.xlsx                    <- Le jeu de données brutes
├── 📁 scripts/
│   └── 💻 Code R.Rmd                   <- Script principal Markdown R
├── 📁 report/
│   └── 📑 Rapport de reformulation.pdf <- Le rapport PDF final généré depuis R
└── 📁 article_scientifique/            <- Dossier pour l'article de référence
```

---

## 🛠 Outils et Technologies

Ce projet a été intégralement développé et documenté avec **R** et généré via **R Markdown** pour l'intégration automatique des équations (LaTeX) et des graphiques.

* **Langage** : R
* **Environnement** : RStudio / R Markdown (Compilateur `xelatex`)
* **Packages clés** : `ggplot2`, `dplyr`, `tidyr`, `corrplot`, `MASS`, `psych`, `openxlsx`

---

## 🤝 Équipe du Projet

Ce projet a été réalisé par des étudiants en ingénierie de l'**ESPRIT (École Supérieure Privée d'Ingénierie et de Technologies)** pour l'année universitaire 2025–2026.

* **Mohamed Ali Jabri**
* **Farah Baklouti**
* **Mohamed Khalil Kamessi**
* **Ines Bendhifallah**
* **Najeh Benrebeh**

👨‍🏫 **Sous la supervision académique de** : M. Youssef Mejri (Statistiques)
