Telco Customer Churn Analysis and Prediction:
This project analyzes a Telco customer dataset to understand the factors influencing customer churn and predict churn using logistic regression. The code explores the dataset, preprocesses it, performs exploratory data analysis (EDA), and builds a logistic regression model to predict churn.

Project Structure
Data Loading and Inspection: Load and inspect the dataset, checking the first few rows and looking for missing values.
Data Preprocessing: Handle missing values and encode categorical variables for modeling.
Exploratory Data Analysis (EDA): Visualize churn rates and analyze key factors affecting customer churn.
Feature Engineering: Create new features for better predictive power.
Modeling: Train a logistic regression model to predict churn.
Evaluation: Assess the model's performance using classification metrics and a confusion matrix.

Steps
1. Prerequisites
This project requires the following Python libraries:
pip install pandas seaborn matplotlib scikit-learn

2. Loading the Dataset
The dataset, telco.csv, should be located in the same directory as the script. We use pandas to load the dataset and inspect the first few rows to understand its structure.

3. Data Cleaning
Missing values are identified and filled using:
Numerical columns: Filled with the median value.
Categorical columns: Filled with the mode (most frequent value).

4. Exploratory Data Analysis (EDA)
EDA includes:
Customer Churn Rate Analysis: Calculating the percentage of churned customers.
Contract Type vs. Churn: Visualizing how contract type affects churn.
Monthly Charges Analysis: Analyzing monthly charges for churned vs. non-churned customers.
Correlation Analysis: Using a heatmap to show relationships between numerical features.
Satisfaction Score Analysis: Examining satisfaction scores for churned vs. non-churned customers.

5. Feature Engineering
To enhance predictive accuracy, an Age Group column is created by segmenting the Age feature into three categories:
Under 30
30-50
Above 50

6. Encoding Categorical Variables
Label encoding is applied to convert categorical variables into numerical format for model compatibility. The following features are encoded:
Gender
Churn Label
Contract
Payment Method
Offer

7. Model Training and Evaluation
Feature Selection: Selects relevant features for the model, including age, tenure, monthly charges, satisfaction score, contract type, and payment method.
Splitting Data: The data is split into training and test sets (80/20 split).
Logistic Regression Model: A logistic regression model is trained on the data.
Model Evaluation: The model is evaluated using:
Classification Report: Provides precision, recall, and F1-score.
Confusion Matrix: Visualized as a heatmap to show the distribution of predictions.

8. Results
The model performance is assessed with the classification report and confusion matrix, providing insights into the model's accuracy and areas for improvement.

Files
telco.csv: The Telco customer dataset.
main_script.py: The Python script for loading, cleaning, analyzing, and modeling the data.
README.md: Project documentation (this file).

Visualization Examples
The script produces several plots to visualize data:
Count Plot of Contract Type by Churn Label
Box Plot of Monthly Charges for Churned vs. Non-Churned Customers
Heatmap of Correlation Matrix for Numerical Columns
Box Plot of Satisfaction Score by Churn Label

Running the Code
To run the script, ensure that all dependencies are installed and execute:
python main_script.py
