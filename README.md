Challenge Kaggle : "Natural Language Processing with Disaster Tweets"

Ce projet a été développé dans le cadre de la compétition Kaggle "Getting Started". Il s'agit d'une introduction au traitement automatique du langage naturel (NLP).

🎯 Objectif du projet

L'objectif est de construire un modèle de classification binaire capable de distinguer les tweets qui mentionnent un désastre réel de ceux qui ne le font pas, en utilisant un jeu de données d'environ 10 000 tweets annotés.

La performance du modèle est évaluée à l'aide du F1-score, une métrique qui équilibre la précision (precision) et le rappel (recall).

💻 Solution technique

La solution est implémentée dans un notebook Jupyter (NLP_disaster_tweets.ipynb) et suit un pipeline de NLP standard :

    Exploration des données (EDA) : Analyse initiale du jeu de données pour comprendre la distribution des tweets, des mots-clés et des localisations.

    Prétraitement du texte :

        Nettoyage des tweets (suppression des URL, des mentions @, de la ponctuation, etc.).

        Tokenisation et lemmatisation pour standardiser les mots.

        Gestion des stop words.

    Vectorisation des données : Transformation du texte en vecteurs numériques, en utilisant des techniques comme le TF-IDF (Term Frequency-Inverse Document Frequency) ou des embeddings de mots comme GloVe.

    Modélisation : Entraînement de plusieurs modèles de classification. Les modèles suivants ont été explorés :

        Classificateurs de base : Naive Bayes et Logistic Regression.

        Modèles de boosting : XGBoost.

        Réseaux de neurones : Modèles de type RNN, LSTM ou Transformers (tels que BERT) pour capturer les séquences et le contexte.

    Optimisation et évaluation : Réglage des hyperparamètres et validation des performances à l'aide du F1-score sur un jeu de données de validation.

🚀 Guide d'utilisation

    Clone le dépôt.

    Installe les dépendances requises :
    Bash

    pip install pandas numpy scikit-learn nltk xgboost

    Si tu utilises des modèles de deep learning, il faudra aussi installer tensorflow ou pytorch.

    Télécharge les jeux de données train.csv et test.csv depuis la page de la compétition Kaggle et place-les dans le même répertoire que le notebook.

    Exécute le notebook (NLP_disaster_tweets.ipynb) pas à pas pour reproduire l'analyse et les prédictions.

📁 Structure des fichiers

    NLP_disaster_tweets.ipynb : Le notebook Jupyter contenant le code de la solution.

    train.csv : Le jeu de données d'entraînement.

    test.csv : Le jeu de données de test.

    sample_submission.csv : Un exemple de fichier de soumission.

    submission.csv : Le fichier de soumission généré par le modèle.

    README.md : Ce fichier de documentation.
