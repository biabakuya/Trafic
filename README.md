# Trafic

Ce projet vise à prédire le volume de trafic routier en utilisant des techniques avancées de deep learning, telles que les architectures CNN+LSTM et Transformer, appliquées à des données temporelles.

---

## Contenu du projet

- **data/** : Contient les fichiers de données nécessaires pour l'entraînement. 
  - Le dataset principal peut être téléchargé via ce lien : [Télécharger le dataset](https://drive.google.com/file/d/1N7IFxE9NGfI-ZaAhfcYf0yVAOX52xa0f/view?usp=sharing).
- **models/** : Contient les modèles entraînés sauvegardés.
- **notebooks/** : Notebooks Jupyter utilisés pour le développement et les expérimentations.
- **scripts/** : Scripts Python pour le prétraitement, l'entraînement et l'évaluation.

---

## Résultats obtenus

### 1. **Courbes d'apprentissage pour le modèle CNN+LSTM**
Les courbes montrent la perte (MSE) pendant l'entraînement et la validation pour le modèle CNN+LSTM. La perte d'entraînement reste stable et basse, mais la perte de validation fluctue légèrement, indiquant des variations possibles dans la capacité à généraliser.

![Courbes d'apprentissage](C:/Users/ibrahim/Pictures/Trafic-main/scripts/lstm.png)

### 2. Courbes d'apprentissage pour le Transformer

Les courbes ci-dessous montrent que le modèle Transformer converge rapidement, avec une perte d'entraînement et de validation qui restent stables après quelques époques.

![Courbes d'apprentissage pour le Transformer](C:/Users/ibrahim/Pictures/Trafic-main/scripts/trans.png)

Ce comportement reflète la robustesse de l'architecture Transformer pour les tâches de prévision temporelle.


### 3. **Comparaison des courbes de perte de validation**
Ce graphique compare les pertes (MSE) de validation des modèles CNN+LSTM et Transformer au fil des époques d'entraînement.
On observe que le modèle Transformer converge vers une perte plus basse que le modèle CNN+LSTM, indiquant une meilleure capacité à généraliser sur les données de validation.

![Comparaison](C:/Users/ibrahim/Pictures/Trafic-main/scripts/pred.png)

### 4. **Comparaison des prédictions entre CNN+LSTM et Transformer**
Ce graphique compare les prédictions des deux modèles (CNN+LSTM et Transformer) sur un échantillon de 50 données. 
La ligne bleue représente les valeurs réelles, tandis que les lignes orange et verte représentent respectivement les prédictions des modèles CNN+LSTM et Transformer. 
Ce type de visualisation permet de déterminer quel modèle offre des prédictions plus proches des tendances réelles.


![Comparaison des prédictions](C:/Users/ibrahim/Pictures/Trafic-main/scripts/comp.png)

- **En bleu** : Valeurs réelles
- **En orange** : Prédictions du modèle CNN+LSTM
- **En vert** : Prédictions du modèle Transformer

---

## Modèles utilisés

1. **Modèle CNN+LSTM**
   - Capture des dépendances locales avec des couches convolutionnelles.
   - Capture des dépendances temporelles longues avec des couches LSTM.

2. **Modèle Transformer**
   - Utilise des mécanismes d'attention multi-têtes pour capturer les relations complexes dans les données temporelles.

---

## Résultats chiffrés

| Modèle          | MSE (Validation) | MAE (Validation) | R²    |
|------------------|------------------|-------------------|-------|
| **CNN+LSTM**     | 0.0604           | 0.2056            | -0.0004 |
| **Transformer**  | 0.0334           | 0.1292            | 0.4601  |

---