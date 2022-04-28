NYC Taxi Trip Duration
New York City’s 12,779 yellow medallion taxicabs comprise a $1.8 billion industry serving about 240 million passengers a year. Information on New York’s cabs attracts a broad audience due to their central transportation role and their prominence in Manhattan traffic. Exploiting an understanding of taxi trip durations and the ability to predict taxi durations could present valuable insights to city planners and the people of New York. Hence, this problem statement is of great significance.

The Kaggle competition named “New York City Taxi Trip Duration” consists of the 2016 NYC Yellow Cab trip record data, which was originally published by the NYC Taxi and Limousine Commission (TLC). This competition demands us to build a model that predicts the total ride duration of taxi trips in New York City. Thus, the problem statement is defined as follows: determine best predictors of NYC taxi trip durations, and build a multivariate taxi trip duration predictor.

![image](https://user-images.githubusercontent.com/66200786/165702179-2c51f77d-a062-4451-a698-bbd767a0acbf.png)



**Model Performance**

**Final Model: LightGBM model**

![image](https://user-images.githubusercontent.com/66200786/165720833-34a07bfe-494a-4f8c-9301-077360f611ff.png)


Result (Kaggle Public Leaderboard): RMSLE 0.44
![image](https://user-images.githubusercontent.com/66200786/165720462-37753c3f-0b0a-49a5-b644-4e831494f7f6.png)


**Team:**

1. Ganeshkumar Patel
2. Akanksha Agrawal
3. Yaman Saini
4. Sanjay Kumar
5. Saurabh Funde

#**Conclusion & Future Scope:**

**Conclusion:** In this project, we tried to predict the trip duration of a taxi in NYC. We took the information of pick up latitude, longitude and drop off latitude, longitude, along with some other fetures to get the distance of the trip. For our given dataset, LightGBM showed the best predictions of trip duration for a particular taxi.

**Future Scope:** There's always a room for the improvement and a lot more to explore

with newer feature creation,
using some other filters than used in this notebook accuracy may get improved
with target transformation.
