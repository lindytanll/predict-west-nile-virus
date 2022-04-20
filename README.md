# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 4: West Nile Virus Prediction

### Description

1. As an employee of Disease And Treatment Agency, division of Societal Cures In Epidemiology and New Creative Engineering (DATA-SCIENCE), we are tasked to better understand the mosquito population and advise on appropriate interventions which are beneficial and cost-effective for the city.


2. Through this exploration, we hope to:

- Identify features which are most important to predict presence of West Nile Virus (which can be done by ranking the coefficients of each feature in a logistic regression model)
- Predict the probability of West Nile Virus (WNV) by location to provide decision makers an effective plan to deploy pesticides throughout the city, which consequently can help to reduce cost.


#### About: The Datasets and Data Cleaning

Data has been given to us for mosquito traps set up all over Chicago, and the number of mosquito trapped and presence of WNV. These are spread out across multiple years and within the years, multiple dates where data was collected. For the test dataset, there are different years compared to that of the train.

Weather data was also provided, which was collected by 2 different weather stations, with features such as average temperature, rainfall, and sun rise and sunset.

Spray data, which aims to reduce the population of mosquitoes, also was provided.

Null values were cleaned for the data sets, and certain missing values were interpolated and imputed.


---

#### About: Exploratory Data Analysis

Data features that we have explored include

1) WNV presence by year
2) WNV presence in traps
3) Existence of co-relation spatially for WNV
4) Whether data can be used since there are missing data between years 
5) Weeks which WNV has peaked
6) Weather variables that might have contributed to peaks (e.g. high temperatures and precipitation)
7) Lagged effect of precipitation on WNV presence
8) Station pressure having inverse relationship with precipitation and by extension WNV


#### About: Model Exploration and Feature Selection and Model Selection

Models that we ran through included Logistic Regression, Random Forest, SVM, ExtraTrees, ADA Boost, Gradient Boost and Neural Network.
Due to the paucity of positive cases (i.e. WNV Positive) in our dataset, we had to SMOTE our train data for WNV present cases to allow for better training of the model, and to also not get a model where the accuracy high, but is simply the negative class.

For model selection: 

For feature engineering, we did some changes such as having interaction terms, which eventually turned out interaction between terms scuh as average temperature with precipitation.

Eventually, we decided to go for Logistic Regression as it is able to quantify the impact of features on the probability of WNV, and the AUC (Area under the curve) ROC (receiver operating characteristics) curve is quite clsoe to the other models. 


#### About: Cost Benefit Analysis

Using an estimate of the number of people who might get the virus based on our model and past data (which indicates an approximate infection rate), we are able to get the number of people who might get the virus, and subsequently cost saved if citizens do not get infected with the virus. By estimating the area where we need to spray based on a 1Km radius around the traps, we found out that the cost saved will be higher than the costs of spraying, even before factoring any factors of increased public health and reduced disamenities.

We subsequently tried another model of 30% threshold to be considered as a positive case, which deferred from the default 50%. This means that more cases will be considered as positives, and we are able to catch more true positive cases. However, more false negative cases will be casught as well, and a wider area has to be sprayed. However, the increase in true positives of about 14 patients helped to defray costs of increased spray.

We therefore would prefer to choose the model of 30% threshold for positive cases.



---

## Conclusions, Recommendations:

Probability of WNV increases exponentially from week 31 to 35, especially when there is a combination of high temperature and precipitation (rainfall). Certain traps have higher chance of contracting WNV (e.g. T900, T003, T028).

We recommend using Logistic Regression with 30% threshold to predict WNV

    89% of WNV+ is being captured our model (based on sensitivity)
    15% of our positive predictions are correct
    More cost-effective for the city 

Benefits to public health are economically significant when compared to the cost of eradicating mosquitoes
    
    About 14 more true positives can be prevented in 2014, preventing medical costs
    
    Cost of spray is lower than short and long term medical costs

Next steps:

    Further tune parameters to improve accuracy
        More weather features and their interaction
        Grouping of traps based on risk level (likelihood of WNV)

    





---