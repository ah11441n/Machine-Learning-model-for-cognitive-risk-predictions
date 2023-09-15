
Introduction: 

1. Surveys conducted by organizations like OSMI often aim to collect valuable data and insights about the mental health challenges faced by individuals working in the technology sector. These surveys play a crucial role in shedding light on the prevalence of issues such as stress, burnout, anxiety, and depression among tech professionals.
2. Survey Purpose: It would explain that the survey is being conducted to understand better the mental health experiences of individuals in the tech industry. The goal is to gather accurate and comprehensive data that can inform strategies and policies to support employee well-being.
3. Confidentiality: Participants would be assured of the confidentiality of their responses. This is important to encourage open and honest sharing of experiences.
4. Scope: The introduction will mention the specific areas the survey aims to cover, such as work-related stressors, available support systems, experiences of stigma, and personal coping mechanisms.
5. Impacts on Work and Life: It might highlight how mental health challenges can affect not only work performance but also overall quality of life.
6. Future Action: Participants might be informed that the survey results will be used to drive initiatives, resources, and awareness campaigns that address mental health issues within the tech community.


Problem Statement:

1. This analysis aims to understand factors contributing to a person's mental health.
2. The dataset measures mental health attitudes and the frequency of mental health disorders in the tech workplace. 
3. The project will systematically explore workplace mental health, starting with a comprehensive explanation of the dataset and performing EDA.
4. We then create machine-learning models to predict the result
5. What we’re Addressing: We will develop a model to predict whether an employee should seek treatment for mental health.

Source of dataset:
1. 2016 dataset: https://www.kaggle.com/datasets/osmi/mental-health-in-tech-2016
2. 2017 dataset: https://www.kaggle.com/datasets/osmihelp/osmi-mental-health-in-tech-survey-2017
3. 2018 dataset: https://www.kaggle.com/datasets/osmihelp/osmi-mental-health-in-tech-survey-2018
4. 2019 dataset: https://www.kaggle.com/datasets/osmihelp/osmi-mental-health-in-tech-survey-2019
5. 2020 dataset: https://www.kaggle.com/datasets/osmihelp/osmi-2020-mental-health-in-tech-survey-results
6. 2021 dataset: https://www.kaggle.com/datasets/osmihelp/osmh-2021-mental-health-in-tech-survey-results


Data Preparation:

1. The  data sets from 2016-2022 are loaded into DataFrames.

2. Column names are renamed to meaningful one-word names.

3. Unwanted columns deleted.

4. All 6 Data Frames combined into a single data frame.

5. Null values filled with random values from respective columns.

6. Unwanted rows dropped.

7. Meaningless values are renamed to meaningful ones.


Analyzing Data using Visualization:

1. Does an employee's mental health issue impact their productivity, and if so, to what extent?
Observations:
> 85% of employees are unsure whether they are experiencing mental health issues.
> Among them, they report a productivity impact ranging from 1% to 25%.
14% of employees acknowledge that they are indeed dealing with mental health problems.
> A mere 1% of employees state that they are not facing any mental health issues.
Conclusion:
> It's evident that a significant proportion of tech employees are affected by mental health challenges, and this is having an impact on their work.

2. Is the employee currently experiencing a mental health issue, and if so, are they seeking treatment for it?
Observations:
> 46% of employees are uncertain whether they are experiencing mental illness, yet they are actively undergoing treatment.
> 39% of employees are uncertain whether they are experiencing mental illness and have opted not to pursue any form of treatment.
> Among the remaining employees who confirm their mental health challenges, some are undergoing treatment while others are not.
Conclusion:
> Overall, it's evident that there's a complex relationship between employees' perception of their mental health, treatment-seeking behavior, and the need for further support and education in the workplace.


Understanding the type of dataset:

Classification Problem:
1. Involves categorizing input data into predefined classes or categories.
2. The goal is to train a model that can accurately assign new instances to known classes.
3. Supervised learning tasks with labeled training data.
4. The type of problems whose prediction is either one or Zero
5. For Example - Email Spam Detection: which predicts whether an email is "Spam" or "Not Spam" (Ham).
6. Our problem is a binary classification task where the goal is to predict whether an employee should seek treatment for mental health or not.

Reasons to Use Logistic Regression for Classification:
1. Binary Classification: It's specifically designed for binary classification problems, where the outcome falls into one of two classes.
2. Interpretability: The coefficients of the model can be interpreted to understand the impact of each feature on the probability of the positive class.
3. Regularization: Logistic Regression can handle overfitting using L1 (Lasso) or L2 (Ridge) regularization, which helps prevent excessive complexity and improves generalization.
4. Quick Training: It's computationally efficient and relatively quick to train, making it suitable for large datasets.
5. Good Baseline: It serves as a solid baseline model for many classification problems, providing a straightforward starting point for more complex algorithms.
6. Binary Outcome: When the outcome is categorical and binary (e.g., spam or not spam), Logistic Regression offers a simple yet effective way to model the relationship between features and the outcome.
7. Easily Extendable: It can be extended to handle multi-class classification through techniques like one-vs-all (OvA) or softmax regression.
8. Widely Used: Due to its simplicity and interpretability, Logistic Regression has been used in various fields for a long time, making it a well-established choice.


Model Creation with Logistic Regression:
1. The dependent variable is stored in the 'ProfessionalTreatment' column, while all other columns are loaded into the independent variable 'x'.
2. Data Splitting: The dataset is divided  into training and testing sets (80% training, and 20% testing).
3. Feature Scaling: Standardize the features using `StandardScaler` to bring them to a common scale.
4. Model Initialization: Initialize a Logistic Regression model.
5. Model Training: The Logistic Regression model is trained using the scaled training data.
6. Prediction: The trained model is now used to predict the labels for the scaled test data.

Model Evaluation:
1. Accuracy is  Calculated  using `accuracy_score`. Got the output an accuracy of 0.82
2. Classification Report: Classification report shows precision, recall, F1-score, and support for each class using `classification_report`. 


Conclusion:
1. Our task involves binary classification to predict if employees should seek treatment for mental health.
2. We utilized Logistic Regression as our algorithm of choice for this binary classification problem.
3. We focused on dataset preparation, model creation, and evaluation.
4. Logistic Regression's probabilistic output and suitability for binary outcomes make it a good fit.
5. Evaluation included accuracy measurement and classification metrics (precision, recall, F1-score) to assess model performance.
6. Visualization techniques like the confusion matrix and ROC curve were employed to gain insights into the model's predictions.
7. Through this approach, we aim to improve employee well-being by identifying individuals who might benefit from mental health treatment.

