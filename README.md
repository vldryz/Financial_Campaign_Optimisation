# Data Science Technical Challenge - Financial Campaign Optimisation

This repository contains the solution to a technical challenge presented during a hiring process for a Data Scientist role. The challenge, divided into two parts, tested coding skills, data science knowledge, and problem-solving abilities. All code is written in Python (version 3.10 and above) and presented in a Jupyter notebook, with detailed documentation.

## **Part 1: Prediction**

### **Overview**

The first task involved developing and evaluating a machine learning model using a real-world dataset from a financial institution aiming to increase the number of customers with a savings account. The recommended time for this challenge was 2-3 hours. However, I invested a bit more time to learn and apply Plotly, a powerful data visualisation tool, to enhance the analysis.

The institution planned to conduct targeted promotional phone calls, offering customers the opportunity to open a high-interest savings account. The goal was to predict the probability that a call would be successful (i.e., the customer agrees to open a savings account) based on contextual customer information.

### **Original Instructions**

1) **Data Preparation**: Load the provided dataset into a Jupyter notebook. Due to confidentiality, the dataset's link and column descriptions are not included in this document.

2) **Data Splitting**: Split the dataset chronologically into a training set (January to September) and test set (October to December).

3) **Model Building**: Using the training data, create a machine learning model to perform the task described in the problem statement. Briefly justify your design choices and document the steps you take in the model development process.

4) **Model Evaluation**: Select a suitable performance metric and use it to evaluate the model‘s out-of-sample performance on the test set.

### **Additional Contributions**

1) **Data Preparation**: Beyond the original instructions, an in-depth exploratory data analysis was conducted, leveraging Plotly for data visualisation. This analysis revealed significant insights, such as the imbalance in the target column, patterns in call success rates related to the day of the week, month, and time since the last contact.

2) **Model Building**:  Extensive feature engineering and selection were performed to enhance the machine learning model. Multiple new features were created to aid the model's learning process, and Recursive Feature Elimination (RFE) was used to select the top 25 features for training the model. An advanced class balancing technique, SMOTENC, was used to handle the class imbalance issue.

3) **Model Selection and Evaluation**: Precision was used as the primary performance metric to evaluate the model's out-of-sample performance on the test set. This metric was selected to prioritise minimising the likelihood of unsuccessful calls. The Extra Trees Classifier was found to be the most suitable model for this task.

## **Part 2: Optimisation**

### **Overview**

The second task involved using the predictions from Part 1 to devise an optimal promotional campaign strategy. A branch of the financial institution wants to conduct a promotion blitz by calling up to 1,000 people over a week. However, due to resource constraints, no more than 400 people may be called on any single day. The goal was to ensure a fair promotion offer to all community members, regardless of demographic or socioeconomic characteristics.

### **Original Instructions**

1) **Algorithm Development**: Implement an algorithm to maximise the expected number of successful promotion calls, subject to the constraints outlined above. The algorithm should use the predictions from Part 1 as an input.

2) **Policy Evaluation**: Apply your approach to the test dataset and estimate the expected impact of your optimised policy relative to a randomised feasible allocation. State any simplifying assumptions you make as part of this evaluation.

### **Additional Contributions**

1) **Optimisation Problem Definition**: Given the probabilities of successful calls, we formulated the optimisation problem as a maximisation problem, which aims to maximise the total probability of successful calls while not exceeding the available capacity of the customer support team.

2) **Optimisation Method**:  Google's OR-Tools library was used to solve the optimisation problem. The library provides a comprehensive suite of optimisation algorithms for various types of problems, including linear programming, constraint programming, and mixed-integer programming.

3) **Optimisation Implementation**: We used the predicted probabilities from the model developed in Part 1 to identify the customers most likely to respond positively to the campaign. This information was then fed into our optimisation solution to generate a prioritised list of customers to be contacted.

4) **Impact of Optimised Policy**: By implementing our optimised policy, we were able to project an increase in overall profit by $66,320.63 compared to a random calling strategy ($83,928.11 vs $17,607.48). This notable improvement in profitability underscores the effectiveness of our approach, which combined comprehensive data analysis, extensive feature engineering, and optimisation techniques.

## **Project Setup and Usage**

1) Ensure that Python 3.10 or above is installed on your system.
2) Clone this repository to your local machine.
3) Install the necessary Python packages mentioned in requirements.txt.
4) Open the Jupyter notebook and follow the instructions and comments within.

Note: Due to certain limitations on GitHub, Plotly graphs are not displayed in the notebook's preview. Please clone the repository or download `main.ipynb` to see the complete solution with visualisations.

## **Disclaimer**

This project description does not disclose the name of the company which provided this technical challenge. The original problem statement contained specific details about the company, which have been omitted to maintain confidentiality.
