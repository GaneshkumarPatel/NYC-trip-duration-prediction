
![image](https://user-images.githubusercontent.com/66200786/165702179-2c51f77d-a062-4451-a698-bbd767a0acbf.png)


# NYC-Taxi-Trip-Time-Prediction

New York City, with a relatively large number of populations and busy streets require taxi with some good algorithms to move from one place to another without any delay. A lot of streets and roads in New York city are quite busy due to traffic jams, construction or road blockage etc. Therefore, it is very important to **predict the trip duration** of taxi so that the user will know how much time it will take to commute from one place to other. 

## Problem Statement

* Task is to predict total ride duration of taxi trips in New York City.
* Independent Features :
* id : a unique identifier for each trip.
* vendor_id : a code indicating the provider associated with the trip record.
* pickup_datetime : date and time when the meter was engaged.
* dropoff_datetime : date and time when the meter was disengaged.
* passenger_count : the number of passengers in the vehicle (driver entered value).
* pickup_longitude : the longitude where the meter was engaged.
* pickup_latitude : the latitude where the meter was engaged.
* dropoff_longitude : the longitude where the meter was disengaged.
* dropoff_latitude : the latitude where the meter was disengaged.
* store_and_fwd_flag : This flag indicates whether the trip record was held in vehicle. 
* Target Feature :
* trip_duration : duration of the trip in seconds.

In this project, through our exhaustive analysis and feature engineering we have trained the model to predict the value of trip duration using various models such as Linear Regression, Random Forest, XG Boost and Light GBM. We started with **understanding the problem statement and studying the dataset**. We found to have approx. 14 lakhs of observations but only 11 features. 

Thereafter, **exploratory data analysis** was performed by closely looking and understanding each of the given features. The extracted features were found to have close relation with trip duration and thus they were of great importance. 

![image](https://user-images.githubusercontent.com/98693201/165889199-a1d75bb1-0fbd-4145-9c59-a385cba58245.png)       ![image](https://user-images.githubusercontent.com/98693201/164925633-6805a1fe-63b6-4567-a332-e311c42beb3a.png)


As **feature engineering** is the main task to be performed while modelling any dataset, therefore we created a new feature distance with help of pickup and dropoff latitude and longitude using distance formula. After completing feature engineering, we plotted distance and trip duration we found to have cone shaped graph but with lots of error.

![image](https://user-images.githubusercontent.com/98693201/164917486-858694fa-9b30-4448-a099-b6d6b3072ab2.png)

![image](https://user-images.githubusercontent.com/98693201/164927390-938c89ef-5bf3-4b6a-9d2b-300126f33390.png)

Further we chose features passenger_count, pickup_longitude, pickup_latitude,dropoff_longitude, dropoff_latitude, store_and_fwd_flag, pickup_month,pickup_tps,pickup_dayn, pickup_timeofday, and distance for **training our models**. Initially we looked at the baseline scores and then we performed Random Forest regressor, XGBoost Regressor and finally LightGBM. After training these models, **LightGBM showed the best score of 81.1% on test data** and therefore we performed hyperparameter tuning using random search cross validation technique to further tune our model, but couldn’t achieved the score better than this.

![image](https://user-images.githubusercontent.com/98693201/164929141-69d14bc5-2aa8-4277-b69a-2a2357a8aced.png)

Lastly, we **studied our model using SHAP** and found that feature: distance is creating maximum impact on our output: trip duration. We also performed a check on Kaggle to check the authenticity    of our model and scored 0.46. Thus, after creating our model we are ready to predict the trip duration with the provided features in dataset. In future we can improve the score by performing more feature and engineering and hyperparameter tuning.

![image](https://user-images.githubusercontent.com/98693201/164931449-b4717888-4b5a-4022-8a6d-91d9102df677.png)   ![image](https://user-images.githubusercontent.com/98693201/164931746-8f59a80c-2d63-45f0-848a-aabf01518a73.png)

### **Conclusion:** 

In this project, we tried to predict the trip duration of a taxi in NYC. We took the information of pick up latitude, longitude and drop off latitude, longitude, along with some other fetures to get the distance of the trip. For our given dataset, LightGBM showed the best predictions of trip duration for a particular taxi.

### **Future Scope**: 

There's always a room for the improvement and a lot more to explore

with newer feature creation,
using some other filters than used in this notebook accuracy may get improved
with target transformation.

**Team:**

1. Ganeshkumar Patel
2. Akanksha Agrawal
3. Yaman Saini
4. Sanjay Kumar
5. Saurabh Funde

### **References-** 

*   https://link.springer.com/article/10.1007/s13198-021-01130-x
*   https://www.kaggle.com/competitions/nyc-taxi-trip-duration/overview
