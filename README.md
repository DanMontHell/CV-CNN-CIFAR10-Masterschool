# ResNet50 Image Classification with Transfer Learning

This project demonstrates a progressive tuning process using a pre-trained ResNet50 architecture for image classification. Built using TensorFlow and Keras, the goal is to iteratively enhance model performance on a dataset of 32x32 RGB images by applying transfer learning, fine-tuning, data augmentation, and early stopping.

---

## 🧠 Project Goals

- Explore the impact of transfer learning using ResNet50.
- Incrementally apply model tuning techniques:
  - Layer unfreezing
  - Learning rate adjustments
  - Data augmentation
  - Early stopping
- Evaluate performance across 4 model versions (`v1` to `v4`) to understand which techniques offer the greatest return.

---

## 🧪 Model Versions

| Version | Description |
|---------|-------------|
| V1 | Base ResNet50 (frozen), with dense layers on top |
| V2 | Unfrozen ResNet50 with lower learning rate |
| V3 | V2 + Data Augmentation |
| V4 | V3 + EarlyStopping (and optional Dropout layers) |

---

## 🖼️ Dataset

- Assumes RGB image input of shape `(32, 32, 3)`.
- Labels are integers (`0–9`) for 10-class classification.
- Dataset is split into `train_images`, `train_labels`, `test_images`, and `test_labels`.

---

## 🚀 How to Run

```bash
# Clone the repository:
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

# Install dependencies:
pip install -r requirements.txt

# Launch the notebook:
jupyter notebook CNN.ipynb
```

---

## 🧹 Structure

```bash
├── CNN.ipynb          # Main notebook containing all model versions
├── README.md
├── requirements.txt
```

---

## 📊 Evaluation Strategy
- Accuracy metrics on both training and validation sets.
- Misclassified examples visualized post-prediction.
- Early stopping used to prevent overfitting.

---

## 💡 Key Learnings
- Fine-tuning a pre-trained model significantly improves performance when combined with a lower learning rate.
- Data augmentation improves generalization.
- Early stopping adds training efficiency and regularization benefits.

---

## 📜 License
This project is licensed under the MIT License.

---

## 🙌 Acknowledgements
- TensorFlow
- Keras Applications
