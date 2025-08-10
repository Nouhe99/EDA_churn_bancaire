# 📊 Analyse du churn bancaire — BankChurners

## 🎯 Objectif
Identifier et comprendre les facteurs qui influencent la résiliation des comptes clients dans le secteur bancaire, afin de proposer des actions ciblées de rétention.

## 🗂 Jeu de données
- Source : jeu de données *BankChurners* (institution bancaire fictive)
- Description : informations démographiques, comportementales et transactionnelles de clients.
- Taille : ~10 000 enregistrements, 20+ variables.

## 🛠 Méthodologie
1. **Chargement et exploration initiale**
   - Aperçu du jeu de données, types, statistiques descriptives.
2. **Qualité et nettoyage des données**
   - Gestion des valeurs manquantes et des codes “Unknown”.
   - Suppression des variables présentant un risque de fuite (leakage).
3. **Analyse exploratoire des données (EDA)**
   - **Univariée** : distributions, outliers (IQR).
   - **Bivariée** : corrélations numériques, tests statistiques (Mann–Whitney, Chi²).
   - **Multivariée** : PCA, t‑SNE.
4. **Feature Engineering**
   - Création de variables dérivées (ex. montant moyen par transaction, tranches d’âge).
5. **Modélisation explicable**
   - Régression logistique avec métriques (ROC‑AUC, matrice de confusion).
   - Importance directionnelle des variables.
6. **Segmentation**
   - Clustering KMeans pour repérer des profils distincts.

## 📈 Résultats clés
- **Taux global de churn** : calculé lors de l’exécution.
- Variables transactionnelles (nombre et montant) et inactivité récente fortement liées à l’attrition.
- Influence de certaines tranches de revenus et catégories de carte.

## 📌 Recommandations
- Cibler en priorité les clients inactifs depuis 2–3 mois.
- Proposer des incitations à l’usage pour les profils à faible volume de transactions.
- Déployer des campagnes de rétention segmentées selon le profil.

## 📷 Exemples de visualisations
- Matrice de corrélation
- Violin plots par cible
- PCA et t‑SNE colorés par statut
- Importances de la régression logistique

## 🧰 Stack technique
- **Langage** : Python 3 (>=3.9)
- **Bibliothèques** : pandas, numpy, matplotlib, seaborn, scikit‑learn, scipy
- **Outils** : Jupyter Notebook, GitHub

## 🚀 Utilisation
1. Cloner le dépôt :
   ```bash
   git clone https://github.com/ton-utilisateur/nom-du-repo.git

2. Installer les dépendances :
   ```bash
   pip install -r requirements.txt

3. Lancer le notebook :
   ```bash
   jupyter notebook

4. Ouvrir "EDA_churners_banque.ipynb" et exécuter les cellules dans l’ordre.
