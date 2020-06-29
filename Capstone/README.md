# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Capstone Project: Airline Topic Modelling

## Gabriel Choo, SG DSI 14

## Problem Statement

Airlines deal with large volumes of unstructured text every day. How can airline leverage on topic modelling to automatically segregate reviews to respective departments so that the departments can execute next call to action in a timely manner?

## Executive Summary

**Exploratory Data Analysis**

The overall ratings is a sentiment of how the user perceived the overall quality in terms of service and attitude of the respective airlines. Looking at the mean overall rating per year as a whole, we can see that the ratings has slid drastically since 2011. This doesn't show positivity as it could mean that the overall standards of the airlines has dropped, else the expectations of the users has increased. The charts shows that this applies to the rest of the ratings including comfort, seats, entertainment and meals.

Singapore airline is ranked one of the top airlines in the world. However according to the charts, it shows that the mean overall rating has dropped from a high score of 8 in 2013 to a score of less than 6 in 2020.

Despite the mean overall rating as a whole is on a slide, but ANA All Nippon Airways showed otherwise. Hence it's important to segregate the reviews into various departments to understand which areas need improvements or require next call of action.


**Modelling**

Latent Semantic Analysis (LSA), TF-IDF, Doc2Vec and Word2Vec are techniques used to vectorize the data before feeding into Logistic Regression for modelling.
TF-IDF and Logistic Regression has shown to be the best performing model at an overall accuracy of 93.9%, with AUC ROC score of 92.5%.

## Conclusions & Recommendations

By automating the topic labelling, we can actually eliminate human errors made on wrong labelling by the staff or consumers. For example, when an online form is used, sometimes consumers don't really understand which specific department their questions or review falls under hence there is a high chance choosing the wrong label. Secondly, some manual labor costs can be saved as sieving out reviews requires manpower. Lastly, if there is any necessary next call of actions, it will be done more timely as the reviews is automatically segregated straight to the respective departments.  


### Considerations

There are some considerations to take note of, firstly, the current model is build in a general way. Meaning the number of topics is limited at 3 and it's targeting some specific topics (departments) like airline operations, passenger services and in-flight experience. In order to expand the number of topics, more data from different sources like social media, online forms can be collected to do topic labelling and train classification models to predict the text. Lastly, we could even do more in-depth segregations of topics to enhance the efficiency.

### References

**Data**
- [Skytrax reviews: github](https://github.com/quankiquanki/skytrax-reviews-dataset)
- [Skytrax reviews: Kaggle](https://www.kaggle.com/efehandanisman/skytrax-airline-reviews)
- [Skytrax reviews: Scraped](https://www.airlinequality.com/review-pages/a-z-airline-reviews/)

**Data dictionary**


|Feature|Type|Description|
| --- | --- | --- |
|**airline_name**|*obj*|airline name|
|**author**|*obj*|name of user|
|**date**|*datetime*|date of review|
|**content**|*obj*|text review|
|**type_traveller**|*obj*| type of traveller|
|**cabin_flown**|*obj*| class of travel|
|**overall_rating**|*int*| overall rating with rating of 1-10|
|**seat_comfort_rating**|*int*| seat comfort with rating of 1-5|
|**cabin_staff_rating**|*int*|cabin staff rating with rating of 1-5|
|**food_beverages_rating**|*int*|meals onboard with rating of 1-5|
|**inflight_entertainment_rating**|*int*|inflight entertainment with rating of 1-5|
|**ground_service_rating**|*int*|ground service with rating of 1-5|
|**value_money_rating**|*int*|value for money with rating of 1-5|
|**recommended**|*int*|Whether the user recommend the airline|
|**hubs**|*obj*|The hubs of the airline|
|**country**|*obj*|The country airline located|
