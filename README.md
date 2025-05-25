# 🏦 Prédiction d’Octroi de Crédit Bancaire

Ce projet a été réalisé dans le cadre d’un travail pratique de machine learning, ayant pour objectif de prédire si un client est éligible à un crédit bancaire à partir de ses informations personnelles et financières.

## 👥 Réalisé par

- Nechat Nouhayla  
- Fatimazahra Borzal  
- Fatimazahra Fedol

## 🎯 Problématique

Permettre à une institution bancaire de mieux décider l’octroi d’un crédit en s’appuyant sur un modèle de machine learning, au lieu de critères purement manuels ou subjectifs.

## 🗃️ Données

- Fichier : `credit_data.csv`
- 613 observations et 12 variables
- Variables : Genre, Situation matrimoniale, Revenu, Montant du prêt, Historique de crédit, etc.
- Variable cible : `Loan_Status` (Y/N) indiquant si le prêt est accepté.

## ⚙️ Prétraitement

- Remplissage des valeurs manquantes :
  - Catégorielles → modalité la plus fréquente
  - Numériques → méthode du backfill
- Transformation de la variable cible (`Loan_Status`) en binaire : Y → 1, N → 0
- Encodage des variables catégorielles (Label Encoding)
- Suppression de la colonne `Loan_ID`
- Fusion des données numériques et catégorielles

## 📊 Analyse Exploratoire

- Étude de la distribution de la variable cible (déséquilibre modéré)
- Identification de variables influentes comme `Credit_History`
- Visualisations par genre, revenu, historique de crédit, etc.

## 🧠 Modélisation

Modèles testés :
- Régression Logistique
- K-Nearest Neighbors (KNN)
- Arbre de Décision

Approche :
- Division en ensembles d’entraînement/test (80/20) via StratifiedShuffleSplit
- Évaluation des performances avec des métriques de précision
- Sélection de variables importantes : `Credit_History`, `Married`, `CoapplicantIncome`

## 💾 Déploiement

Le meilleur modèle (Régression Logistique) a été sauvegardé avec `joblib` pour une intégration possible dans une application.

## ✅ Conclusion

Ce projet illustre comment le machine learning peut améliorer les décisions d’octroi de crédit en automatisant l’analyse des profils clients. Un prétraitement rigoureux et un choix judicieux de variables ont permis d’obtenir un modèle performant, prêt à être utilisé dans un contexte réel.

---
