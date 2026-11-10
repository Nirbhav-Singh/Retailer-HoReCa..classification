
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
| Nirbhav Singh | 2026AIB1064 | Documentation and GitHub Lead|
| Bhavya Gupta | 2026MCB1522 | Execution Lead|
| Himanshu | 2026EEB1354 | Video Lead |
| Sumanth Nayak | 2026EEB1334 | Presentation Lead |

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
git clone "https://github.com/Nirbhav-Singh/Retailer-HoReCa..classification"
cd "Retailer-HoReCa..classification"
```
### Create a Virtual Environment

A virtual environment is created to keep the project's Python dependencies isolated from other Python projects.

```bash
python -m venv venv
```

### Activate the Virtual Environment

**Windows (Command Prompt):**
```bash
venv\Scripts\activate
```

**Windows (PowerShell):**
```powershell
.\venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
source venv/bin/activate
```

### Upgrade pip

Upgrade pip to the latest available version:

```bash
python -m pip install --upgrade pip
```

### Install Dependencies

Install all the required Python libraries listed in `requirements.txt`:

```bash
python -m pip install -r requirements.txt
```

### Set Up Jupyter Notebook Kernel

To run the project in Jupyter Notebook using the created virtual environment, install and register the Jupyter kernel.

Install Jupyter Notebook and IPython Kernel:

```bash
python -m pip install ipykernel notebook
```

Register the virtual environment as a Jupyter kernel:

```bash
python -m ipykernel install --user --name horeca-env --display-name "AI101 Project first year B-Tech.ipynb"
```

After registration, select **Python (HoReCa Project)** as the kernel when opening the project notebook in Jupyter Notebook.

### Verify Installation

Check whether Python and pip are installed correctly:

```bash
python --version
python -m pip --version
```

After completing these steps, the project environment is ready to run the classification program.

---
## 7. How to Run

The project is implemented using Jupyter Notebook. Follow the steps below to execute the project.

### Launch Jupyter Notebook

```bash
jupyter notebook
```

you can also write `code .` in the terminal.
### Open the Project Notebook

Open the project notebook (`.ipynb` file) from the Jupyter Notebook interface.

### Execute the Notebook

Run the notebook cells sequentially from beginning to end to perform data loading, preprocessing, model training, evaluation, and prediction.

The notebook displays the classification results and visualisations after execution.
--- 

## 8. Model Evaluation

The Logistic Regression model is evaluated using standard
classification metrics.

The following metrics are considered:

| Metric | Description |
|---|---|
| Accuracy |the proportion of total binary predictions (both positive and negative) that the model gets right |
| Precision | Correct positive predictions among all positive predictions |
| Recall | Correctly identified instances of a class |
| F1-score | Harmonic mean of precision and recall |
| Confusion Matrix | Shows correct and incorrect predictions for both classes |

### Evaluation Results of the original model

| Metric | Value |
|---|---|
| Accuracy | 92.424% |
| Precision | 42/45 |
| Recall | 42/44 |
| F1-score | 0.944 |

### Evaluation Results of the improved model

| Metric | Value |
|---|---|
| Accuracy | 93.939% |
| Precision | 43/45 |
| Recall | 43/45 |
| F1-score | 0.956 |


---

## 9. Results and Learnings
Original model displayed an accuracy of 92.424% with an F1 score of 0.944 while the improved
model(obtained by removing a less important feature) achieved an accuracy of 93.939% and an F1 score
of 0.956 in testing.

The improved model saw an increase in both accuracy as well as F1 score.
While its accuracy improved by 1.515%, its F1 score increased by 0.015.

We learnt that reducing the number of input features by removing either of the highly correlated ones
can help us improve the performance of the model.
We also learnt that a clean and organised dataset is the base of any model and selecting/preparing such
a dataset is the first step towards building any model.

A KEY OBSERVATION:
Reducing the test size to a very small value(eg. just 10% of the whole data) gave us a remarkable accuracy score,
but such a train-test split has a risk that we will not be able to detect an existing overfitting issue.
This is because, a very small-sized testing set has a high chance that it will not include such edge cases which 
will not be correctly predicted by the model. In that case the overfitting would remain 'hidden'.




### Confusion Matrix

![Confusion Matrix]
("https://github.com/user-attachments/assets/817ef2f2-f7f8-4457-b7e7-8a75f7f48368" /)

*The confusion matrix illustrates the correct and incorrect
classifications for HoReCa and Retail customers.*


---

## 10. Repository Structure

```text
Retailer-HoReCa-classification/
│
├── data/
│   └── wholesale_customers_data.csv
│
├── src/
│   ├── main.ipynb
│   ├── preprocessing.ipynb
│   └── model.ipynb
│
├── outputs/
│   ├── confusion_matrix.png
│   └── model_performance.png
│
├── requirements.txt
│
└── README.md
```


---

## 11. Project Links

| Resource | Link |
|---|---|
| GitHub Repository | [Project Repository](https://github.com/Nirbhav-Singh/Retailer-HoReCa..classification) |
| Dataset | [UCI Wholesale Customers](https://archive.ics.uci.edu/dataset/292/wholesale+customers) |
| Presentation | [Project Slides](<SLIDES_LINK>) |
| Demonstration Video | [Project Video](<VIDEO_LINK>) |

---

## 12. AI-Use Disclosure

AI tools including Chat Gpt were used to assist with selected tasks such as
handling Grammar, understanding errors, and improving project
documentation, where applicable.

All the results were reviewed and verified
by the team.

All submitted code has been written completely by the team members without any AI-use.





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
