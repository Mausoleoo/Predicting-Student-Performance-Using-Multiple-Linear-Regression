# Predicting Student Performance Using Multiple Linear Regression
 This project, coded in R, uses multiple linear regression to analyze student performance based on 10,000 observations. Key factors like study hours, previous scores, and sleep hours were analyzed, achieving an R-squared of 0.9888. Insights support informed decisions to enhance academic outcomes.


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

### Training

![image](https://github.com/user-attachments/assets/1a14ed8b-b024-421c-917e-6546c2d92eda)

The P-values for each parameter in our analysis are remarkably low, approaching almost zero. The low P-values indicate a high level of statistical significance, suggesting that each parameter plays a significant role in influencing the observed outcomes. 

The model achieved a remarkable R-squared of 0.9888, signifying that 98.88% of the dependent variable's variance is explained by the independent variables. The Adjusted R-squared, closely trailing at 0.9887, adjusts for predictor count, these high values suggest a strong fit.

### ANOVA table

![image](https://github.com/user-attachments/assets/0dddbefa-34d5-4345-8f9e-feb6ea98a846)

![image](https://github.com/user-attachments/assets/0865c5cb-8a7c-4390-802d-a6d926402e6b)

A remarkably low Sum of Squares Error (SSE) suggests that the linear regression model effectively captures and explains the variability in the data, resulting in a highly precise fit.

### Stepwise process

![image](https://github.com/user-attachments/assets/4feff5a4-03e6-436a-973a-1c9f50fd24a2)

The stepwise process, guided by the Akaike Information Criterion (AIC), sequentially optimized the model by adding or removing variables. The decreasing AIC values (14246, 14468, 14961, 15727, 40733, 57567) indicate the iterative refinement, with the final model having the lowest AIC (14246), suggesting a well-balanced when all the predictors are used.

### Adequacy of the model

![image](https://github.com/user-attachments/assets/722f38f1-b07e-4340-85e9-51ecc4f9d0d5)

The points in the QQ plot of residuals are close to the line, which indicates that the residuals follow a normal distribution. Having residuals that closely follow the line in a QQ plot is a good sign for the validity of the linear regression model. It implies that the model assumptions related to the distribution of errors are met, which enhances the reliability of statistical inferences and predictions made by the model. 

# Conclusion

In this project, we embarked on a comprehensive exploration of a dataset on student performance, applying statistical methods learned in the course, including multiple linear regression. The dataset, comprising 10,000 observations with six features, was a rich source for uncovering patterns influencing academic outcomes. We observed distributions and relationships through histograms, correlation maps, and boxplots, laying the foundation for our regression modelling.

The regression model, with an impressive R-squared of 0.9888 and an adjusted R-squared of 0.9887, showcased its effectiveness in explaining student performance. The low p-values of all parameters underscored their significance, and the confidence intervals at a 95% confidence level provided insights into parameter precision.

Further analysis involved examining residuals through QQ plots and residuals vs. fitted values plots. The QQ plot displayed adherence to normality assumptions, while the residuals vs. fitted values plot revealed a random, patternless scatter with a uniform spread, validating the model's linearity and homoscedasticity assumptions.

In conclusion, the project successfully applied regression techniques to understand and predict student performance with a robust model supported by thorough statistical diagnostics. The adherence to assumptions and the model's reliability encourage confidence in leveraging these insights for informed decision-making in educational contexts.
