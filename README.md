
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

## 📂 Organisation du Projet

- `data/` : Contient les images utilisées pour l'entraînement et le test.
- `models/` : Fichiers de sauvegarde des modèles entraînés.
- `notebooks/` : Contient les notebooks Jupyter utilisés pour l'entraînement et l'analyse.
- `scripts/` : Contient les fichiers Python pour le prétraitement et l'entraînement.

---

## ⚙️ Utilisation

1️⃣ **Exécuter l'entraînement des modèles**  
Lancez le script suivant pour entraîner les modèles sur vos données :

```bash
python scripts/train_model.py
```

2️⃣ **Tester une image spécifique**  
Une fois le modèle entraîné, vous pouvez tester une image avec :

```bash
python scripts/predict.py --image chemin/vers/image.png
```

Cela retournera si la cellule est **infectée** ou **saine**.

---

## 📦 Modèles Utilisés

- **CNN from scratch** : Créé spécifiquement pour ce projet, optimisé pour la détection d’infection sur des images 64x64.
- **VGG16** : Réseau pré-entraîné sur ImageNet, adapté à notre tâche avec fine-tuning des dernières couches.
- **ResNet50** : Réseau pré-entraîné sur ImageNet, fine-tuning des 20 dernières couches.

Les meilleurs poids des modèles sont stockés dans le dossier `models/`.

---

## 📊 Évaluation des Performances

Les modèles sont évalués à l'aide de métriques standards comme **accuracy, precision, recall et F1-score**.  
L'évaluation se fait via :

```bash
python scripts/evaluate.py
```

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

## 🛠️ Développements Futurs

- Ajout de **DenseNet** ou **EfficientNet** pour encore améliorer les performances.
- Déploiement sous forme d'API Flask ou FastAPI.
- Optimisation des temps d'inférence.
- Ajout d'un pipeline d'entraînement automatique sur GPU.

---

## 📄 Licence

Ce projet est sous licence **MIT**.

---

## 🤝 Contributions

Les contributions sont les bienvenues !  
Vous pouvez ouvrir une issue ou soumettre une pull request.

---

## 🧑‍💻 Auteur

- **[Votre Nom]**  
- Contact : [Votre Email]

---

## 🔗 Ressources Utiles

- [Documentation TensorFlow](https://www.tensorflow.org/)
- [Jeu de données Kaggle](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria)
