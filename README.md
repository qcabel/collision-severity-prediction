# Severity prediction of traffic accident in the City of Seattle 

This project aimed at predicting collision severity based on a dataset hosted by the City of Seattle. In particular, the collisions with only property damage are labeled as less severe accidents; the ones involving injuries are deemed as severe. The dataset consists of features such as environmental conditions (<em>e.g.</em>, weather, road condition, and lighting condition), time of the accident, location information (<em>e.g.</em>, type of road), as well as the number of people and vehicles involved. Some of these factors, such as the number of cyclists in the recorded accidents, tend to be obvious features in predicting the severity of the collision, whereas some may be inevident (<em>e.g.</em>, particular road region) but bearing important insights into mitigating the severity of traffic accidents for the city.  

---
## Data
* Severity level of the collision: 
    1. property damage only; 
    2. with injury
* Three types of heuristical code (collision type, SDOT/state assigned code) used to describe the accident
* Other descriptive features
    * Categorical features, such as weather, road conditions
    * Number of people/vehicles involved in the collision
    * Time of the collision
    * Location features, such exact location or address/junction type

## Model
* Tree models to predict the severity level of the accidents
    * Decision tree, 
    * random forest, 
    * xgboost, 
    * catboost
* Model complexity, early stopping - cross validation, hyperparameter tuning

## Highlights
What would lead to more severe collision?
* About 1/3 of all collisions are collisions with injury
* Accidents involving pedestrian or cyclist are more likely to be severe with injury
    * A certain lane segments tend to involve more cyclists in collision, which requires further investigations
* Left turn and angled collision is more likely to cause injury
* Severe accidents tend to happen at intersection
* Raining/wet road slightly elevates the probability of more severe accidents
* The latitude matters more in predicting severe collision (Seattle is bounded by water along longitude)