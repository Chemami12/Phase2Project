#KING COUNTY HOUSE PRICE ANALYSIS



## Project Overview

This project uses linear regression analysis to understand how certain variables impact housing prices in King County. Several models  will be genereted in order to create the most accurate coefficients and the highest R-squared value.


### Business Understanding

The real estate market is a critical driver of economic growth in many countries globally. It is a dynamic and ever-changing industry where key stakeholders (buyers and sellers) have to make accurate prediction of home prices in order to make informed decisions through use of reliable and comprehensive data.

Real estate is dramatically affected by its location and factors such as employment rates, economy, crime rates, transport facilities and land rates.

The King County House Sale dataset is a valuable source of information for analysing house sales in the Northwestern county. The dataset has several variables that can act as key indicators in price of houses in this area such as Zip code, number of bedrooms, number of bath rooms, square feet, numeric grade and the year the house was built.
The dataset will be used for analysis and modelling to better understand the factor that affects house pricing.


### The Data

This project uses the King County House Sales dataset, which can be found in  `kc_house_data.csv` in the data folder in this assignment's GitHub repository. The description of the column names can be found in `column_names.md` in the same folder. As with most real world data sets, the column names are not perfectly described, so you'll have to do some research or use your best judgment if you have questions about what the data means.This data is originally from the King County website.

Variables used in final model:
price
bedrooms
bathrooms
sqft_living
numeric_grade
zipcode
Year built

### Data Cleaning

The data needs to be cleaned before it can be used in the linear regression model. The cleaning steps that we followed were:

Finding and Dropping Missing Data
There was missing data in waterfront, view and year renovated columns that were then dropped.

Changing Categorical to Numeric Variables
We had the grade variables that needed to be changed from categorical values to numeric before we could perform any functions on them. The variable was grade. It now has numerical grade and descriptive grade.

Dropping columns
The columns of Id, date, condition and grade were removed as they would not be used in the analysis due to lack of relevance

Dropping Outliers
We removed outliers from our variables

## Methodology

Pandas and numpy was used to explore the data. Columns with duplicates were removed and those with missing values. Then we one hot encoded categorical variables. Statsmodel.api to determine R scores. Matplotlib and seaborn were used for visualizations.  


### Modelling

Baseline Model
After our data was cleaned, we created a baseline linear regression model that only included the price and sqft_living. This model gave us an R-squared value of .383, meaning that our model could only explain 38.3% variance of price.

Increasing R-squared
From there, we aimed to increase our R-squared value by adding in more variables. Our final linear regression model had an R-squared value of 0.560, which is much greater than our baseline.


### Results of model with 6 predictors

1.The model explains a 56% of the variance in price which shows an increase compared to the first model which had a variance of 38% with only one predictor (sqft_living).

2. The model is statistically significant overally, with an F-statistic p-value below 0.05.

3. The model coefficients (const, sqft_living, numeric_grade, bathrooms, bedrooms, yr_built and zipcode) are all statistically significant, with t-statistic p-values of 0.000 which is below 0.05

4. For each increase of 1 sqft in sqft_living, there is an increase in price of about $103

5. For each increase in numeric grade, there is an increase in price of about $114400

5. For each increase of 1 bathroom, we see an associated increase in price of about $45730

6. For each increase of 1 bedroom , we see an associated decrease in price of about $20580

7. For a change in location zipcode, there is an increase in price by $167



### Recommendation
1. The real estate agency should advice their clients that the pricing of houses increases with each sqft increase of the house and they should showcase this.
2. Houses with higher numerical grade fall in high price category. Home owners should be advised to improve the grade of their houses so at to increase their value.
3. There are certain zipcodes that are more expensive than others as the price of houses increases by $167. The real estate agency should highlight this areas to home buyers and sellers.
4. Buyers who are looking for high-end properties may not necessarily prioritize the number of bedrooms. Therefore, sellers should be aware that adding additional bedrooms may not necessarily increase the value of the property as houses with more bedrooms have low prices.
5. The more the bathrooms a house has, the price increases by $45730. The real estate agents should showcase that bathrooms are a great addition to the house as it increases its price.


### Conclusion

This project is aimed to develop a model to predict housing prices in King County based on various features such as square footage, number of bedrooms and bathrooms, grading and zipcode.

Firstly, we performed exploratory data analysis (EDA) and found that the price of houses was positively correlated with the square footage and the grade of the house. We also discovered that the location of the house had a significant impact on the price.

Secondly, multiple linear regression models was used to predict the price of the house. The model included square footage, grade, bedrooms, bathrooms and zipcode as the predictors performed reasonably well, explaining about 56% of the variance in price.

Based on the results, we can conclude that square footage, the numeric grade and zipcode of the house are significant predictors of housing prices in King County. 

#### Next steps

In this project, we were only looking at the coefficients in order to give our recommendations. Further research and indepth analysis can be done to improve the accuracy of the models and to gain a better understanding of the factors that influence housing prices in King County.

