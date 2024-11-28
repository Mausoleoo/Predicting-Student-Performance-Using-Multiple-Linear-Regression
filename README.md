# Predicting Student Performance Using Multiple Linear Regression
 This project uses multiple linear regression to analyze student performance based on 10,000 observations. Key factors like study hours, previous scores, and sleep hours were analyzed, achieving an R-squared of 0.9888. Insights support informed decisions to enhance academic outcomes.


# Table of content

- Introduction

- Dataset

  - Variables
  - Target Variable
  
- Exploratory Data Analysis
  - Histograms
  - Boxplots
  
- Multiple Linear Regression
  - Dummy variable
  - Correlation Map
  - Fitting
  - Stepwise process
  - Adequacy of the model
- Conclusion



---------------------------------------------------------------------------------------------------------------------------------------------------------------------


# Introduction

In data science and statistical analysis, the application of regression models is a powerful tool for understanding and predicting relationships between variables. As part of our exploration into the diverse landscape of statistical methods, this project explores the complexities of implementing multiple linear regression. The focal point of our investigation is a comprehensive dataset capturing various facets of student performance.

The foundation of this project is grounded in the knowledge gained from our coursework, where we have assimilated the theoretical foundations and practical applications of multiple linear regression and statistical methods. As we traverse through this endeavour, we aim to apply these learned principles to unravel the underlying patterns within the dataset, shedding light on the factors influencing student performance.

The chosen dataset encompasses six variables, ranging from sleeping and studying to extracurricular activities. By employing multiple linear regression, we seek to construct a model that describes the relationships between these variables and enables us to make informed predictions about future student performance.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Dataset

The Student Performance dataset comprises 10,000 observations, each encapsulating six features. This dataset promises a comprehensive overview of factors influencing academic performance. We aim to extract meaningful insights using statistical models, particularly multiple linear regression, to discern patterns within this extensive dataset.

### Variables

- Hours Studied: The total number of hours spent studying by each student.

- Previous Scores: The scores obtained by students in previous tests.

- Extracurricular Activities: Whether the student participates in extracurricular activities (Yes or No).

- Sleep Hours: The average number of hours of sleep the student had per day.

- Sample Question Papers Practiced: The number of sample question papers the student practiced.

### Target Variable

- Performance Index: A measure of the overall performance of each student. The performance index represents the student's academic performance and has been rounded to the nearest integer. The index ranges from 10 to 100, with higher values indicating better performance.

Source: https://www.kaggle.com/datasets/nikhil7280/student-performance-multiple-linear-regression

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Exploratory Data Analysis

### Histograms

![image](https://github.com/user-attachments/assets/25de1ff1-47a1-4699-bd26-1b57cf8cf9ae)

![image](https://github.com/user-attachments/assets/4097a8c9-f316-4347-9693-1ba307758f97)

![image](https://github.com/user-attachments/assets/ec7be083-a9b5-4db5-ad83-7dce3e0f327a)

![image](https://github.com/user-attachments/assets/95a66e03-fca0-40b3-ac1e-da12590263a6)

![image](https://github.com/user-attachments/assets/fd56f9e9-6a1b-4b34-80ca-405e873c64af)

![image](https://github.com/user-attachments/assets/a1ac936e-276e-4d3d-b0e8-aaf0da96520f)

In the histograms, it is evident that Hours.Studied, Previous.Scores, Extracurricular.Activities, Sleep.Hours, and Sample.Question.Papers.Practiced showcase a uniform distribution, implying an even distribution of values.

In contrast, the target variable Performance.Index deviates from this pattern, displaying characteristics consistent with a normal distribution. This deviation suggests a central tendency in Performance.Index, potentially following a bell-shaped curve. These distinct distributional features among predictors and the target variable offer valuable insights, forming a crucial foundation for our subsequent modelling and analytical endeavours.

![image](https://github.com/user-attachments/assets/2cbee588-13fb-4ad1-b6c5-bce0105d0e05)

![image](https://github.com/user-attachments/assets/77363726-f518-4be0-981d-2c22a6105ab6)

It becomes apparent that the variables Previous.Scores and Performance.Index exhibit a discernible linear correlation. The plotted data points suggest a trend where an increase in Previous.Scores aligns with a corresponding rise in Performance.Index, indicative of a positive linear relationship between these two variables. This observation underscores the potential predictive power of Previous.Scores in influencing the overall performance index, providing a valuable insight for further analysis and model development.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Boxplots

![image](https://github.com/user-attachments/assets/98a7e6ef-59d0-4502-a98e-1ddd15432483)

The boxplots for the features Hours.Studied, Previous.Scores, Sleep.Hours, Performance.Index, and Sample.Question.Papers.Practiced reveal a centralized distribution of data. This is evident as the medians are positioned near the center of each box, indicating a balanced distribution of values within these features. Notably, the absence of outliers in the boxplots suggests a consistent and concentrated spread of data points, reinforcing the stability of these variables.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Multiple Linear Regression

### Dummy variable

As the the feature Extracurricular.Activities is a categorical variable with values of yes or no. It must be changed to a numerical value. That is why a dummy variable has been used. The value yes has been changed for 1 and no for 0.

### Correlation Map

![image](https://github.com/user-attachments/assets/71dbef8c-9a08-47ba-9c1e-21ad400fbf13)
