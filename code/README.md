# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

### Description

We are a team of analysts from Uber Eats, attempting to find out if there is brand differentiation between our platform and Door Dash, and what are the general trends in vernacular that our Uber Eats community, both drivers and users, are using.

These will seek to inform our marketing team about how we can bring out brand forward, and also our platform/product management team on how we can improve our services.

We will be using subreddit posts to find out what words differentiate us from our competitor, and which words are most commonly used amongst the communities.

We will explore various models to find out which is the most accurate, as being able to get the highest accuracy of identifying our competitor and our own will allow us to utilise the differentiating words well (these words are able to tell us and DoorDash apart).

Caveats: Throughout this document, there would be references to DD and UE, which are the acronyms for DoorDash and Uber Eats respectively. This will be even more commonly used when labelling our data.


#### About the API

Data has been scraped using this API: https://github.com/pushshift/api
And our Subreddits are UberEATS and doordash 

---

### Analysis

We went through several models to attempt to find out whether there are differences between us and the competitor, and if so, what are the words that differentiate us. The models we used to check are the MultiNomial Naive Bayes model, with both CVEC and TVEC, and Random Forest with Extra Trees. 

To find out the dominant vernacular of the period, we did a count of top bigrams and singular words.

---

## Conclusions, Recommendations:

Our best model for accuracy would be that of the Multinomial NB, TVEC. This model improved our score from the baseline of 65.0% to 69.6%.

For our inquiry into brand differentiation using the best features/ estimators from our various models, main words that differentiate us from DoorDash seems to be "Plus Card" and "Quests", which seems like good anchors. We other word might be seasonal- "surge"s seem to be a good trend which our drivers enjoy.

For our enquiry into the general sentiments towards the two companies, both of us share the communities' concern towards time-related words, while our community can be differentiated from DoorDash's by the word "good". We will take note of this positive trend.

For further steps, We can do more textual analysis on the texts containing these differentiating words. The Words that are of importance in a particular time frame, and we will have to continuously measure these data to update our knowledge of our drivers and users, and our branding

---