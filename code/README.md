# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

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

#### About: Model Exploration and Feature Selection

Models that we ran through included
1) Logistic Regression
2) 
3) 
4)
5)
6)
7)
8)
9)


#### About: Cost Benefit Analysis





---

## Conclusions, Recommendations:



Our best model for accuracy would be that of the Multinomial NB, TVEC. This model improved our score from the baseline of 65.0% to 69.6%.

For our inquiry into brand differentiation using the best features/ estimators from our various models, main words that differentiate us from DoorDash seems to be "Plus Card" and "Quests", which seems like good anchors. We other word might be seasonal- "surge"s seem to be a good trend which our drivers enjoy.

For our enquiry into the general sentiments towards the two companies, both of us share the communities' concern towards time-related words, while our community can be differentiated from DoorDash's by the word "good". We will take note of this positive trend.

For further steps, We can do more textual analysis on the texts containing these differentiating words. The Words that are of importance in a particular time frame, and we will have to continuously measure these data to update our knowledge of our drivers and users, and our branding

---