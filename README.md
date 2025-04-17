# 🔍 Projet – Conversion Rate Prediction

Ce projet vise à prédire si un utilisateur s'abonnera à une newsletter à partir de ses caractéristiques et de son comportement de navigation.

## 🎯 Objectif

Améliorer le **taux de conversion** de la newsletter "Data Science Weekly" en prédisant les utilisateurs susceptibles de s’abonner.

---

## 🧱 Structure du projet

- **Modèle de base :** Régression logistique simple sur une seule variable (`total_pages_visited`)
- **Modèles avancés :**
  - Random Forest sans feature engineering
  - Random Forest avec GridSearch (optimisation des hyperparamètres)
- **Bonus :**
  - Analyse exploratoire avancée (distribution, outliers…)
  - Feature engineering : création de groupes d’âges et d’intérêt
  - Re-tests avec nouveaux modèles enrichis

---

## 📊 Méthodologie

- **Données utilisées :**
  - `conversion_data_train.csv` : pour entraînement et validation
  - `conversion_data_test.csv` : pour test final

- **Prétraitement :**
  - StandardScaler pour les variables numériques
  - OneHotEncoder pour les variables catégorielles
  - Suppression des valeurs extrêmes (`age < 15` ou `age > 80`)

- **Feature Engineering :**
  - `group_age` : catégorisation des âges
  - `page_visit_group` : catégorisation du nombre de pages visitées

---

## 🧪 Évaluation des modèles

| Modèle                                       | F1-score (Train) | F1-score (Test) |
|---------------------------------------------|------------------|-----------------|
| Régression logistique (1 variable)          | ~0.69            | ~0.69           |
| Random Forest (sans feature eng.)           | ~0.76            | ~0.74           |
| Random Forest (GridSearch sans f.e.)        | ~0.78            | ~0.75           |
| Random Forest (features enrichies)          | ~0.76            | ~0.74           |
| Random Forest (features enrichies + opti)   | ~0.78            | ~0.74           |

🔎 **Interprétation :**
- Le nombre de pages visitées est le facteur le plus influent.
- Le Feature Engineering permet d’améliorer la stabilité du modèle (moins de faux positifs/négatifs selon les groupes).
- Le modèle **GridSearch avec Feature Engineering** est conservé comme meilleur compromis.

---

## 📈 Visualisations

- Histogrammes et boxplots des variables
- Matrices de confusion pour chaque modèle
- Comparaison avant/après feature engineering

---

## ✅ Conclusion

Le modèle final présente une **bonne généralisation** et permet d’identifier les utilisateurs susceptibles de convertir.  
Le projet respecte la méthodologie complète : EDA → Feature Engineering → Modélisation → Évaluation.

---

## 🚀 Prochaines étapes

- Déploiement possible sous forme d’API de scoring
- Intégration dans un dashboard de marketing
- Analyse approfondie des faux négatifs (utilisateurs perdus)

