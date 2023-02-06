# Analyzing Liberia’s Demographic Data
Emma Dubin
# 1.	Introduction
When creating policies and establishing resources to address education deficits in a population, policymakers must not only know what the education levels of said population are, but also why those education levels are what they are. There are numerous factors that can influence an individual’s level of education, including their location, size, wealth, gender, and age. In the event that Liberian policymakers want to change the overall education levels of their country, they must first recognize the underlying factors that may be contributing to low education levels while also understanding what factors promote higher education levels. In order to better understand this along with numerous other demographic information, the Liberia Institute of Statistics and Geo-Information Services released the 2013 Liberia Demographic and Health Survey. For our research purposes, we will focus on a subset of data released as a result of this survey. This subset of data contains 48,219 data points from individuals. For each individual, there are several independent variables— location, size, wealth, gender, and age. There is also the dependent variable— education.
# 2. Summary Statistics
Number of Observations = 48,219

The average level of education of an individual in Liberia is 0.6653. The average size is 6.9345. The average wealth is 2.4319. The average age is 22.4990.

Table 2.1: Averages, Standard Deviations, and Ranges of Numerical Variables.

![](table1.png) 

There are two genders in the data set. There is a slight majority in Gender 1. There are 15 localities in the data set. The location with the most data points is location 11 with 13.20% of the individuals from there.

Table 2.2: Counts & Proportions for Gender and Location

![](table2.png) 

The average education level for a person of gender 1 is 0.8153. The average education level for a person of gender 2 is 0.5118.

Table 2.3: Average and Standard Deviation of Education by Gender

![](table3.png)

Compared to the average education associated with the complete set of data, the average for individuals with above average (>2.4319) wealth is higher (31.87% increase). There is also more variation in the education levels of the above average wealth subset than there is for the total education level. The average education for the top wealth tier (where wealth is equal to 5) is also significantly higher than the total education average (90.21% increase). In this subset, the data continues to become even more varied than both the original set of data and the above average wealth subset. The average education level for individuals with below average wealth is less than the all data average with a 23.84% decrease. This subset also appears to have the least variation of any of the other education subsets.

Table 2.4: Average and Standard Deviations of Variables of Above/Below Average Wealth Individuals
![](table4.png)
# 3. Histograms
## 3.1: Education
The data is skewed right meaning that there are more individuals with low education levels than there are with high education levels. This means the surveyed population of Liberia is made up of mostly low leveled education individuals. The data is unimodal with a peak at 0-1, showing that most of the population falls into that education range than any other range. 

Figure 3.1: Education Counts

![](education.png)

## 3.2: Location
The location data shows the number of surveyed individuals in each locality of Liberia. The data is unimodal with a peak at 11, indicating that this locality is the most populous amongst those who were surveyed. 

Figure 3.2: Location Counts

![](location.png)

## 3.3: Size
The size data is very skewed to the right meaning that there are more individuals with low size levels than there are with high size levels. The data is unimodal with a peak at 0-5, showing that more of the population falls into that size range than any other range.

Figure 3.3: Size Counts

![](size.png)

## 3.4 Wealth
The wealth data appears to be much more evenly distributed than the previous variables. However, the data still seems to be skewed towards the right. 

Figure 3.4: Wealth Counts

![](wealth.png)

## 3.5 Gender
The gender data appears to be evenly split between the two dummy variables, yet there does appear to be slightly more gender one data points than gender 2 points. 

Figure 3.5: Gender Counts

![](gender.png)

## 3.6 Age
The age data is skewed to the right and unimodal with a peak at 0-10.

Figure 3.6: Age Counts

![](age.png)

# 4. Pairwise Correlation
The pairwise correlation plot reveals that the variable that is most correlated to education is wealth, with a correlation coefficient of 0.2584. The least correlated variable to education is size, with a correlation coefficient of -0.0207. Overall, there is no strong correlation between any of the variables. 

Figure 4: Pairwise Correlation Coefficients Amongst all Variables

![](corr.png)

# 5. Logistic Regression
The logistic regression model fitted with a training split of the data revealed a 57.03% accuracy in correctly classifying the testing split of the data. When the MinMaxScaler was applied to the splits before the model was fitted, the model classified the testing data with 57.02% accuracy. Thus, this scaler made the model slightly less accurate in classifying the data. When the MinMaxScaler was applied after the model was fit, the model classified the testing data with 55.27% accuracy. Once again, the MinMaxScaler actually hindered the performance of the model. 

The RobustScaler and StandardScaler produced similar results to the MinMaxScaler. When applied before the model was fit, the robust scaled model performed with 57.02% accuracy. When applied after the model was fit, it performed with 55.27% accuracy. When the standard scaler was applied before the model was fitted, the model performed with 57.03% accuracy, and when applied after it performed with 56.05% accuracy. 

Out of all the scaled transformations, the Normalizer performed the best. It improved the performance of the model when applied before the model was fit, boasting an accuracy of 64.65%. When applied after the model was fit, it had an accuracy of 55.27% which was comparable to the other scalers when applied at that stage.

Overall, the logistic regression model did a decent job at classifying the data, with a peak accuracy rate of 64.65% when the Normalizer was applied on the testing training split before the model was fit. 
# 6. k-NN
The k-NN model outperformed the logistic regression model. With its default settings, the model performed with an accuracy of 67.40%. However, when experimenting with the n_neighbors parameter, an accuracy of 69.55% was reached when n_neighbors was equal to 92. With some additional experimentation with the other parameters, a peak accuracy of 70.50% was reached when n_neighbors=92, leaf_size=1, and p=1. 

Overall, even the most basic k-NN model outperformed the best logistic regression model. However, with some additional parameters, the k-NN model became the best model thus far with an accuracy of 70.50% on the testing split of the data.
# 7. Decision Tree & Random Forest
The basic decision tree model performed with quite similar accuracy as the best logistic regression at 64.20% (the best logistic regression model had an accuracy of 64.45%). After some testing, a peak accuracy of 71.63% was reached when the parameters max_depth=9 and min_samples_leaf=8 were added. With these additional parameters, the decision tree model outperformed both the best logistic regression model and the best k-NN model.

With its default settings, the Random forest model performed with 67.75% accuracy. The first parameter that was altered was n_estimators. An accuracy of 68.14% was reached when n_estimators was set to 700. A peak accuracy of 72.22% was reached when the additional parameters max_depth=8 and min_samples_split=.001 were included in the model.

Overall, both the best decision tree and random forest models performed the best k-NN and best logistic regression models. The best performance came from the random forest model, with a peak accuracy of 72.22%.

# Summary of Findings
Out of all the models tested, the best random forest model with additional parameters n_estimators=700, max_depth=8, and min_samples_split=.001 performed with the highest accuracy of 72.22% in classifying the data points in the testing split. This model would be the best fit model out of those tested in this study to predict the education level of a Liberian individual, given some basic knowledge of their background. 

