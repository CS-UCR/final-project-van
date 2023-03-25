# final-project-van : CS 108 Gender Bias Project

final-project-van created by GitHub Classroom

Team members: Anushka Pandya, Neha Mathews, Vishal Gondi

Project Description:
Our group chose to do project option 2. We analyzed 2 datasets about gender pay gap to see the disparity between the pay between both genders. We cleaned the data sets by removing unnecessary columns, renaming coloumns to make it more easy to understand, and removing nulls. We used two predictive models: KNN and Linear Regression. 

Challenges + Solutions:
The first challenge that we came across was finding a dataset that included all the attributes that we wanted to include. Many of the datasets were either too small or did not have necessary attributes such as experience or age. We ended up finding two data sets, however, we had to clean a large portion of dataset 1 (PanelIncome) to be able to use it. The second challenge that we came across  was trying to find a visualization to illustrate the importance of features in our models. A solution to this issue was to use the SelectKbest function which gives importance scores for each feature in the linear regression model. The third challenge was with the bias portion.

Conclusion:
The project goal was to analyze the disparity in pay between males and females by using different datasets and examining whether there is bias present or not within the data. After cleaning the data, we will build a predictive models using linear regression and KNN based on the data and used Aequitas toolkit to examine bias in the datasets. We also analyzed the fairness in both datasets. Our first dataset is called "PanelStudyIncomeDynamics_cleaned.csv". We primarily focused on the variables sex, age, and experience. We found that in this dataset sex had a good amount of importance in the linear regression model. This gave reason to believe that there could be a possibility of gender bias present in the dataset. The second dataset is called "GenderPayGap2.csv". In this dataset we focused on gender, age, and seniority. Gender did not have that high of an importance in the linear regression model. This gave reason to believe that gender bias may not be prevalent in this dataset. What we found is that while there is bias present in sex in terms of income, bias is more prevalent in age, experience and seniority. In the first dataset, we also found that age and experience is generally fair, while sex is unfair. In the second dataset, gender, age, and seniority all are generally unfair. 
 
Contributions:
Neha and Vishal worked on cleaning the data and Neha found dataset1. Anushka found dataset 2. Vishal worked on the predictive models. Both Anushka and Neha helped Vishal with the predictive models. Anushka worked on the bias portion. Neha helped Anushka work on the fairness and metrics part. Everyone contributed to creating the readme/report and creating the slides. 

Libraries used:
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import math 
import seaborn as sns
from sklearn import preprocessing
from sklearn.model_selection import train_test_split
from sklearn.neighbors import KNeighborsClassifier
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
from sklearn.neighbors import KNeighborsRegressor


Additional Notes:
Dr. Salloum looked over our project and told us to consider removing age and gender from the trained model and reintroduce it later as individual records. At this time she said it was okay that we kept our project as is but told us to keep this in mind for the future.
