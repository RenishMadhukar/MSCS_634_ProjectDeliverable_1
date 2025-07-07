# MSCS_634_ProjectDeliverable_1

## Dataset Summary
For this project, I used the **Heart Disease Dataset**, which contains **303 records** and **14 attributes**. The dataset includes both numerical and categorical features, such as:
- **Age**: Age of the individual.
- **Sex**: Gender (1 = male, 0 = female).
- **Chest Pain Type (cp)**: Type of chest pain experienced.
- **Resting Blood Pressure (trestbps)**: Blood pressure during rest (mm Hg).
- **Cholesterol (chol)**: Serum cholesterol level (mg/dl).
- **Fasting Blood Sugar (fbs)**: Whether fasting blood sugar is greater than 120 mg/dl.
- **Resting Electrocardiographic Results (restecg)**: Electrocardiographic results.
- **Maximum Heart Rate Achieved (thalach)**: Highest heart rate achieved during exercise.
- **Exercise Induced Angina (exang)**: Whether exercise induced angina was experienced.
- **Oldpeak**: Depression induced by exercise relative to rest.
- **Slope**: Slope of the peak exercise ST segment.
- **Number of Vessels Colored by Fluoroscopy (ca)**: Count of colored vessels.
- **Thalassemia (thal)**: A categorical feature indicating the presence of thalassemia.
- **Target**: Whether the individual has heart disease (1 = yes, 0 = no).

I chose this dataset because predicting **heart disease** is a significant healthcare challenge, and the dataset provides a range of features that can be useful for classification.

## Key Insights from My Analysis
- **Cholesterol Distribution**: The distribution of **cholesterol** levels was right-skewed, suggesting that a **log transformation** may help in normalizing the data.
- **Age and Heart Rate**: There was a positive correlation between **age** and **maximum heart rate**. This means that older individuals tend to have lower maximum heart rates during exercise.
- **Heart Disease Prediction**: The **target variable** (heart disease) showed a slight imbalance, with more individuals suffering from heart disease. However, the dataset was balanced enough to proceed with predictive modeling.
- **Outliers**: Significant outliers were present in the **cholesterol** feature. I addressed this by removing extreme values using the **Interquartile Range (IQR)** method, ensuring the data is more suitable for analysis.

## Major Steps Taken in Data Cleaning and Exploration
1. **Handling Missing Values**: 
   - I identified a few missing values in the dataset and decided to **impute** them with the **mean** of the respective columns. This ensured the dataset remained complete without losing too many records.
   
2. **Removing Duplicates**: 
   - I checked for duplicate rows in the dataset and found a few duplicates, which I removed to ensure the analysis wasn't skewed by redundant data.
   
3. **Outlier Detection and Removal**: 
   - I used **boxplots** to visually detect outliers, especially in the **cholesterol** feature. After detecting the extreme values, I removed them using the **IQR method** to improve the data's quality.
   
4. **Ensuring Correct Data Types**: 
   - I checked the data types of each column to ensure they were accurate (e.g., categorical variables like **sex** and **cp** were treated as categorical features). I corrected any inconsistencies to avoid errors in analysis.

## Challenges Encountered and How They Were Addressed
1. **Handling Missing Data**: 
   - I initially considered removing rows with missing values but decided to **impute** missing numerical values using the **mean** of the respective columns. This decision helped preserve the dataset size without significantly affecting the quality of the data.
   
2. **Dealing with Outliers**: 
   - I was unsure whether to remove the outliers entirely or apply transformations to make them less influential. After visualizing the data using **boxplots**, I chose to **remove the extreme outliers** using the **IQR method**. This approach ensured that the data would be more suitable for modeling without extreme values affecting the results.

3. **Feature Scaling**: 
   - While I didn't perform scaling in this deliverable, I considered it for the next step of the project. Some features (like **cholesterol**) may benefit from normalization or transformation to improve model performance.

## Conclusion
This deliverable focused on **data cleaning** and **exploratory data analysis (EDA)**. Through this process, I ensured that the dataset was clean, outliers were removed, and missing values were handled. I also identified some useful insights, such as the correlation between **age** and **maximum heart rate**. The next steps in the project will involve building predictive models to classify whether a person has heart disease based on the cleaned dataset.

