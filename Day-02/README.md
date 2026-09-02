# Day 02 — Data Preprocessing

## 📌 Overview

Data preprocessing is the process of **cleaning and transforming raw data** into a suitable format for a Machine Learning model.

Real-world datasets may contain **missing values, duplicate records, categorical data, and features with different scales**. These problems need to be handled before training an ML model.

---

## 📚 Topics Covered

* Data Preprocessing
* Missing Values
* Mean, Median and Mode
* Duplicate Values
* Categorical Data
* Label Encoding
* One-Hot Encoding
* Feature Scaling
* StandardScaler
* Train-Test Split
* Data Leakage
* `fit_transform()` vs `transform()`

---

## 🧹 Missing Values

Missing values are values that are not available in a dataset.

Common methods:

* **Numerical data** → Mean / Median
* **Categorical data** → Mode
* Rows with unsuitable missing data → `dropna()`

### Pandas Functions

```python
df.isnull().sum()
```

```python
df["age"] = df["age"].fillna(df["age"].median())
```

```python
df["gender"] = df["gender"].fillna(df["gender"].mode()[0])
```

---

## 🔁 Duplicate Values

Duplicate data means the same record appears multiple times.

### Check duplicates

```python
df.duplicated()
```

### Count duplicates

```python
df.duplicated().sum()
```

### Remove duplicates

```python
df = df.drop_duplicates()
```

---

## 🔤 Categorical Data & Encoding

Machine Learning models generally work with numerical data, so categorical values need to be converted into numerical form.

### Label Encoding

Assigns numerical labels to categories.

Example:

```text
Low → 0
Medium → 1
High → 2
```

Useful when categories have a **natural order**.

### One-Hot Encoding

Creates separate binary columns for each category.

Example:

```text
Male   → [0, 1]
Female → [1, 0]
```

Useful for categories with **no natural order**.

---

## ⚖️ Feature Scaling

Feature scaling transforms numerical features to a comparable scale.

For example:

```text
Age    → 20–30
Salary → 25,000–85,000
```

These features have very different scales.

### StandardScaler

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

`StandardScaler` transforms data so that the training features have approximately:

```text
Mean → 0
Standard Deviation → 1
```

---

## 🚨 Data Leakage

Data leakage occurs when information from the test data accidentally becomes available during the training process.

### Important Rule

```text
X_train → fit_transform()
X_test  → transform()
```

The scaler should learn its parameters from **training data only**.

---

## 🧪 Practical Workflow

A messy student dataset was created using a Python dictionary and preprocessing was performed using Pandas and Scikit-learn.

The workflow was:

```text
Raw Dataset
     ↓
Check Dataset
     ↓
Handle Missing Values
     ↓
Check & Remove Duplicates
     ↓
Separate Features & Target
     ↓
Train-Test Split
     ↓
One-Hot Encoding
     ↓
Align Train/Test Columns
     ↓
Feature Scaling
     ↓
Verify Preprocessed Data
```

---

## 🛠️ Libraries Used

* Python
* Pandas
* Scikit-learn

---

## 📁 Files

```text
Day-02/
├── README.md
└── data_preprocessing.ipynb
```

---

## 🎯 Key Learning

The main goal of preprocessing is to convert **raw and imperfect data into clean, consistent and ML-ready data** while avoiding problems such as **data leakage**.
