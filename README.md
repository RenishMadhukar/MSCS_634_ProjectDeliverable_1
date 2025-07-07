# MSCS_634_ProjectDeliverable_1

## Dataset Summary
For this project, I used a **heart disease dataset** that contains **303 records** with **14 features**. The dataset includes both numerical and categorical attributes, such as:
- **Age**: The age of the individual.
- **Sex**: Gender (1 = male, 0 = female).
- **Chest Pain Type (cp)**: Type of chest pain the individual experiences.
- **Resting Blood Pressure (trestbps)**: Blood pressure during rest (mm Hg).
- **Cholesterol (chol)**: Serum cholesterol level (mg/dl).
- **Fasting Blood Sugar (fbs)**: Whether fasting blood sugar is greater than 120 mg/dl.
- **Resting Electrocardiographic Results (restecg)**: Results of electrocardiographic tests.
- **Maximum Heart Rate Achieved (thalach)**: The highest heart rate achieved during exercise.
- **Exercise Induced Angina (exang)**: Whether exercise induced angina was experienced.
- **Oldpeak**: Depression induced by exercise relative to rest.
- **Slope**: The slope of the peak exercise ST segment.
- **Number of Vessels Colored by Fluoroscopy (ca)**: A count of colored vessels.
- **Thalassemia (thal)**: A categorical feature indicating the presence of thalassemia.
- **Target**: Whether the individual has heart disease (1 = yes, 0 = no).

I selected this dataset because **heart disease prediction** is a critical problem in healthcare, and it provides a good mix of features for classification and analysis.

## Data Cleaning Steps
1. **Handling Missing Values**: 
   - I found a few missing values in the numerical columns. I chose to **impute** these missing values with the **mean** of the respective columns.
   
2. **Removing Duplicates**:
   - I checked for duplicate rows in the dataset and removed them to ensure the dataset was clean and unbiased.

3. **Identifying and Removing Outliers**:
   - I used **boxplots** to detect outliers in numerical features, such as cholesterol levels. After identifying the outliers, I used the **IQR method** to remove extreme outliers.

4. **Ensuring Correct Data Types**:
   - I verified that each column had the appropriate data type (e.g., categorical variables as `object`, numerical variables as `int` or `float`).

## Key Insights
- **Cholesterol Distribution**: The distribution of **cholesterol levels** was skewed. This suggested that a **log transformation** might be helpful to reduce skewness for future modeling steps.
- **Correlation Between Age and Maximum Heart Rate**: There was a **positive correlation** between **age** and **maximum heart rate**. Older individuals tended to have a lower maximum heart rate during exercise.
- **Heart Disease Prediction**: The **target variable** (heart disease) showed a slight imbalance, with more individuals showing signs of heart disease. However, the data is not overly skewed.
- **Outliers**: I identified and removed outliers, particularly in the **cholesterol** feature, which helped in ensuring the model is not biased by extreme values.

## Challenges
- **Handling Missing Values**: Initially, I was unsure whether to remove rows with missing values or impute them. After considering the impact on the dataset, I chose **mean imputation** for simplicity and consistency across columns.
- **Outliers**: Deciding how to handle outliers was tricky, as removing them could impact the model. However, after visualizing the data with boxplots, I felt confident in removing extreme outliers using the **IQR method** to avoid distortions.

## Next Steps
- **Modeling**: I plan to move on to the next phase, where I will apply machine learning models (such as Logistic Regression, Decision Trees, etc.) to predict heart disease based on the cleaned data.
- **Evaluation**: I will evaluate the models using metrics like **accuracy**, **precision**, and **recall**, and fine-tune them to improve prediction performance.
- **Visualization**: I will continue using visualizations to better understand the model's performance and the feature importance.

## Conclusion
This deliverable focused on the **data cleaning** and **exploratory data analysis (EDA)** of the heart disease dataset. I’ve cleaned the data by handling missing values, removing duplicates, and eliminating outliers. Additionally, I’ve derived key insights, such as correlations between features and their distribution patterns, which will guide future modeling steps. In the next phase, I will work on building predictive models and evaluating their performance.

## Files Included
- **`cleaned_heart_dataset.csv`**: The cleaned dataset after data preparation.
- **`ProjectDeliverable_1.ipynb`**: Jupyter notebook containing all the code for data cleaning, analysis, and visualizations.
- **`Comprehensive_Report.pdf`**: The report summarizing the project steps, findings, and future work.

