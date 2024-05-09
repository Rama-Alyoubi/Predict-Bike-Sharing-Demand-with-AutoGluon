# Report: Predict Bike Sharing Demand with AutoGluon Solution
Rama Alyoubi

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
When I tried to submit my predictions, I noticed that some of the numbers were negative, which isn't possible for counting bikes. So, I changed all the negative numbers to zero before submitting.

### What was the top ranked model that performed?
The best model was : "WeightedEnsemble_L3"

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
During the exploratory analysis, I looked at how different conditions like temperature, humidity, and windspeed might affect bike rentals. I noticed that adding features like the hour, day, month, and day of the week extracted from the datetime column might help improve predictions. By including these, the model could better understand and predict the demand for bikes at different times and conditions.

### How much better did your model preform after adding additional features and why do you think that is?
After adding additional features such as hour, day, month, and day of the week to the model, the performance improved significantly. The root mean squared error (RMSE) decreased from -53.135606 to -30.333932. This improvement is likely due to the model's enhanced ability to capture more complex patterns and trends in the data.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
After adjusting the settings of the model, it performed much better on the test data, showing lower scores, which means it did better. Even though the local tests seemed a bit worse, the real results on Kaggle showed that the changes I made were effective. This taught me that fine-tuning the model settings is really important for getting good results in real situations.

### If you were given more time with this dataset, where do you think you would spend more time?
If I had more time with this dataset, I would focus on expanding feature engineering to explore new interactions and potential features. I'd also experiment with different machine learning models and advanced techniques to enhance the model's accuracy. Further, I'd dedicate effort to fine-tuning the hyperparameters systematically to optimize performance. Lastly, understanding which features most significantly impact predictions would be valuable, helping to provide deeper insights beyond just model improvements.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default|default|default|1.80541|
|add_features|default|default|default|0.62215|
|hpo|'RF': {'n_estimators': 300}|GBM': {'num_boost_round': 100}|GBM': {'num_boost_round': 200}|0.47943|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
