# Pegasos: Primal Estimated sub-GrAdient SOlver for SVM

This repository contains an implementation and analysis of the **Pegasos** algorithm.

## Dataset Description & Installation

For this project, no external data files or manual downloads are required. All datasets are obtained directly via artificial generation or loaded using `scikit-learn` built-in features to ensure reproducibility. There is no traditional "installation" of a dataset other than running the Python code provided below, which pulls or synthesizes the data on the fly.

### 1. Breast Cancer Wisconsin (Diagnostic)

**Source**: A real-world dataset provided built-in with scikit-learn. It contains 569 samples and 30 continuous numeric features for binary classification (Malignant vs. Benign).

**Usage/Installation in Project**:
Loaded via `sklearn.datasets.load_breast_cancer` to evaluate the core implementation, objective convergence metrics, and ablation setups.

```python
from sklearn.datasets import load_breast_cancer
import numpy as np

data = load_breast_cancer()
X, y = data.data, data.target

y = np.where(y == 0, -1, 1)
```
