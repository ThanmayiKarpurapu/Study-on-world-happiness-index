**Intoduction:**
In an ever-evolving world, the pursuit of happiness is a fundamental aspiration for individuals and nations 
alike. The World Happiness Index, a comprehensive measure of well-being and life satisfaction, offers a 
unique lens through which we can analyze and understand the factors that contribute to happiness on a 
global scale.  
Leveraging the power of Python, this project delves into the exploration and analysis of the World 
Happiness Index dataset, aiming to uncover patterns, trends, and insights that shape the happiness landscape 
across countries and over time. 


**Data Source:**
https://worldhappiness.report/data/ 
The World Happiness Report is a landmark survey of the state of global happiness and we aim to study 
how happy we actually are. 
For this study we have taken the data from the link displayed on screen. The time coverage for the dataset 
is from 2005 to 2023. There are approximately 165 countries which we have taken into consideration while 
doing our analysis. 


**Variables taken into Account while doing the study are as follows:**
● Country Name: Name of Countries 
● Year: Years taken into account  
● Life Ladder: This is the indication of Happiness score. The top of the ladder represents the best possible 
life for you and the bottom of the ladder represents the worst possible life for you. 
● Log GDP Per capita: The statistics of GDP per capita (variable name gdp) in purchasing power parity 
(PPP) at constant international dollar prices from World Development Indicators 
● Social Support: This is to check whether there is anyone you can count on in times of help and other 
such variables that define the happiness of a person. 
● Healthy Life Expectancy at Birth: It is the expected age of a child at birth. 
● Freedom to make Life Choices: It is the national average of responses to the question: Are you 
satisfied or dissatisfied with your freedom to choose what you do with your life?  
● Generosity: It is the national average of responses to the question: “Have you donated money to a 
charity in the past month?” on GDP per capita. 
● Perceptions of Corruption: The measure is the national average of the survey responses to two 
questions: “Is corruption widespread throughout the government or not” and “Is corruption widespread 
within businesses or not?” The overall perception is just the average of the two 0-or-1 responses. 
● Positive Effect: The average of three positive affect measures in GWP: laugh, enjoyment and doing 
interesting things in the Gallup World Poll waves 3-7. 
● Negative Effect: The average of three negative affect measures in GWP. They are worry, sadness and 
anger, respectively. 


**MISSION OBJECTIVES:** 
● To identify what is the average happiness throughout all years in all countries 
● To understand which are the Top happiest & Bottom least happy 10 countries  
● To analyze the correlation between the variables that define the Happiness of a country 
● To predict the Happiness of any particular country with the given variables by using Machine 
Learning 


**Data Cleaning:**
1. We ensure data integrity by conducting a thorough examination for duplicates and affirming the 
absence of any duplicate entries in our dataset. 
2. Removed data pertaining to the years 2005 and 2006, where the datasets exhibited less than 100 
rows, optimizing dataset quality. 
3. Tackled missing data by utilizing the isna() method for each column, effectively identifying cells 
containing NaN values. 
4. Employed a data-driven approach to handle missing values by imputing them with country-specific 
mean values, preserving the overall coherence and reliability of the data. 
5. Post-imputation, 
we conducted a validation check, revealing that the 
'country_healthy_life_expectancy' column for Hong Kong S.A.R. of China and Kosova, as well as 
the 'country_corruption' column for China and Turkmenistan, were entirely populated with NaN 
values. 
6. Recognizing that the mean value would also be NaN, we made the informed decision to drop entire 
rows associated with these countries, ensuring data accuracy. 
7. Achieved data consistency by eliminating both missing and duplicate values, resulting in a refined 
dataset ready for further analysis. 

**EXPLORATORY DATA ANALYSIS:**
Descriptive Statistics: 
In our exploratory data analysis (EDA), we began by visualizing the trend of the happiness index over the 
years. This provided insights into how overall happiness has evolved across different time periods. 
Subsequently, we delved into the relationship between happiness and specific variables. We examined how 
perceptions, freedom to make life choices, and negative affect varied over time in relation to the happiness 
index. This approach allowed us to uncover potential patterns, correlations, or trends associated with these 
factors and their impact on overall happiness. 

By conducting this EDA, we aimed to gain a comprehensive understanding of the dynamics between the 
happiness index and selected variables, shedding light on the nuanced factors that contribute to or influence 
happiness trends over the years.

1. Happiness Index Trend Over the Years
2. Happiness V/S Perception of Corruption Over the years
3. Happiness V/S Freedom to make Life choices Over the years
4. Happiness V/S Negative Affect Over the years
5. Bar Graph of top 10 and lowest 10 countries based on life ladder
7.  Bar graph of country vs Number of times in top 10
8.  Correlation Matrix
9.  Violin plots

