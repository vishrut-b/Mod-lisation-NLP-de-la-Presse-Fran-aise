# Analyse Thématique Non Supervisée de la Presse Française

## Description

Ce projet met en œuvre un pipeline complet de traitement automatique du langage naturel (NLP) pour analyser et modéliser les thèmes présents dans plus de 500 articles de presse en français.

Le flux inclut la collecte automatique des articles via l’API NewsAPI, un nettoyage et une lemmatisation précis avec spaCy, la génération d’embeddings sémantiques par CamemBERT, la réduction dimensionnelle avec UMAP, et la modélisation de sujets avec BERTopic.

Une évaluation quantitative par cohérence sémantique garantit la qualité et la pertinence des thèmes extraits.

---

## Fonctionnalités principales

* Collecte d’articles français via NewsAPI
* Nettoyage linguistique adapté au français (lemmatisation, stopwords, normalisation Unicode)
* Encodage des textes avec CamemBERT
* Réduction dimensionnelle UMAP pour visualisation et clustering
* Clustering thématique avec BERTopic (basé sur HDBSCAN)
* Évaluation de la cohérence des topics par mesures vectorielles
* Export de visualisations interactives pour exploration des résultats

---

## Installation

### Prérequis

* Python 3.8+
* [pip](https://pip.pypa.io/en/stable/installation/)

### Installation des dépendances

```bash
pip install -r requirements.txt
```

Le fichier `requirements.txt` inclut :
`spacy`, `transformers`, `sentence-transformers`, `bertopic`, `umap-learn`, `hdbscan`, `nltk`, `pandas`, `numpy`, etc.

---

## Usage

### Collecte des articles

```bash
jupyter notebook collect_articles.ipynb
```

Cette étape télécharge et enrichit les articles français via NewsAPI.

### Prétraitement et modélisation

```bash
jupyter notebook preprocessing.ipynb
```

Effectue le nettoyage, lemmatisation, calcul d’embeddings, clustering thématique et évaluation.

### Visualisation

Les notebooks génèrent des fichiers HTML interactifs pour explorer les topics, la répartition des documents, et les relations thématiques.

---

## Structure du projet

```
collect_articles.ipynb          # Notebook de collecte via NewsAPI
preprocessing.ipynb             # Notebook de nettoyage, modélisation et évaluation
french_news_articles.json        # Articles bruts (JSON)
enriched_french_news_articles.json  # Articles enrichis/nettoyés
topic_barchart.html             # Histogramme interactif des mots-clés
topic_heatmap.html              # Heatmap des similarités thématiques
topic_documents.html            # Nuage 2-D interactif des documents
topic_summary.csv               # Tableau récapitulatif (topics, mots-clés, exemples)

```

---

## Contribuer

Contributions, suggestions et rapports de bugs sont les bienvenus. N’hésitez pas à ouvrir une issue ou une pull request.

---

## Auteur

Vishrut Bezbarua – passionné par le NLP et la science des données appliquée au traitement du langage naturel.
