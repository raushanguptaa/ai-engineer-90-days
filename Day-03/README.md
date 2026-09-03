# Day 03 — Model Training & Evaluation

## 📌 Overview

In Day 3, I learned how to train a Machine Learning model, make predictions, and evaluate its performance using different classification metrics.

## 🎯 Topics Covered

* Model Training
* `fit()`
* `predict()`
* Logistic Regression
* Accuracy
* Confusion Matrix
* TP, TN, FP, FN
* Precision
* Recall
* F1 Score
* Classification Report
* Train vs Test Accuracy

## 🧠 Practical Work

I created a small student performance dataset containing:

* Study Hours
* Attendance
* Assignment Score
* Result

I used **Logistic Regression** to predict whether a student would **Pass or Fail**.

### Basic Workflow

```text
Dataset
   ↓
Features (X) & Target (y)
   ↓
Train-Test Split
   ↓
Logistic Regression
   ↓
Model Training
   ↓
Prediction
   ↓
Model Evaluation
```

## 💻 Important Code

### Train Model

```python
model = LogisticRegression()
model.fit(X_train, y_train)
```

### Make Predictions

```python
y_pred = model.predict(X_test)
```

### Accuracy

```python
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)
```

### Confusion Matrix

```python
cm = confusion_matrix(y_test, y_pred)
print(cm)
```

### Classification Metrics

```python
precision_score(y_test, y_pred, pos_label=1)
recall_score(y_test, y_pred, pos_label=1)
f1_score(y_test, y_pred, pos_label=1)
```

### Classification Report

```python
print(classification_report(y_test, y_pred))
```

### Train vs Test Accuracy

```python
train_accuracy = model.score(X_train, y_train)
test_accuracy = model.score(X_test, y_test)

print("Train Accuracy:", train_accuracy)
print("Test Accuracy:", test_accuracy)
```

## 📊 Results

For this small practice dataset:

* Train Accuracy: **100%**
* Test Accuracy: **100%**
* Precision: **100%**
* Recall: **100%**
* F1 Score: **100%**
* Confusion Matrix: **No incorrect predictions**

> Note: The test set contained only 4 samples, so these results should not be considered proof that the model will achieve 100% accuracy on real-world data.

## 📚 Key Learning

> Training a model is only one part of Machine Learning. We also need to evaluate the model to understand how well it performs on unseen data.

## 📁 Files

```text
Day-03/
├── README.md
└── model_training_evaluation.ipynb
```
