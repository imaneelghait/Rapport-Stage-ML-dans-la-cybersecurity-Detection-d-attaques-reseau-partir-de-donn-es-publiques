# Rapport de Stage en ML dans la cybersécurité : Détection d'attaques réseau à partir des données publiques
**Groupe MANAGEM — Imane EL GHAIT**

Ce dépôt contient le rapport complet et le code associé à mon stage de fin d’année portant sur la **détection d’intrusions réseau** à l’aide du Machine Learning, en utilisant le dataset **NSL-KDD**.  
Le projet inclut : l’analyse du dataset, son prétraitement, l’entraînement de modèles ML, l’évaluation des performances et le déploiement d’une application **Streamlit** permettant de tester le modèle final.

---

##  1. Résumé du projet

L’objectif principal du stage est de développer un modèle capable de distinguer le trafic **normal** du trafic **malveillant** à l’aide d’approches Machine Learning, en s’appuyant sur un dataset public utilisé dans la recherche en cybersécurité : **NSL-KDD**.

Le travail effectué couvre l’ensemble du pipeline Machine Learning :

- Exploration du dataset NSL-KDD  
- Prétraitement et préparation des features  
- Entraînement de plusieurs modèles (Random Forest, SVM, Logistic Regression)  
- Évaluation via accuracy, precision, recall, F1-score, matrice de confusion et ROC  
- Sauvegarde du modèle via `joblib`  
- Création d’une application **Streamlit (App.py)** pour tester le modèle avec de nouvelles entrées

Les résultats montrent que le **Random Forest** surpasse les autres modèles évalués.

---

##  2. Objectifs du stage

- Concevoir un système de détection d’attaques basé sur le Machine Learning  
- Explorer et analyser les caractéristiques du dataset NSL-KDD  
- Comparer l’efficacité des modèles ML classiques pour la classification des attaques  
- Construire une interface utilisateur simple (Streamlit) pour tester le modèle  
- Documenter chaque étape de manière claire et reproductible

---

---

##  4. Présentation du dataset NSL-KDD

Le dataset NSL-KDD est une version améliorée du KDD 99, couramment utilisé pour les systèmes de détection d’intrusions (IDS).  
Il contient :

- 41 features  
- 5 catégories d’attaques : DoS, Probe, U2R, R2L, Normal  
- Données d’entraînement : `KDDTrain+`  
- Données de test : `KDDTest+`

Les attaques sont regroupées en deux classes dans ce projet :  
**0 = normal**, **1 = attaque**

---

## ⚙️ 5. Pipeline Machine Learning

###  a) Prétraitement
- Encodage One-Hot des colonnes catégorielles  
- Normalisation via MinMaxScaler  
- Transformation du dataset en matrice numérique exploitable  
- Séparation train/test  

###  b) Entraînement des modèles
Les modèles entraînés incluent :
- Random Forest  
- SVM (kernel linéaire)  
- Régression Logistique

Chaque modèle a été évalué selon :

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **Matrice de confusion**
- **Courbe ROC/AUC**


## 📂 3. Organisation du dépôt

