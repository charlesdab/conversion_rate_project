# 🧠 Conversion Rate Prediction – Machine Learning Project

## 📌 Objectif
L’entreprise **Data Science Weekly** souhaite prédire si un utilisateur va s’abonner à sa newsletter, à partir de données issues de son trafic web.  
Nous avons construit un pipeline complet de classification pour maximiser le **score F1**, la métrique utilisée pour ce défi.

---

## 📁 Données
- `conversion_data_train.csv` : données étiquetées (train/test interne)
- `conversion_data_test.csv` : données sans étiquette (soumission finale)

Variables disponibles :
- `country`, `age`, `new_user`, `source`, `total_pages_visited`, `converted`

---

## 🧰 Étapes du projet

### 1. Modèle de base
- Régression logistique **univariée** (`total_pages_visited`)
- Score F1 ≈ **0.70**  
- Sert de baseline pour la suite du projet

### 2. Analyse exploratoire (EDA)
- Distributions de `age`, `total_pages_visited`
- Visualisation des corrélations et valeurs extrêmes

### 3. Feature Engineering
- Suppression des outliers (`age < 15` ou `age > 80`)
- Création de `group_age` (5 groupes d’âge)
- Création de `page_visit_group` (intérêt faible à élevé)

### 4. Modèles testés
- Régression logistique multivariée
- Random Forest Classifier
- Random Forest + GridSearchCV (modèle final)

---

## 📈 Résultats finaux

| Modèle                        | F1-score (Train) | F1-score (Test) |
|------------------------------|------------------|-----------------|
| Régression logistique (base) | 0.69             | 0.70            |
| Random Forest (simple)       | 0.7555           | 0.7419          |
| Random Forest (GridSearch)   | 0.7555           | **0.7419**      |

✅ **Modèle final retenu** : RandomForestClassifier optimisé via GridSearchCV  
✅ Bon compromis biais/variance, sans surapprentissage visible

---

## 📊 Visualisations
- Distributions des variables numériques
- Matrice de confusion
- Comparaison avant/après Feature Engineering

---

## 🚀 Conclusion
- Modèle robuste avec score F1 ≈ 0.74
- Feature engineering pertinent (groupes d’âge, pages visitées)
- Pipeline complet, reproductible, prêt à être déployé ✅

---

## 📦 Installation

```bash
pip install -r requirements.txt
