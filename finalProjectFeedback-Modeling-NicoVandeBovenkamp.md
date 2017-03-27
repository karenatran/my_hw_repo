### ***Final Project - Modeling Analysis Feedback***

***Nico Van de Bovenkamp***
***

**Overall** Great work on this first stab at modeling! You are definitely moving along and grasping key concepts from the course! The next steps will be to define your subsequent models and then compare them to your earlier linear models. Also, I would recommend that you do a gridsearch over your Lasso and your Ridge models to test those out as well. The Random Forest will be interesting to test out too. In the next steps, think about how you want to visualize and represent your results (as well as the ways in which you evaluate your model). I put some notes below, but if you have some further questions, we can discuss them in class.

*Quick question to discuss later:* Why is it that you dropped time? I didn't fully understand it from the comment you made. Last time we spoke, I thought you wanted Time as a key independent variable in your analysis ('How much time should we be commited posting ads to get the best rate.")

**Some thoughts**

* **Train/Test Split and Defining Models** It looks like when you did your train test split, the `X` and `y` were not well defined, thus you only have two columns for some reason in your model? You should have all the columns in your dataset, less the `Rate` so you make use of all features!:
```python
# Well defined X and Y
X = df_join.drop('Rate',axis=1)
y = df_join[['Rate']]
# Then you should do train test split on all those columns:
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)
```
* **Model Evaluation** Great work on setting aside a particular error metric, and methodology, to use here! Note, however, that when you do your train test split, the purpose is to 'Test' your model on your test set. Thus, you should build a model on 'Train' and then evaluate it on 'Test' ie when measuring MSE:
```python
metrics.mean_squared_error(y_test, lm.predict(X_test))
```
* **Cross Validation/Gridsearch:** Nice work on that gridsearch! Gridsearch is a really handy tool for your hyper-parameter tuning across all models. Be sure to implement that when you bring in your Random Forrest Regressor. I noticed that you are often using just 5 fold validation. I recommend that you increase the folds. Given the number of instances you have, you will greatly reduce your model variance by increasing the number of folds. In the case of tree based models, as well as other non-linear models, this is key.
* **Random Forest:** Nice work with the modeling, and definitely try out a Random Forest Regressor! Warning though, typically a random forest 'out of the box' is going to over-fit a bit. I highly recommend you add in some hyper-parameters and perform a Grid Search (with the cross validation) and then evaluate that fit: **min-leaf-size and/or min-split-size, tree depth, and add estimators (you can probably add a couple hundred)!** [Check out this guide](https://www.analyticsvidhya.com/blog/2015/06/tuning-random-forest-model/).
* **Feature importance** In cases like these, you often want to walk away with a 'why' you get the best Rate from your features. One interesting way of visualizing that is by plotting the `feature_importance_` attribute of a Random Forest. [Check this out, and note that it works the same with Random Forest!](http://datascience.stackexchange.com/questions/13754/feature-importance-with-scikit-learn-random-forest-shows-very-high-standard-devi)
* **Plotting Results:** When you are plotting your model results, the linear fit of the predictions against circulation are quite nice, but there are many other ways to show that. One great one is to plot a KDE and then plot a KDE of your *predicted* Rate. Also, recall that you can always plot residuals and the MSE over various parameters/features to show how your model is (and is not) learning the data.
