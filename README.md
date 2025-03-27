<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titanic Survival Prediction</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 40px; }
        h1, h2, h3 { color: #333; }
        code { background-color: #f4f4f4; padding: 2px 4px; border-radius: 4px; }
        pre { background-color: #f4f4f4; padding: 10px; border-radius: 5px; }
    </style>
</head>
<body>
    <h1>Titanic Survival Prediction</h1>
    <p>This project analyzes the Titanic dataset and builds a logistic regression model to predict passenger survival based on age, fare, class, and gender.</p>
    
<h2>Dataset Overview</h2>
    <ul>
        <li><strong>PassengerId:</strong> Unique identifier</li>
        <li><strong>Survived:</strong> 0 = No, 1 = Yes</li>
        <li><strong>Pclass:</strong> Passenger class (1st, 2nd, 3rd)</li>
        <li><strong>Name:</strong> Passenger name</li>
        <li><strong>Sex:</strong> Gender</li>
        <li><strong>Age:</strong> Age of the passenger</li>
        <li><strong>SibSp:</strong> Siblings/spouses aboard</li>
        <li><strong>Parch:</strong> Parents/children aboard</li>
        <li><strong>Ticket:</strong> Ticket number</li>
        <li><strong>Fare:</strong> Fare price</li>
        <li><strong>Cabin:</strong> Cabin number (missing values)</li>
        <li><strong>Embarked:</strong> Port of embarkation (C, Q, S)</li>
    </ul>
    
<h2>Data Preprocessing</h2>
    <ol>
        <li>Dropped the <code>Cabin</code> column due to excessive missing values.</li>
        <li>Filled missing <code>Age</code> values with the mean age.</li>
        <li>Filled missing <code>Embarked</code> values with the most common value ('S').</li>
    </ol>
    
<h2>Installation</h2>
    <pre><code>pip install numpy pandas matplotlib seaborn scikit-learn</code></pre>
    
<h2>Usage</h2>
    <pre><code>import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score

# Load dataset
titanic_dataset = pd.read_csv('tested.csv')

# Data preprocessing
titanic_dataset.drop(columns=['Cabin'], inplace=True)
titanic_dataset['Age'].fillna(titanic_dataset['Age'].mean(), inplace=True)
titanic_dataset['Embarked'].fillna('S', inplace=True)

# Display dataset information
titanic_dataset.info()</code></pre>
    
<h2>Results</h2>
    <p>After data preprocessing, a logistic regression model can be trained to predict survival rates. The model's accuracy can be evaluated using <code>accuracy_score</code> from <code>sklearn.metrics</code>.</p>
    
<h2>Contributing</h2>
    <p>Feel free to fork this repository and contribute improvements or additional analyses.</p>
    
<h2>License</h2>
    <p>This project is licensed under the MIT License.</p>
</body>
</html>
