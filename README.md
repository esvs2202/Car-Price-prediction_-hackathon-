This project is part of "MATHCO.THON" Data scientist hiring hackathon conducted by The Math Company and Machinehack.com 
url:https://machinehack.com/hackathons/data_hack_mathcothon_car_price_prediction_challenge/overview-

Problem Statement:
---------------------------------------------------------------------------------
With the rise in the variety of cars with differentiated capabilities and features such as model, 
production year, category, brand, fuel type, engine volume, mileage, cylinders, colour, airbags and many more, 
we are bringing a car price prediction challenge for all. We all aspire to own a car within budget with the best features available. 
To solve the price problem we have created a dataset of 19237 for the training dataset and 8245 for the test dataset.

Brief summary of the Solution implemented:
----------------------------------------------------------------------------------
1. Loaded the train data set and did basic data cleaning and feature engineering.
2. Having more number of categorical features, used LabelEncoder() method from sklearn.(can be accessed through "from sklearn.preprocessing import LabelEncoder".
3. Visualized all the columns using both histogram and boxplot to check the presence of outliers and did outlier treatment using "Interquartile range method" or IQR method.
4. Visualized the correlation among all the features, dropped the one feature "Cylinders" which has more positive correlation with the "Engine volume" column and the latter one 
    is enough to explain the importance of the feature.
5. Built a linear regression model, during the residual analysis found that Linear regression assumptions are not completely followed. The R2 scores of both the train and test
    data are very low i.e, in the range of 12-13% and the root mean squared log error (RMSLE) of both the train and test data are in the range of 17-18% respectively.
6. As per the residual analysis, the linear regression model is not a best choice to do solve this multivariate regression problem. Hence, tried with Decision tree regressor
    algorithm.
7. After experimenting with all the hyperparameters, got this combo (max_depth = 20, min_samples_leaf = 5, criterion = 'friedman_mse'), with which we got an R2 scores of both
    the train and test data are  94% and the root mean squared log error (RMSLE) of both the train and test data are in the range of 4% respectively. 
8. Saved the model to local disk using joblib library.
9. Then loaded the actual test data, did similar data cleaning and feature engineering, and made predictions using the decision tree regressor model that we built on the training 
    data.

Indeed, it's a challenging hackathon, but gained a beautiful knowledge on automobile industry and enabled me to brush up my concepts on the statistics. 

Please go through my notebook to understand my complete solution and kindly let me know the feedback so that I can make changes to the solution to make it even better 
😊😊😊
