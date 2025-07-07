# MSCS_634_ProjectDeliverable_1

## Dataset Summary
In this project, I am working with a heart disease dataset. The dataset contains **303 records** with **14 attributes**, including:
- **Age**: The age of the individual.
- **Sex**: Gender (1 = male, 0 = female).
- **CP (Chest Pain Type)**: A categorical feature indicating the type of chest pain.
- **Trestbps**: Resting blood pressure (mm Hg).
- **Chol**: Serum cholesterol level (mg/dl).
- **Fbs**: Fasting blood sugar (1 if > 120 mg/dl, 0 otherwise).
- **Restecg**: Resting electrocardiographic results.
- **Thalach**: Maximum heart rate achieved.
- **Exang**: Exercise induced angina (1 = yes, 0 = no).
- **Oldpeak**: Depression induced by exercise relative to rest.
- **Slope**: Slope of the peak exercise ST segment.
- **Ca**: Number of major vessels colored by fluoroscopy.
- **Thal**: Thalassemia (categorical).
- **Target**: Whether the person has heart disease (1 = yes, 0 = no).

I selected this dataset because heart disease prediction is a well-known and important medical problem, and it contains a variety of attributes that are useful for prediction tasks.

## Data Cleaning Steps
1. **Missing Values**: I identified and handled missing values in the dataset. Since there were only a few missing values in numerical columns, I chose to impute them with the **mean** of the respective columns.
2. **Duplicates**: I removed any duplicate rows to ensure that my analysis and modeling aren't biased by redundant data.
3. **Outliers**: I used **boxplots** to identify outliers in the numerical columns, particularly in features like cholesterol levels, and I removed extreme outliers using the **IQR method**.
4. **Data Types**: I ensured that all columns had the correct data types (e.g., categorical variables as objects and numerical variables as floats or integers).

## Key Insights
- The distribution of **cholesterol** levels showed a skewed pattern, suggesting that a **log transformation** might be necessary before applying machine learning models.
- A strong positive correlation between **age** and **maximum heart rate** was observed, indicating that older individuals tend to have lower maximum heart rates during exercise.
- Outliers were present in the **cholesterol** feature, which were removed to avoid any distortion in the modeling phase.
- The **target variable** (heart disease presence) is balanced, with a slightly higher number of people having heart disease.

## Challenges
- One challenge I faced was handling the **missing values**, particularly deciding on the best method to impute them. After some consideration, I chose to impute with the mean for simplicity.
- Another challenge was deciding how to handle the **outliers**. I used the IQR method but debated whether to remove them entirely or apply transformations instead.

## Next Steps
- The next step in the project will involve building predictive models using the cleaned dataset.
- I will experiment with different machine learning algorithms (e.g., Logistic Regression, Decision Trees) to predict the likelihood of heart disease in individuals.
- I also plan to evaluate the models and tune their hyperparameters to improve accuracy.

## Conclusion
This deliverable focused on the **data cleaning and exploration** phase of the project. I’ve learned a lot about handling missing data, identifying outliers, and visualizing relationships between features. In the next steps, I will shift focus towards predictive modeling and evaluation.
