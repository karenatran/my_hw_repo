### ***Final Project - Exploratory Analysis Feedback***

***Nico Van de Bovenkamp***
***

**Overall:** Good job on the set up of the project! Getting data from work definitely helps with the background knowledge and set up for your problem.

**Analysis Structure going forward:** Moving on, you will have to work on setting up your problem. As we discussed, you are going to want to dummify all of your categorical variables (Ad size, Web Domain, Device, etc.). And you will prepare your test and training set. Then, you will fit that matrix onto your regression output, Rate. As I mentioned, if you think about all those dependent variables you choose, *Time* is one of them.


**Some notes and thoughts:**

* **Scaling Data:** We discussed this earlier, but check out the [Standard Scaler](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html) package. The Standard Scaler will scale all numerical data, which will allow for some easier computation and more efficient computation. This part can actually be quite critical for distance based functions and SVMs.
* **Feature Importance:** One nice feature of random forests, is the ability to use, and then plot, the `.feature_importance_` of each feature (usually calculated via lowest entropy or gini coeffient). In These types of *why and what factors influence [blank]* problems, the prediction power of a feature can be very handy!
* **Plotting and Evaluation:** In your case, you will be using some regression model to find the impression rate. Thus, you should model via Mean Squared Error (or Log-Likelihood), and then you can plot in many ways! You can plot residuals (very key), KDE (distributions) of the actual Rate and Predicted Rate, and you can even compute expected values if you have the associated cost of advertising for a certain amount of time, device, size, etc.!

***A Table of Key Evaluation Metrics and Visuals:***

*Throwing this in here too! Below is a brief set of many ways you can communicate/measure results that will be useful for your final project. Please let me know if you have any questions!*

| Metrics | |
|--- | --- |
| *Classification* | Accuracy, Precision, Recall, AUC Score, Lift, F-Score, Log-Loss, Gini, Entropy/Information Gain, Statistical Significance (p-value) |
| *Regression* | Mean Squared Error, Mean Absolute Error, Log-Likelihood Estimation, Statistical Significance (p-value) |

| Visualizations | |
|--- | --- |
| *Model Tuning* | Learning Curves, Regularization Learning Paths with an Error Metric, Model Error stepwise increasing feature set size |
| *Classification* | ROC Curve, Feature Importance Charts, Lift Curves, Expected Value Plots |
| *Regression* | Residual plots(!), KDE and KDE of Predicted Values, Expected Value |
