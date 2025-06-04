# 🎧 Music Genre Clustering & Recommendation System (GTZAN)

Ce projet implémente un système de **clustering non supervisé** et de **recommandation musicale** basé sur le célèbre dataset GTZAN. L’objectif est de grouper automatiquement des morceaux similaires à l’aide de caractéristiques audio, puis de recommander des pistes proches à partir de la similarité entre ces features.

---

## 📌 Objectifs du projet

- Extraire des **features audio** (MFCC, Chroma, Spectral features, etc.)
- Appliquer le **clustering KMeans** pour découvrir des groupes musicaux
- Déterminer la **similarité entre morceaux** via distance Cosinus et Euclidienne
- Fournir un **système de recommandation** à partir de ces similarités
- Évaluer les recommandations avec des **métriques robustes** : précision, rappel, F1, NDCG, diversité
- Visualiser les clusters et la structure des morceaux en 2D (PCA / t-SNE)

---

## 📁 Dataset : GTZAN Genre Collection

- 📦 1 000 extraits audio (`.wav`) de 30 secondes chacun
- 🔟 Genres musicaux : blues, classical, country, disco, hiphop, jazz, metal, pop, reggae, rock
- 📍 Source : [GTZAN sur Kaggle](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification)

---

## 🛠️ Fonctionnalités principales

### 🔊 Extraction de features (avec Librosa)
- Zero Crossing Rate
- Spectral Rolloff
- Spectral Centroid
- Bandwidth
- MFCCs (20 coefficients)
- Chroma features
- Spectral Contrast
- Fundamental frequency (YIN)
- Tempo

### 🤖 Clustering KMeans
- Détermination du nombre optimal de clusters via **silhouette score**
- Visualisation en 2D avec **PCA** ou **t-SNE**

### 🤝 Système de recommandation
- Basé sur **similarité Cosinus** ou **distance Euclidienne**
- Génération de **matrices de similarité**
- Recommandations par genre ou par proximité

### 🧪 Évaluation du système
- **Précision, Rappel, F1-score**
- **NDCG@k** (Normalized Discounted Cumulative Gain)
- **Diversité** : écart Cosinus moyen entre recommandations
- **Matrice de confusion** cluster / genre

---

## 🖼️ Visualisations incluses

- Clusters de morceaux projetés en 2D (PCA ou t-SNE)
- Heatmap des similarités cosinus
- Répartition des genres dans les clusters
- Graphiques d’évaluation (barplots, courbes)

---

## ⚙️ Installation

```bash
git clone https://github.com/votre-utilisateur/music-clustering-reco.git
cd music-clustering-reco
pip install -r requirements.txt
