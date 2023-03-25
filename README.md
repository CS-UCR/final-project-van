# final-project-van : CS 108 Gender Bias Project

final-project-van created by GitHub Classroom

## Team members: Anushka Pandya, Neha Mathews, Vishal Gondi

### Project Description:
Our group chose to do project option 2. We analyzed 2 datasets about gender pay gap to see the disparity between the pay between both genders. We cleaned the data sets by removing unnecessary columns, renaming coloumns to make it more easy to understand, and removing nulls. We used two predictive models: KNN and Linear Regression. To create the linear regression model a train test split was used. Then the model was fitted and we predicted on the test set. This was also done for the KNN model. To measure the accuracy of our models we used mean squared error and root mean square error. We calculated feature importance For the linear regression models, to see which features were being used the most by the model. We used aequitas toolkit and preprocessed the data to find bias. We grouped variables like age into age group and experience group into experience for better visuals. We created a false positive rate plot and examined the bias for three variables in each dataset. We then examined the fairness of the variables and examined the disparity on the plots.

### Challenges + Solutions:
The first challenge that we came across was finding a dataset that included all the attributes that we wanted to include. Many of the datasets were either too small or did not have necessary attributes such as experience or age. We ended up finding two data sets, however, we had to clean a large portion of dataset 1 (PanelIncome) to be able to use it. The second challenge that we came across  was trying to find a visualization to illustrate the importance of features in our models. A solution to this issue was to use the SelectKbest function which gives importance scores for each feature in the linear regression model. The third challenge was with the bias portion.

### Conclusion:
The project goal was to analyze the disparity in pay between males and females by using different datasets and examining whether there is bias present or not within the data. Our first dataset is called "PanelStudyIncomeDynamics_cleaned.csv".We primarily focused on the variables sex, age, and experience. We found that in this dataset sex had a good amount of importance in the linear regression model. This gave reason to believe that there could be a possibility of gender bias present in the dataset. The second dataset is called "GenderPayGap2.csv". In this dataset we focused on gender, age, and seniority. Gender did not have that high of an importance in the linear regression model. This gave reason to believe that gender bias may not be prevalent in this dataset. What we found is that while there is bias present in sex in terms of income, bias is more prevalent in age, experience and seniority. In the first dataset, we also found that age and experience is generally fair, while sex is unfair. In the second dataset, gender, age, and seniority all are generally unfair. As a group we decided on some potential improvements to our project. The first one was to try to improve the model. For the KNN model, we could use the Elbow method to find the optimal K value. Additionally,we could look at different combinations fo features. In the end, we found that there wasn’t as much bias present in sex in terms of income as expected. This was surprising since we expected a higher bias since Gender Pay gap is a issue in our society. This project allowed us to learn more about bias. We were able to learn more about ethics of data. It was interesting to see the bias using Aequitus toolkit since we were not familiar with that tool prior to this project.
 
### Contributions:
Neha and Vishal worked on cleaning the data and Neha found dataset1. Anushka found dataset 2. Vishal worked on the predictive models. Both Anushka and Neha helped Vishal with the predictive models. Anushka worked on the bias portion. Neha helped Anushka work on the fairness and metrics part. Everyone contributed to creating the readme/report and creating the slides. 

### Applicable Libraries:
import pandas as pd,
import numpy as np,
import matplotlib.pyplot as plt,
import math,
import seaborn as sns,
from sklearn import preprocessing,
from sklearn.model_selection import train_test_split,
from sklearn.neighbors import KNeighborsClassifier,
from sklearn.linear_model import LinearRegression,
from sklearn.metrics import mean_squared_error,
import matplotlib.pyplot as plt,
import seaborn as sns,
import pandas as pd,
from sklearn.neighbors import KNeighborsRegressor


Additional Notes:
Dr. Salloum looked over our project and told us to consider removing age and gender from the trained model and reintroduce it later as individual records for the bias. At this time, she said it was okay that we kept our project as is but told us to keep this in mind for the future.
