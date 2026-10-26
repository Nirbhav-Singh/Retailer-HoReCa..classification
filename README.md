
# 🏪 Retailer vs HoReCa Customer Classification

### Customer classification using annual wholesale purchase patterns

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Logistic%20Regression-green)
![Dataset](https://img.shields.io/badge/Dataset-UCI-orange)
![Project](https://img.shields.io/badge/Project-IIT%20Ropar-navy)

---

## 1. Project Overview

This project focuses on classifying wholesale customers into two
categories: **HoReCa (Hotels, Restaurants and Cafés)** and
**Retailers**, based on their annual purchasing patterns.

Using the Wholesale Customers dataset from the UCI Machine Learning
Repository, we apply **Logistic Regression**, a supervised machine
learning classification algorithm, to identify patterns in customer
spending across six product categories.

The objective is to develop a model that can predict whether a
customer belongs to the HoReCa or Retail channel based on their
annual expenditure.

---

## 2. Team Members and Responsibilities

| Team Member | Entry Number | Role |
|---|---|---|
| Nirbhav Singh | 2026AIB1064 | Documentation and GitHub management |
| Bhavya Gupta | 2026MCB1522 | Setup and code execution |
| Himanshu | 2026EEB1354 | Presentation |
| Sumanth Nayak | 2026EEB1334 | Video |

*All team members contributed to the development and implementation
of the project. Responsibilities indicate primary areas of work.*

---

## 3. Dataset Description

We use the **Wholesale Customers Dataset** obtained from the
UCI Machine Learning Repository.

Dataset link:
[UCI Wholesale Customers Dataset](https://archive.ics.uci.edu/dataset/292/wholesale+customers)

### Dataset Information

- Total records: 440 customers
- Input features: 6 annual spending categories
- Target variable: Channel
- Classification type: Binary classification
- Missing values: None reported by UCI

### Features Used

| Feature | Description |
|---|---|
| Fresh | Annual spending on fresh products |
| Milk | Annual spending on milk products |
| Grocery | Annual spending on grocery products |
| Frozen | Annual spending on frozen products |
| Detergents_Paper | Annual spending on detergents and paper |
| Delicassen | Annual spending on delicatessen products |

### Target Variable

The `Channel` column represents the customer category:

- **1 – HoReCa:** Hotels, Restaurants and Cafés
- **2 – Retail:** Retail businesses

The `Channel` column is used as the target variable and is not
included among the model's input features.

The original dataset also contains a `Region` column. Our model
uses the six annual spending features as predictors.

---

## 4. Project Workflow

The project follows these major steps:

1. Dataset collection from the UCI repository.
2. Data loading and exploratory data analysis.
3. Data preprocessing and preparation.
4. Splitting the dataset into training and testing sets.
5. Training the Logistic Regression classifier.
6. Evaluating the trained model.
7. Predicting the customer category.

---

## 5. Machine Learning Algorithm

### Logistic Regression

We use **Logistic Regression** as the primary classification
algorithm for this project.

Logistic Regression is a supervised machine learning algorithm
used to predict the probability of an observation belonging to
a particular class.

In our project, it learns the relationship between customers'
annual spending patterns and their respective purchasing channels.

### Working Principle

1. The six annual spending features are provided as model inputs.
2. The algorithm learns coefficients from the training data.
3. It calculates the probability of a customer belonging to
   either class.
4. A classification threshold is used to determine the final
   predicted category.

### Model Input

- Fresh
- Milk
- Grocery
- Frozen
- Detergents_Paper
- Delicassen

### Model Output

- HoReCa
- Retail

---

## 6. Installation and Setup

### Prerequisites

- Python 3.10 or above
- Git
- pip package manager

### Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_REPOSITORY_FOLDER>
```

### Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows**
```bash
venv\Scripts\activate
```

**macOS / Linux**
```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 7. How to Run

After installing the required dependencies, execute the
main project script.

```bash
python src/main.py
```

> Note: Replace the command above with the actual entry-point
> script and path used in your repository.

The program should perform the classification workflow and
display the evaluation results.

---

## 8. Model Evaluation

The Logistic Regression model is evaluated using standard
classification metrics.

The following metrics are considered:

| Metric | Description |
|---|---|
| Accuracy | Overall percentage of correct predictions |
| Precision | Correct positive predictions among all positive predictions |
| Recall | Correctly identified instances of a class |
| F1-score | Harmonic mean of precision and recall |
| Confusion Matrix | Shows correct and incorrect predictions for both classes |

### Evaluation Results

| Metric | Value |
|---|---|
| Accuracy | [Add actual result] |
| Precision | [Add actual result] |
| Recall | [Add actual result] |
| F1-score | [Add actual result] |

*All values should be filled using the actual model evaluation
output. Report class-wise precision, recall and F1-score
where appropriate.*

---

## 9. Results and Visualisations

This section presents the outcomes obtained after training
and evaluating the Logistic Regression model.

### Confusion Matrix

![Confusion Matrix](outputs/confusion_matrix.png)

*The confusion matrix illustrates the correct and incorrect
classifications for HoReCa and Retail customers.*

### Model Performance

![Model Performance](outputs/model_performance.png)

*Visual representation of the model's classification performance.*

### Key Findings

- [Add the main observation from the model results.]
- [Mention which customer category is predicted more accurately.]
- [Mention any important limitation or observation.]

> Replace the example image paths with the actual filenames
> generated by your project. Do not include graphs or metrics
> that have not been produced by your model.

---

## 10. Repository Structure

```text
Retailer-HoReCa-classification/
│
├── data/
│   └── wholesale_customers.csv
│
├── src/
│   ├── main.py
│   ├── preprocessing.py
│   └── model.py
│
├── outputs/
│   ├── confusion_matrix.png
│   └── model_performance.png
│
├── requirements.txt
│
└── README.md
```

*The structure above is a suggested layout. Update it to
match the actual files and folders in the repository.*

---

## 11. Project Links

| Resource | Link |
|---|---|
| GitHub Repository | [Project Repository](<YOUR_REPOSITORY_URL>) |
| Dataset | [UCI Wholesale Customers](https://archive.ics.uci.edu/dataset/292/wholesale+customers) |
| Presentation | [Project Slides](<SLIDES_LINK>) |
| Demonstration Video | [Project Video](<VIDEO_LINK>) |

---

## 12. AI-Use Disclosure

AI tools were used to assist with selected tasks such as
debugging, understanding errors, and improving project
documentation, where applicable.

All submitted code and results were reviewed and verified
by the team.



---

## 13. References

1. Cardoso, M. (2013). Wholesale Customers [Dataset].
   UCI Machine Learning Repository.

   https://doi.org/10.24432/C5030X

2. UCI Machine Learning Repository:
   https://archive.ics.uci.edu/dataset/292/wholesale+customers

---

<p align="center">
  <b>Developed as part of the B.Tech AI & Data Engineering
  academic project at IIT Ropar.</b>
</p>
