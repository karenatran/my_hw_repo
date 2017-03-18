### ***Project 4 Feedback***

***Nico Van de Bovenkamp***
***

**Overall:** Nice work on this final notebook! Your discussion and write up is very thorough, and to the point, which will pay off when you are doing this for your final project. Also, nice work on imputing the mean, that is definitely good practice (if the mean does not significantly shift/skew the distribution).

**Some thoughts:** In this final notebook, which is similar to how you want to walk through your final project, you should walk through how and why you constructed and chose the model that you did. For example, explaining why you use a logit model, if/why you used regularization, what error metric you used, etc. Finally, given you used Statsmodels API, you could talk about the statistical significance (p-values) for each coefficient (feature, in Machine Learning). ***As always, try out many different models, which you note at the end there!***

**Other Visualizations:** In your final presentation, it is often hard to find the best way to show your results. Sometimes, it is in just bits of code or sudo-code, but often we want clean images and visualizations. The predicted probabilities (which works in the case of classification) across several values provided are one fantastic way of conveying results. However, think back to the lectures were we show learning curves, ROC curves, and discuss many error metrics. Showing those error metrics, and some visualizations of how you control or tune models to impact an evaluation metric is key! Think about this for your final project.

***A Table of Key Evaluation Metrics and Visuals:***

*Below is a brief set of many ways you can communicate/measure results that will be useful for your final project. Please let me know if you have any questions!*

| Metrics | |
|--- | --- |
| *Classification* | Accuracy, Precision, Recall, AUC Score, Lift, F-Score, Log-Loss, Gini, Entropy/Information Gain, Statistical Significance (p-value) |
| *Regression* | Mean Squared Error, Mean Absolute Error, Log-Likelihood Estimation, Statistical Significance (p-value) |

| Visualizations | |
|--- | --- |
| *Model Tuning* | Learning Curves, Regularization Learning Paths with an Error Metric, Model Error stepwise increasing feature set size |
| *Classification* | ROC Curve, Feature Importance Charts, Lift Curves, Expected Value Plots |
| *Regression* | Residual plots(!), KDE and KDE of Predicted Values, Expected Value |
