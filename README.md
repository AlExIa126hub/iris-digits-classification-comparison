# Logistic Regression vs k-Nearest Neighbours

Machine Learning project comparing the performance of two classification algorithms — Logistic Regression and k-Nearest Neighbours (kNN) — on different datasets.

The project evaluates both **custom implementations** and **scikit-learn implementations**, analysing their performance in terms of classification accuracy, training time and inference time.

Datasets used:
- Iris Dataset
- Digits Dataset

Sources:
https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html  
https://scikit-learn.org/stable/auto_examples/classification/plot_digits_classification.html


---

# Project Structure

```
logistic-vs-knn-comparison/
│
├── logistic_vs_knn.ipynb
└── README.md
```

---

# Project Overview

The objective of this project is to compare two popular classification algorithms:

- **Logistic Regression**
- **k-Nearest Neighbours (kNN)**

The comparison focuses on how these algorithms behave under different dataset conditions and how their performance changes depending on dataset size, feature representation and noise.

The analysis includes:

1. Implementing both algorithms from scratch
2. Evaluating their performance on two datasets
3. Comparing them with the implementations provided by scikit-learn
4. Analysing how dataset modifications influence model performance

---

# Datasets

## Iris Dataset

The Iris dataset contains measurements of iris flowers belonging to three species:

- Setosa  
- Versicolor  
- Virginica  

Each sample includes four numerical features:

- sepal length
- sepal width
- petal length
- petal width

This dataset is commonly used for classification problems and has relatively low dimensionality.

---

## Digits Dataset

The Digits dataset contains images of handwritten digits from **0 to 9**.

Each image:

- is represented as an **8×8 grayscale image**
- is flattened into **64 numerical features**

This dataset represents a **higher dimensional classification problem** compared to the Iris dataset.

---

# Algorithms

## Logistic Regression

Logistic Regression is a linear classification algorithm that models the probability that an input belongs to a given class.

The model estimates class probabilities using the logistic (sigmoid) function and predicts the class with the highest probability.

Logistic Regression is generally efficient and performs well when classes are linearly separable.

---

## k-Nearest Neighbours (kNN)

kNN is a distance-based classification algorithm.

For each data point:

1. The distance to all training samples is calculated.
2. The **k closest neighbours** are selected.
3. The predicted class is determined using **majority voting**.

The algorithm was tested with different values of **k** and different distance metrics in order to optimise performance.

---

# Experiments

## Iris Dataset Experiments

The algorithms were compared on:

- the **original Iris dataset**
- a dataset where the **total number of samples gradually decreases**
- a dataset where the **number of samples decreases for a single class**

These experiments analyse how model performance changes when the dataset becomes smaller or imbalanced.

---

## Digits Dataset Experiments

For the Digits dataset, several variations were analysed:

- original pixel values
- **normalised pixel values**
- **binary pixel representation**
- images with **added noise**

Noise was added to evaluate how robust each algorithm is to data perturbations.

---

# Evaluation Metrics

The algorithms were compared using several metrics:

### Accuracy

```
Accuracy = Correct Predictions / Total Predictions
```

### Training Time

Time required to train the model.

### Inference Time

Time required to make predictions on unseen data.

These metrics help evaluate both the **predictive performance** and **computational efficiency** of the algorithms.

---

# Results and Analysis

The results highlight several important differences between the algorithms:

- **Logistic Regression** tends to train faster because it learns a parametric model.
- **kNN** requires almost no training but can be slower during prediction because distances must be calculated to all training samples.
- Performance differences depend strongly on dataset characteristics such as dimensionality, noise and sample size.

The experiments demonstrate how algorithm choice should depend on the structure of the dataset and the requirements of the problem.

---

# Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

# Running the Project

Install dependencies:

```
pip install numpy pandas matplotlib scikit-learn
```

Launch Jupyter Notebook:

```
jupyter notebook
```

Open and run:

```
logistic_vs_knn.ipynb
```

---

# Datasets

Iris Dataset  
https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html

Digits Dataset  
https://scikit-learn.org/stable/auto_examples/classification/plot_digits_classification.html
