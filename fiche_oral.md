# 🏩️ Fiche orale - Projet Conversion Rate Prediction

## ✅ 1. CONTEXTE & OBJECTIF
L'entreprise **Data Science Weekly** souhaite mieux comprendre les comportements utilisateurs sur son site web afin d'améliorer son taux d'abonnement à la newsletter.

**Objectif :** construire un modèle de machine learning capable de prédire si un utilisateur va s'abonner à la newsletter, sur la base de données de navigation.

## 🧰 2. STRUCTURE DU PROJET
- **Partie 1 : Modèle de base** (régression logistique univariée)
- **Partie 2 : EDA complète + Feature Engineering** (analyse, nettoyage, transformation)
- **Partie 3 : Modélisation avancée** avec Random Forest optimisée

## 🧰 3. MÉTHODOLOGIE
- Suppression des valeurs aberrantes (`age < 15` ou `> 80`)
- Création de colonnes de segmentation :
  - `group_age` (teen, young_adult, etc.)
  - `page_visit_group` (low, medium, high, very_high)
- Encodage des variables qualitatives + standardisation des quantitatives

## 📊 4. RÉSULTATS

| Modèle                          | F1-score (Train) | F1-score (Test) |
|----------------------------------|------------------|-----------------|
| Logistic Regression (baseline)   | 0.7555           | 0.7419          |
| Random Forest (simple)          | 0.7805           | 0.7545          |
| Random Forest (GridSearchCV)    | 0.78             | **0.76**        |

> Le modèle **Random Forest avec GridSearchCV** obtient le **meilleur F1-score test**.

## 🔍 5. INTERPRÉTATION
- Les utilisateurs visitant plus de pages sont bien plus susceptibles de se convertir.
- L'âge est une variable clé : comportement très différent chez les tranches `teen` et `adult`.
- Les performances des modèles sont équilibrées (pas de surapprentissage).
- Selon les besoins métiers (limiter les faux positifs ou faux négatifs), on pourrait adapter le choix du modèle.

## ✈️ 6. CONCLUSION
- Projet complet : EDA, modélisation, amélioration et optimisation.
- F1-score test final de **0.76**, gage d'un bon compromis précision/recall.
- Feature engineering pertinent pour booster les performances.
- Prêt pour intégration ou test dans un pipeline de scoring utilisateurs.

---
