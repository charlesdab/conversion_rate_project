# 🎤 Fiche orale – Projet Conversion Rate Prediction

## ✅ CONTEXTE

L’objectif est de prédire le taux de conversion d’une newsletter ("Data Science Weekly") à partir des données utilisateur (âge, pays, canal d’arrivée, comportement).

---

## 📊 STRUCTURE DU PROJET

- Modèle de base : régression logistique simple
- Modèles avancés : Random Forest, avec ou sans optimisation
- Feature Engineering : groupes d’âge + pages visitées
- Comparaison avant/après FE

---

## 🔬 MÉTHODOLOGIE

- Préprocessing :
  - Standardisation des variables numériques
  - Encodage des variables catégorielles
  - Suppression des valeurs aberrantes
- Évaluation :
  - F1-score train + test
  - Matrice de confusion

---

## 🧪 SCORES & MODÈLES

| Modèle                                       | F1-score (Train) | F1-score (Test) |
|---------------------------------------------|------------------|-----------------|
| Régression logistique (baseline)            | ~0.69            | ~0.69           |
| Random Forest (sans FE)                     | ~0.76            | ~0.74           |
| Random Forest (GridSearch sans FE)          | ~0.78            | ~0.75           |
| Random Forest (avec FE)                     | ~0.76            | ~0.74           |
| Random Forest (FE + GridSearch)             | ~0.78            | ~0.74           |

---

## 📌 ANALYSE QUALITATIVE

- Meilleur modèle : RF optimisé avec FE → bon équilibre entre précision et généralisation
- Matrices de confusion analysées : selon les cas, on peut préférer limiter les faux négatifs (ne pas rater des abonnés) ou les faux positifs (éviter les erreurs marketing)
- FE utile mais surtout pour segments spécifiques

---

## ✅ CONCLUSION

Projet complet et structuré, avec :
- Baseline claire
- Feature engineering pertinent
- Modèles comparés proprement
- Bonne interprétation des résultats

