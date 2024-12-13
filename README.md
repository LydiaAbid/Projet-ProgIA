# Projet : Analyse des Sentiments avec un Modèle LSTM

## Introduction
Ce projet porte sur l'analyse des sentiments à partir de critiques de films en utilisant un modèle basé sur un réseau de neurones récurrent (RNN) avec des couches LSTM. L'objectif est de prédire si une critique est positive ou négative.

## Dataset
Le dataset utilisé provient de l'ensemble de données **IMDB**, qui contient :
- **50 000 critiques de films** annotées comme positives ou négatives.
- Données équilibrées : 25 000 critiques positives et 25 000 négatives.
- Les critiques varient en longueur, ce qui rend le prétraitement important.

## Méthodologie
1. **Prétraitement des données :**
   - Nettoyage du texte (suppression des balises HTML et ponctuation).
   - Tokenisation et vectorisation des critiques.
   - Troncature et padding pour uniformiser la longueur des séquences.
2. **Modèle utilisé :**
   - Une couche d'Embedding pour représenter les mots en vecteurs.
   - Une couche LSTM pour capturer les dépendances dans les séquences textuelles.
   - Une couche Dense avec activation sigmoïde pour prédire le sentiment.
3. **Entraînement :**
   - Fonction de perte : Binary Crossentropy.
   - Optimiseur : Adam.
   - Régularisation : Dropout pour limiter le surapprentissage.

## Résultats
- **Précision** : 85%
- **Rappel** : 84%
- **F1-Score** : 84.5%
- **AUC** : 0.91

## Points à Améliorer
- Optimisation des hyperparamètres pour améliorer les performances.
- Enrichissement du dataset avec des embeddings préentraînés (ex : GloVe, Word2Vec).
- Comparaison avec d'autres modèles comme SVM ou Random Forest.

## Conclusion
Le projet met en évidence l'efficacité des LSTM pour l'analyse de sentiments dans des données textuelles. Bien que les performances soient prometteuses, des améliorations supplémentaires pourraient être apportées pour affiner les résultats.
