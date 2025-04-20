# Conversion Rate Prediction Project (Bloc 3 - Machine Learning)

## 🧠 Objectif

L’objectif de ce projet est de prédire si un utilisateur va s’abonner à une newsletter, à partir de ses données de navigation. Il s'agit donc d'un **problème de classification binaire**.

Ce projet fait partie du bloc 3 de la certification CDSD, dédié à l’apprentissage automatique supervisé.

## 📂 Données

Les données sont issues d’un défi de machine learning simulant une compétition Kaggle.

- `data_train.csv` contient les variables explicatives (X) et la variable cible (Y)
- `data_test.csv` contient les données sans la cible (pour prédiction)
- Les colonnes incluent des indicateurs de comportement sur un site web (durée de visite, nombre de pages vues, etc.)

## ⚙️ Méthodologie

### 1. 🔍 EDA
- Analyse des distributions et corrélations
- Détection des valeurs aberrantes
- Traitement des valeurs manquantes

### 2. 🛠️ Prétraitement
- Encodage des variables catégorielles
- Normalisation
- Séparation train/test

### 3. 🧪 Modélisation
- Modèle de base : Logistic Regression (baseline)
- Modèle principal : RandomForestClassifier
- Optimisation des hyperparamètres avec GridSearchCV

### 4. 📈 Évaluation
- **Métrique principale : F1-score**
- Affichage de la matrice de confusion
- Comparaison entraînement vs test

## 🧠 Résultats et conclusion

Le modèle RandomForest optimisé atteint un F1-score de **0.758** sur les données de test. Il surpasse largement la baseline.

Certaines variables (durée de session, type d'appareil, fréquence de visite) ont un impact fort sur la prédiction.

## 📢 Recommandations business proposées

- 💡 Cibler les utilisateurs ayant des **sessions longues** et plusieurs visites : leur probabilité de conversion est plus élevée.
- 📱 Optimiser les campagnes sur **mobile** si ce type d'appareil est corrélé positivement avec les conversions.
- 🔁 Mettre en place des relances automatisées pour les visiteurs **fréquents mais non convertis**.
- 🚫 Réduire les efforts marketing sur les utilisateurs avec **peu d'interactions** ou des visites très courtes.

Ces recommandations permettent d’optimiser les efforts marketing et d’améliorer le taux de conversion global.

## 📄 Fichiers livrés

- `Conversion_rate_final_notebook.ipynb` : Notebook complet
- `README.md` : Présentation du projet
- `requirements.txt` : Librairies utilisées

## 🔗 GitHub

👉 https://github.com/charlesdab/conversion_rate_project
