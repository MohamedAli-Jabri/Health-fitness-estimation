Estimation de la Condition Physique Liée à la Santé
Analyse Statistique et Régression Linéaire Multiple

Présentation du projet
Ce projet consiste en l’analyse et la reformulation d’un article scientifique
portant sur l’estimation de la condition physique liée à la santé à l’aide
de méthodes statistiques et de la régression linéaire multiple.

L’objectif est de proposer une alternative rapide, économique et accessible
aux tests physiques classiques, souvent coûteux et difficiles à généraliser
pour un dépistage de masse.

------------------------------------------------------

Contexte et problématique
La mesure de la condition physique nécessite généralement :
- un équipement coûteux
- un temps d’évaluation important
- du personnel qualifié
- un espace dédié

Ces contraintes rendent difficile une évaluation à grande échelle.
La solution proposée repose sur la modélisation statistique des relations
entre des variables anthropométriques simples et des indicateurs de
performance physique.

------------------------------------------------------

Objectifs du projet
- Explorer et décrire des données physiologiques
- Vérifier les conditions statistiques (normalité, homogénéité)
- Comparer les performances physiques selon le sexe et l’âge
- Construire des modèles prédictifs basés sur la régression linéaire multiple
- Interpréter et analyser les résultats obtenus

------------------------------------------------------

Données utilisées
- Taille de l’échantillon : 2 000 participants
- Tranche d’âge : 19 à 64 ans

Variables explicatives :
- Sexe
- Âge
- Indice de masse corporelle (IMC)
- Pourcentage de masse grasse

Variables cibles :
- Force de préhension (hand grip strength)
- Flexibilité (sit and reach)
- Endurance musculaire (sit-ups)
- Capacité cardiorespiratoire estimée (VO₂)

------------------------------------------------------

Préparation des données
- Suppression des identifiants non pertinents
- Vérification de l’absence de valeurs manquantes
- Détection et traitement des valeurs aberrantes
- Analyse exploratoire des distributions
- Étude des corrélations entre variables

------------------------------------------------------

Analyse statistique
- Tests de normalité (Shapiro-Wilk, Kolmogorov-Smirnov)
- Utilisation du bootstrap pour valider les moyennes
- Tests de corrélation
- Tests t pour la comparaison selon le sexe
- Tests ANOVA pour la comparaison selon l’âge
- Vérification de l’homogénéité des variances (test de Bartlett)
- Tests de proportion

------------------------------------------------------

Modélisation statistique
Deux modèles de régression linéaire multiple ont été développés :

1. Modèle de la force de préhension
- Variables explicatives : sexe, âge, IMC, pourcentage de masse grasse
- Sélection des variables par méthode stepwise (critère AIC)
- Nettoyage des valeurs aberrantes par analyse des résidus
- R² ajusté ≈ 61 % de variance expliquée

2. Modèle de la VO₂ estimée
- Variables explicatives : sexe, âge, IMC, pourcentage de masse grasse
- Même démarche de sélection et de nettoyage
- R² ≈ 31 % de variance expliquée

------------------------------------------------------

Résultats principaux
- La force de préhension est positivement influencée par le sexe masculin,
  l’âge et l’IMC
- La capacité cardiorespiratoire diminue avec l’âge et l’augmentation
  du pourcentage de masse grasse
- Les différences de performances selon le sexe et l’âge sont statistiquement
  significatives
- Une part de la variance reste inexpliquée, liée à des facteurs non observés
  tels que l’entraînement et la génétique


------------------------------------------------------

Technologies et outils
- R
- R Markdown
- Analyse statistique
- Régression linéaire multiple

------------------------------------------------------

Conclusion
Ce projet met en évidence l’importance des méthodes statistiques et de la
modélisation prédictive pour l’analyse de données de santé. Il démontre
qu’il est possible d’estimer certains indicateurs de condition physique
à partir de variables simples, offrant ainsi une solution pertinente
pour le dépistage et l’aide à la décision en santé publique.
