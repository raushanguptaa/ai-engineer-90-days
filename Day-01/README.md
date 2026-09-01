# Day 1 — AI & Machine Learning Foundation

## Overview

Day 1 focuses on the fundamental concepts of Artificial Intelligence and Machine Learning.

## Topics Covered

* Artificial Intelligence
* Machine Learning
* Deep Learning
* Generative AI
* Types of Machine Learning
* Machine Learning Terminology
* ML Workflow
* Train/Test Split
* Overfitting
* Underfitting
* Generalization

## AI vs ML vs DL

```text
Artificial Intelligence
        ↓
Machine Learning
        ↓
Deep Learning
```

### Artificial Intelligence

AI is a field of computer science that focuses on creating systems capable of performing tasks that require human-like intelligence.

### Machine Learning

Machine Learning is a method of AI where a model learns patterns from data and uses those patterns to make predictions or decisions.

### Deep Learning

Deep Learning is a subset of Machine Learning that uses multi-layer neural networks to learn complex patterns from data.

### Generative AI

Generative AI refers to AI systems that can generate new content such as text, code, images, audio, and video.

---

## Types of Machine Learning

### 1. Supervised Learning

The model is trained using data where the correct target/output is provided.

Two major types:

* **Regression** — predicts numerical/continuous values.
* **Classification** — predicts categories/classes.

Examples:

```text
House Price → Regression
Pass/Fail → Classification
Spam/Not Spam → Classification
```

### 2. Unsupervised Learning

The model is trained without a predefined target/label and attempts to discover patterns, relationships, or groups in the data.

Examples:

* K-Means Clustering
* PCA
* DBSCAN

### 3. Reinforcement Learning

An agent interacts with an environment and learns through rewards and penalties.

```text
Agent → Action → Environment
                  ↓
             Reward/Penalty
```

---

## Important ML Terminology

| Term           | Meaning                                |
| -------------- | -------------------------------------- |
| Dataset        | Complete collection of data            |
| Sample         | One individual observation/row         |
| Feature        | Input variable used for prediction     |
| Target         | Output/value the model predicts        |
| Algorithm      | Learning method                        |
| Model          | Trained system                         |
| Parameter      | Value learned during training          |
| Hyperparameter | Configuration used to control training |

In Python/ML notation:

```text
X = Features
y = Target
```

---

## Machine Learning Workflow

```text
Problem Definition
        ↓
Data Collection
        ↓
Data Exploration
        ↓
Data Preprocessing
        ↓
Features + Target
        ↓
Train/Test Split
        ↓
Model Selection
        ↓
Training
        ↓
Prediction
        ↓
Evaluation
        ↓
Improvement
        ↓
Deployment
```

---

## Train/Test Split

Training data is used to learn patterns.

Testing data is kept separate and used to evaluate the trained model on unseen data.

Example:

```text
1000 Samples
     ↓
80% Training
20% Testing
```

In Python:

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

---

## Overfitting

Overfitting occurs when a model performs very well on training data but poorly on unseen data.

```text
Training Data → Excellent
New Data      → Poor
```

## Underfitting

Underfitting occurs when a model fails to learn important patterns from the data.

```text
Training Data → Poor
New Data      → Poor
```

## Generalization

Generalization is the ability of a model to perform well on new/unseen data after learning useful patterns from training data.

---

# Day 1 Practical

## Problem

Predict whether a student will **Pass or Fail** based on:

* Study Hours
* Attendance
* Assignment Score

### Features

```text
study_hours
attendance
assignment_score
```

### Target

```text
result
```

Since the target contains two classes:

```text
Pass
Fail
```

this is a **Classification problem**.

### Model Used

```text
Logistic Regression
```

### Workflow

```text
Dataset
   ↓
Features + Target
   ↓
Train/Test Split
   ↓
Logistic Regression
   ↓
Training
   ↓
Prediction
   ↓
Accuracy Evaluation
```

## Key Learning

* Features are inputs.
* Target is the value to predict.
* Training data is used to learn patterns.
* Test data is used to evaluate performance.
* Classification predicts categories.
* Regression predicts numerical values.
* Overfitting means poor generalization despite strong training performance.
