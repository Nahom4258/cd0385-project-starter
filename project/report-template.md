# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I realised that I needed to check if there are any negative prediction values as Kaggle doesn't accept the negative prediction values. So, what I did was, I changed all the negative predictions to 0.

### What was the top ranked model that performed?
WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I added additional feature by splitting the datetime components all by themselves, making each datetime character an independant feature that affects the prediction of the model. I also changed the season and weather type to 'categorical'.

### How much better did your model preform after adding additional features and why do you think that is?
It did much better. And that's because I split the datetime components all by themselves. Making them each individual features. This gives the model more feature which makes the model predict better.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
It didn't improve it much. I rank the hyperparameter model 2nd after the 'datetime splitted model' and before the first model. Some hyperparameter configurations might have been good and some were bad for the model's prediction ability.

### If you were given more time with this dataset, where do you think you would spend more time?
I would definately spend more time on the hyperparameters and how I can try to tweak with them so that I can improve the model's prediction.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
model	hpo1	hpo2	hpo3	score
0	initial	default_vals	default_vals	default_vals	1.79941
1	add_features	default_vals	default_vals	default_vals	0.64211
2	hpo	GBM: num_leaves: lower=26, upper=66	NN: dropout_prob: 0.0, 0.5	GBM: num_boost_round: 100	0.48523

### Create a line plot showing the top model score for the three (or more) training runs during the project.
![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.
![model_test_score.png](img/model_test_score.png)

## Summary
In this project, I successfully applied the concepts covered in this unit of the course. Leveraging the skills acquired, I developed a machine learning regression model using the AutoGluon framework. This project was both challenging and rewarding, as it allowed me to put theory into practice and achieve a high Kaggle score. Overall, it was a valuable learning experience, and I feel more confident in my machine learning abilities as a result.