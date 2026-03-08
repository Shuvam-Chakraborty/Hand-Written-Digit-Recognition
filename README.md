# ✍️ Hand-written Digit Recognition

A machine learning project that recognizes handwritten digits (0–9) using Logistic Regression on the MNIST dataset, achieving **~91.79% accuracy**.

---

## 📦 Libraries

```python
from sklearn.datasets import fetch_openml
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score
import matplotlib, matplotlib.pyplot as plt
import numpy as np
```

---

## 📊 Dataset

- **Source:** MNIST via `fetch_openml('mnist_784')`
- **Size:** 70,000 samples × 784 features (28×28 pixels)
- **Type:** `float64`, ~418.7 MB

---

## 🔧 Pipeline

| Step | Details |
|------|---------|
| Load | `fetch_openml('mnist_784')` |
| Split | 80% train / 20% test (`random_state=42`) |
| Train | `LogisticRegression()` |
| Predict | Per-sample inference on test set |
| Evaluate | `accuracy_score` |

---

## 🚀 Usage

```python
# Predict a single digit
n = int(input("Enter index: "))
some_digit = x.to_numpy()[n].reshape(28, 28)
plt.imshow(some_digit, cmap='binary'); plt.show()
print("Predicted:", model.predict([x.to_numpy()[n]]))
```

---

## 📈 Results

| Metric | Value |
|--------|-------|
| Accuracy | **91.78571 %** |
