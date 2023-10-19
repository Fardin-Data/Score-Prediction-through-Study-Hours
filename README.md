# Score Prediction through Study Hours
![image](https://github.com/Fardin-Data/Score-Prediction-through-Study-Hours/assets/137788371/d20a044e-08dc-42a4-bfc4-ecdc4002590a)

## Introduction
This project is part of my internship at "The Sparks Foundation," a renowned organization committed to promoting skill development, innovation, and research in the field of technology and data science. As an intern with The Sparks Foundation, I have undertaken a task that aligns with the organization's mission to foster learning and exploration.

## Objective
Aims to predict a student's anticipated exam score by utilizing a linear regression model, with the input variable being the number of hours they have dedicated to studying.

## Table of Contents
- [Data Source](#data-source)
- [Process](#process)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Data Preparation](#data-preparation)
  - [Model Training](#model-training)
  - [Model Evaluation](#model-evaluation)
  - [Saving the Model](#saving-the-model)
- [File Information](#file-information)
- [Usage](#Usage)

## Data Source
The dataset used for this project can be found at [this link](http://bit.ly/w-data).

## Process

### Exploratory Data Analysis (EDA)
- Checking for null values.
- Identifying and handling duplicates.
- Exploring data types and dataset entries.
- Providing a statistical summary of the data.
- Visualizing the relationship between hours studied and scores.
  
![image](https://github.com/Fardin-Data/Score-Prediction-through-Study-Hours/assets/137788371/f88f1d2a-0a00-4ac9-83a7-dc771863ac52)

### Data Preparation
- Defining the feature (input) and label (output).
- Splitting the data into training and test sets.

### Model Training
- Utilized the Scikit-learn library for linear regression.

### Model Evaluation
- The performance of the model is evaluated using the R-squared (R2) score, which provides insights into how well the model fits the data. The R2 score ranges from 0 to 1, with a higher score indicating a better fit. In this project, the R2 score is 0.89, demonstrating the model's capability to predict scores based on study hours.
  
![image](https://github.com/Fardin-Data/Score-Prediction-through-Study-Hours/assets/137788371/56943ff5-4b32-451e-9492-35d3eb407f90)

### Saving the Model
- Saved the trained model using Pickle, now one can easily use the "score_prediction_model.pkl" file only to import the model without loading this entire ipynb file, and utilize it for predictions.

## File Information

- `data/`: Folder containing the dataset file.
  - `student_scores`: Dataset file used for analysis.
  
- `notebook/`: Folder containing Jupyter notebook file.
  - `Task-1 GRIP.ipynb`: Jupyter notebook containing the code for the entire project.
  
- `model/`: Folder containing model file.
  - `score_prediction_model.pkl`: The trained machine learning model for score prediction.
  
## Usage
To predict a student's score after a given number of hours, simply load the model using the provided "score_prediction_model.pkl" file.

```python
import pickle

# Load the model
with open("models/score_prediction_model.pkl", "rb") as file:
    model = pickle.load(file)

# Predict the score
hours_studied = 9.25
predicted_score = model.predict([[hours_studied]])[0]
print(f"Predicted Score for {hours_studied} hours of study: {predicted_score}")
```

## License
This project is licensed under the MIT License, allowing you to use, modify, and distribute the code and visuals while maintaining the original license terms.

---

For questions or feedback, please contact: fardinkhan.data@gmail.com

Enjoy exploring the project!
