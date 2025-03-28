# ISD Océanographie 🌊📊

## Description

Ce projet analyse des données océanographiques issues du fichier `bottle.csv`, en utilisant des techniques de **prétraitement des données** et de **modélisation prédictive**. L'objectif est d'explorer les relations entre différentes variables océaniques et de construire des modèles de régression pour les prédictions.

## Technologies utilisées 🛠️

- **Python** : Traitement et modélisation des données
- **Pandas & NumPy** : Manipulation des données
- **Matplotlib** : Visualisation des données
- **Scikit-Learn** : Modèles de régression et évaluation

## Prétraitement des Données 🧹

1. **Chargement des données** :
   ```python
   import pandas as pd
   data = pd.read_csv("bottle.csv")
   ```
2. **Nettoyage** :
   - Suppression des colonnes avec trop de valeurs manquantes
   - Remplacement des valeurs manquantes par `0.0`
   ```python
   data_preprocessed = data.dropna(axis=1, thresh=50000)
   data_preprocessed = data_preprocessed.fillna(0.0)
   ```

## Modélisation 🔍

### 1. Régression Linéaire
```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
```

### 2. K-Nearest Neighbors (KNN)
```python
from sklearn.neighbors import KNeighborsRegressor
knn = KNeighborsRegressor(n_neighbors=5)
knn.fit(X_train, y_train)
```

### 3. Random Forest
```python
from sklearn.ensemble import RandomForestRegressor
rf = RandomForestRegressor(n_estimators=100)
rf.fit(X_train, y_train)
```

## Évaluation 📊

- **Erreur quadratique moyenne (MSE)**
- **Erreur absolue moyenne (MAE)**
- **Coefficient de détermination (R²)**

```python
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score
mse = mean_squared_error(y_test, y_pred)
mae = mean_absolute_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)
```

## Installation 🚀

1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/Ismaelwn/isd_oceanographie.git
   ```

2. **Lancer le notebook** :
   ```bash
   jupyter notebook isd_oceanographie.ipynb
   ```

## Contribution 🤝

Les contributions sont les bienvenues !

1. **Forker le dépôt** 📌
2. **Créer une branche** (`git checkout -b feature/NouvelleAmélioration`)
3. **Committer vos modifications** (`git commit -m "Ajout d'un nouveau modèle"`)
4. **Pousser votre branche** (`git push origin feature/NouvelleAmélioration`)
5. **Ouvrir une Pull Request** 📬



