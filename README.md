
# 🦠 Détection Automatisée de la Malaria

Ce projet utilise l'intelligence artificielle et des **réseaux de neurones convolutionnels (CNN)** pour détecter la malaria sur des images microscopiques de cellules sanguines. Il repose sur l'entraînement de trois modèles :

- **CNN from scratch** (conçu spécifiquement pour ce projet)
- **VGG16** (pré-entraîné sur ImageNet, avec fine-tuning)
- **ResNet50** (pré-entraîné sur ImageNet, avec fine-tuning)

L'objectif est d'assister les professionnels de santé en automatisant le diagnostic de la malaria à partir d'images microscopiques.

---

## 🚀 Installation

Assurez-vous d'avoir installé les bibliothèques nécessaires :

```bash
pip install tensorflow opencv-python matplotlib scikit-learn pillow numpy pandas
```

---


## 📦 Modèles Utilisés

- **CNN from scratch** : Créé spécifiquement pour ce projet, optimisé pour la détection d’infection sur des images 64x64.
- **VGG16** : Réseau pré-entraîné sur ImageNet, adapté à notre tâche avec fine-tuning des dernières couches.
- **ResNet50** : Réseau pré-entraîné sur ImageNet, fine-tuning des 20 dernières couches.

Les meilleurs poids des modèles sont stockés dans le dossier `models/`.

---


## 📷 Jeu de Données

Le jeu de données utilisé est **Cell Images for Malaria Detection**, disponible sur Kaggle :  
🔗 https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria

Il contient :
- **Parasitized** : Cellules infectées par la malaria.
- **Uninfected** : Cellules saines.

---

## 🧠 Comprendre le CNN From Scratch

Le modèle **CNN personnalisé** suit une architecture classique :

1. **Convolution** : Extraction de caractéristiques via des filtres.
2. **MaxPooling** : Réduction de la taille tout en gardant les informations importantes.
3. **Batch Normalization** : Stabilisation et accélération de l’apprentissage.
4. **Flatten** : Mise à plat des features extraits.
5. **Dense Layers** : Couches entièrement connectées pour la classification.
6. **Dropout** : Prévention du surapprentissage.
7. **Sigmoid** : Activation pour une sortie binaire (infecté ou sain).

---


---

## 🔗 Ressources Utiles

- [Documentation TensorFlow](https://www.tensorflow.org/)
- [Jeu de données Kaggle](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria)
