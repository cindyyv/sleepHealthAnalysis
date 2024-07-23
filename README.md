# Sleep Health and Lifestyle Analysis
## Project Overview
This project was developed as a part of the Introduction to Data Science course taken in 2023. Our goal was to analyze the Sleep Health and Lifestyle dataset from Kaggle, which encompasses diverse individual attributes including demographic details, lifestyle factors such as sleep duration, physical activity, stress levels, and health metrics like BMI, blood pressure, heart rate, and daily steps. Additionally, it provides insights into sleep quality and disorders, categorizing individuals based on their sleep patterns—whether they exhibit no sleep disorder, struggle with insomnia, or face sleep apnea-related breathing interruptions during sleep.

## Data Statistics
After loading the dataset, the initial step involved understanding the data and its statistics for each feature. Key observations included the presence of several columns with object or categorical types. The statistics also highlighted quartile, mean, and median values of numerical features.

## Handling Missing Data
We identified duplicated, unique, and missing values, finding that the 'Sleep Disorder' feature had 219 missing instances. We replaced all 'NaN' values in this feature with 'None'.

## Data Preprocessing
The ‘Blood Pressure’ feature, initially in string format, was split into two integer features: ‘High Pressure’ and ‘Low Pressure’. Additionally, the BMI Category feature showed unique values ['Overweight', 'Normal', 'Obese', 'Normal Weight']. We combined 'Normal Weight' with 'Normal' and 'Obese' with 'Overweight', resulting in two unique values.

## Data Visualization and Analysis
Using Seaborn, Matplotlib, and Plotly, we visualized the data by their types. For categorical features, visualizations compared the average sleep duration. For numerical features, scatter plots showed relationships with sleep duration, revealing linear trends. Key insights included:
* Salespeople had the least average sleep duration.
* Insomniacs had lower sleep durations.
* The relationships between numerical features and ‘Sleep Duration’ were mostly linear.

Focusing on the ‘Sleep Disorder’ attribute, we produced various visualizations (bar charts, pie charts, boxplots) to analyze correlations with other features. Key insights included:
* More men than women are classified as 'Normal'.
* More men suffer from Insomnia, while more women suffer from Sleep Apnea.
* Most 'Normal' individuals have high sleep quality.
* Sleep Apnea individuals exhibit slightly more physical activity.
* Insomniacs sleep less than others.
* Sleep Apnea is more common in people in their 40s.
* Boxplots revealed outliers in physical activity levels among Sleep Apnea individuals.

## Correlation Analysis
A correlation matrix, visualized using heat scaling, showed correlation values between features. Categorical features were encoded prior to correlation analysis.

## Data Classification Models
To predict sleep disorders based on the dataset, we tested several classification models. The dataset was split into input (all data except ‘Sleep Disorder’ and ‘person ID’) and output (‘Sleep Disorder’). The input data was normalized and split into training (70%) and testing (30%) sets. The models tested included:
1. **Decision Tree**: Achieved an accuracy of 0.911.
2. **Random Forest**: Achieved the highest accuracy of 0.929.
3. **Logistic Regression**: Achieved an accuracy of 0.9203.
4. **Support Vector Machine (SVM)**: Achieved an accuracy of 0.9203.
5. **K-Nearest Neighbors (KNN)**: Achieved an accuracy of 0.911.
6. **Gradient Boosting**: Achieved an accuracy of 0.9203.
The Random Forest model performed the best, with the highest accuracy of 0.929.

## Conclusion
This project provided valuable insights into the relationships between lifestyle factors and sleep disorders. The Random Forest model proved to be the most effective in predicting sleep disorders. Future work could involve deeper analysis and further tuning of the models to improve prediction accuracy.