**MACHINE LEARNING:**
For performing model validation, we applied Machine Learning techniques on our World Happiness Index 
dataset. 
The steps we followed for regression modeling were- 
1. Defined features (X) and target variable (Y) i.e. Happiness score 
2. Split the dataset into training and testing sets (80%-20% split) 
3. Train the model using the training data 
4. Made predictions on the testing set 
5. Displayed model outcomes using scatter plot 
6. Assessed model performance using metrics like squared mean error and R squared value

We evaluate our model by checking two important parameters- MSE (Mean Squared Error) and R-squared 
Score. A lower MSE value indicates better model performance. R-squared values close to 1.0 indicate a 
good fit, while values close to 0.0 indicate poor fit. 
Both models are pretty good and accurate with high R-squared values of 0.795 for simple linear regression 
and 0.878 for random forest regression. They also have lower MSE values of 0.25 for simple regression 
and 0.15 for random forest regression. 
Random forest has lower values of residuals, showing less differences between predicted and actual values. 
Random forest is an ensemble model where the building blocks are decision trees, which get trained on a 
random set of data, due to which it does not overfit and gives a much robust output as shown by its lower 
MSE value and higher R-squared value 

How is this model useful to us? It can help in many ways such as- 
1. Predictive Analytics: The trained model can be used for predictive analytics to estimate future 
happiness scores based on changing conditions. 
2. Understanding Feature Importance: The feature importance scores provide insights into which 
factors contribute the most to happiness scores. 
3. Monitoring Changes Over Time: The model can be applied to new data to monitor changes in 
happiness trends over time. 
4. Targeted Interventions: With insights into feature importance, interventions can be targeted at 
improving specific aspects that have a significant impact on happiness. This could involve targeted 
social programs, health initiatives, or measures to enhance personal freedoms and choices. 
5. Monitoring Changes Over Time: The model can be applied to new data to monitor changes in 
happiness trends over time. Tracking shifts in feature importance and happiness scores provides a 
dynamic view that can inform ongoing strategies and interventions. 
6. Resource Allocation: Organizations and governments can allocate resources more efficiently by 
understanding which factors are most influential in determining happiness. This can lead to more 
effective resource distribution for the well-being of the population. 
7. Predictive Analytics: The trained model can be used for predictive analytics to estimate future 
happiness scores based on changing conditions.

**CONCLUSION:**
The analysis of global happiness metrics reveals a heartening trend; the average happiness score for the 
leading ten countries stands at an impressive 7.5. Additionally, the general trajectory of happiness over the 
years suggests a positive incline, hinting at improving global sentiments. Core determinants such as 
economic output, social frameworks, and health parameters emerge as pivotal influencers in shaping a 
nation's happiness quotient. Notably, regional disparities in these happiness trends are apparent, reflecting 
the unique socio-economic and political landscapes that characterize different geographies. The utilization 
of regression models has proven to be particularly effective, offering a significant degree of accuracy in 
predicting national happiness levels. This not only validates existing well-being metrics but also encourages 
deeper exploration into the science of happiness and its determinants. 


**RECOMMENDATIONS:**
In light of the findings, it is recommended that health care be made a universal mandate, assuring all citizens 
equitable access to essential medical services, which is a cornerstone for fostering national happiness. 
Economic strategies should also be revised to prioritize growth in GDP per capita, focusing on bolstering 
investment and developing infrastructure as means to this end. Moreover, to sustain and improve the 
happiness index further, it is imperative for policies to nurture work-life balance. This could involve 
instituting flexible working arrangements and comprehensive parental leave policies, thereby addressing 
the multidimensional nature of happiness and contributing to the well-being of the populace. By 
implementing these recommendations, governments can make significant strides towards enhancing the 
collective contentment and prosperity of their nations.
The analysis of global happiness metrics reveals a heartening trend; the average happiness score for the 
leading ten countries stands at an impressive 7.5. Additionally, the general trajectory of happiness over the 
years suggests a positive incline, hinting at improving global sentiments. Core determinants such as 
economic output, social frameworks, and health parameters emerge as pivotal influencers in shaping a 
nation's happiness quotient. Notably, regional disparities in these happiness trends are apparent, reflecting 
the unique socio-economic and political landscapes that characterize different geographies. The utilization 
of regression models has proven to be particularly effective, offering a significant degree of accuracy in 
predicting national happiness levels. This not only validates existing well-being metrics but also encourages 
deeper exploration into the science of happiness and its determinants. 
