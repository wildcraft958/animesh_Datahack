# Vaccination Prediction Project Report

## Introduction
This report documents my journey in the DataHack hackathon organized by IITG on the GFG platform. The hackathon was about predicting vaccination outcomes for diseases like XYZ and seasonal diseases using machine learning techniques.

## Data Preprocessing
1. **Data Acquisition:** I was given the datasets for training and testing from the GFG platform.
2. **Handling Missing Data:** Dealt with missing data by filling in the missing parts with the most common values.
3. **Encoding Categorical Variables:** Converted categorical variables into numerical format using one-hot encoding.
4. **Data Alignment:** Ensured that the training and testing data had the same columns to facilitate model training.
5. **Scaling Numerical Variables:** Scaled the numerical variables to ensure uniformity in the data.

## Exploratory Data Analysis (EDA)
 Considering time constraint i conducted exploratory data analysis (EDA) using Pandas Profiling to gain insights into the data provided. This included:
- Summary statistics of the data.
- Distribution analysis.
- Correlation between features.
- Detection of missing values and imbalance in the data.

## Model Training
1. **Data Splitting:** Divided the data into train and val sets to train and evaluate the model.
2. **Model Training:** In this i used logistic regression models to train the data for predicting XYZ and seasonal vaccination outcomes.

## Testing Different Techniques
Experimented with different techniques to enhance model performance:
- **Regularization:** Applied L1 and L2 regularization to see their impact on model performance. L1 regularization showed some improvement, while L2 regularization had minimal effect.
- **Testing Without Regularization:** I also tested the models without any regularization to compare the results. The models performed slightly better with L1 regularization compared to without any regularization.

## Model Evaluation
Evaluated the trained models using ROC AUC scores to measure their performance in predicting vaccination outcomes:
1. Logistic regression model performance without regularization using ROC AUC scores.<br>
- ROC AUC for xyz_vaccine: 0.8333404768508013<br>
- ROC AUC for seasonal_vaccine: 0.8591162291109835<br>
- Mean ROC AUC: 0.8462283529808924<br>
<br>
2. Logistic regression model performance with L1 regularization using ROC AUC scores.<br>
- ROC AUC for xyz_vaccine: 0.8334121221289361<br>
- ROC AUC for seasonal_vaccine: 0.8591084671530168<br>
- Mean ROC AUC: 0.8462602946409765<br>
<br>
3. Logistic regression model performance using with L2 regularization ROC AUC scores.<br>
- ROC AUC for xyz_vaccine: 0.833341947574986<br>
- ROC AUC for seasonal_vaccine: 0.8591156646049496<br>
- Mean ROC AUC: 0.8462288060899679<br>

## Selection of model
Based on the in ROC AUC scores of model with different techniques. Finally selected the logistic regression model with L1 regularization which performed slightly better than other.

## Prediction on Test Set
The trained models were used to predict vaccination outcomes on the test set.

## Submission
The predicted probabilities for XYZ and seasonal vaccinations on the test set were saved to a CSV file named `final_submission.csv`.

## Conclusion
Participating in the DataHack hackathon provided me with valuable learning opportunities in machine learning and data analysis. It allowed me to explore various techniques for predicting vaccination outcomes and understand their impact on model performance. I am grateful for the experience gained and look forward to applying these skills in future projects.

## Future scope and improvements
- The models achieved reasonable ROC AUC scores on the validation set, indicating their predictive capability. Further improvements could be made by exploring additional features and experimenting with different machine learning algorithms.
- I didnt deal with some specific issues such as Imbalanced Data and Multicollinearity which i concluded after EDA, dealing with them might have further improved the performance of model.
##
