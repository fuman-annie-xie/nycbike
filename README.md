
# Final Project
### Machine Learning Foundations with Python (90-803)
#### Spring 2023
![Screen Shot 2024-03-11 at 6 48 39 PM](https://github.com/fuman-annie-xie/nycbike/assets/114703755/66144fad-aca4-466f-8cd7-775267a5d6a6)

### Title
Understanding User Demand and Vehicle Supply of New York Citi Bike Sharing 


### Authors

* Fuman (Annie) Xie, Jiaxuan (Alice) Ji 
* fumanx@andrew.cmu.edu, jiaxuanj@andrew.cmu.edu

### Project Description
Our project aims to gain insights into the New York City Citi Bikesharing service, focusing on three key aspects: user demand, user type, and vehicle type. With the rising popularity of shared bikes as a means of commuting, particularly in the post-Covid era, our project is interested in investigating user demand, taking into account weather conditions and user profiles. Additionally, we aim to examine the different types of users, including members and casual riders, as well as the usage of different types of bicycles, such as classic and electronic. Through our analysis, we hope to provide valuable insights to the Bikesharing service provider, which can inform future business decisions and service improvements.


**Key Words** bikesharing, user demand, user type prediction, electronic type classification

**Questions Summary** 

**Question 1: How to classify user type based on trip details, weather information, and demographical features?** To explore this question, we want to predict which category a biker falls into: casual users vs. members. Specifically, casual users may tend to use bike-sharing services in an occasional and infrequent basis, probably on weekends or holidays, while members who have purchased long-term membership may use Citibike services more frequently and regularly. We select predictors concerning many aspects such as weather, weekday/weekend and socioeconomic features. For socioeconomic conditions, we particularly focus on start station and examine features such as `car_free_commute`,`mean_travel_time_to_work`, `crime rate`. 

**Question 2: How to classify bike type based on trip details, weather information, and demographical features?** Citibike offers two types of bikes, electric and classic bike. Therefore, we build on the hypothesis that some users might prefer to use one type of bike than the other. For example, those who spend longer travel time to work might prefer to user electric bike as it could potentially save some labor work. Therefore, we user bicycle type as response variable, and utilize weather information and demographical information associated with certain neighborhood to make classification. 

**Question 3: How to predict demand based on peak hour, weekday, weather information?** To explore this question, we use the total number of trips as a response variable to characterize total demand. For predictors, we want to consider the weather patterns, if the day is a weekday or weekend, and if the trip is during peak hour. Considering that some stations tend to be more popular than the other, our next step would narrow down the scope to specific start station and predict the demand of this particular station based on weather, weekday, and peak hour. 



### Data Collection

You may download our dataset here: https://drive.google.com/file/d/1Oan8mSqrZHenywiMW1KC3WhpMPAy76DG/view?usp=share_link

This project investigates the **trip data from Citi Bike in New York City from March 2022 to Febuary 2023**. There are 31,941,199 trips in total. Each entry has the start/end time and station, whether the user chose an electric bike or a a classic bike, whether the user was a member or a casual rider. We extract the date and weekday information from the start time. To enrich our dataset, we merged **weather** dataset (temperature, windspeed, rainy or snowy) on the date. Since we don't have detailed information about the riders, we merged **demographics** from each community district (median household income, the proportion of people having car-free commute, the average time people spend on commute, etc.) based on the start station location to our dataset in hope that these demographics can provide at least some information about the riders.

（Citation: data source is obtained from Citi Bike System Data, see website here: https://citibikenyc.com/system-data)

### Running the Project / Getting Started

#### Package Installation  
If you don't have the xgboost package, please install it before you run the notebook.
You can try the two commands below.
- pip install xgboost
- conda install -c conda-forge py-xgboost

####  Github Branching Strategy 
In this group project, we have three research questions to answer, and have divide our branching strategy by different research questions, and both teammates clearly follows such a strategy. 

- 'classification_reg': this branch is featured as bicycle type predication model which mainly use classification. 'Reg' means that this is a regular research question (not the additional one). 

- 'regression': this branch is featured as user demand analysis, and most methods are regressions. 

- 'additional': this branch is featured as our additional research question with three additional models. 

#### Runing Project Guidline
We only have one jupyter notebook, which contains answer of all of three research questions. The outline for our notebook is below: 
- Exploratory Data Analysis 
- Using Regression to Predict User Demand (refered to above Problem Statement 3) 
- Using Classification to Classify Bicycle Type (refered to above Problem Statement 2)
- Additional Model: Using Classification to Classify User Type (refered to above Problem Statement 1) 

For each research question, you may approach our analysis by following sections, including data cleaning, feature engineering, model training and tuning, model validation (CV score), Model Performance (Test set report), and conclusion for individual research question. And then, you may find our overall conclusion and future work discussion. 
