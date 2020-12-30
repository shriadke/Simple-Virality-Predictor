# Simple-Virality-Predictor

This projects showcases a simple approach to predict the virality of the post based on its text. The dataset used here has given the post along with its user interactions. The task here is to predict the virality score that a new post can achieve.

Considering the scope of the task is open to changes, I have assumed the output prediction can be continuous (regression analysis) or it will be a discrete label(classification). In this case, we can have two different approaches to prepare data as well as selecting the features. Also, the models and evaluation metrics used for both will be different. Overall, the final data frame considered has article text, title and language corresponding to the virality score or the label (viral, not viral) depending upon the approach.

* ***Features used:*** For the classification problem, word vector frequency is used as a feature and bag of words is formed. For each title-text combination. On the other hand, for regression model , data was converted to numerical form with the help of following features: number of words in title, number of words in actual text, number of distinct words in text, average word length in text, and stop token ratio. Based on prior analysis I considered these features.

* ***Models:*** The classification is done using random forest classifier model which gave highest accuracy of 70% (accuracy varied between 60-70% for different trials) and can be improved further by changing the labels from binary to multi-class format. For regression, XGBoost trees are used. The gblinear boosted tree gives the lower RMSE and thus we can select that one for further baseline.

* ***Evaluation Metrics:*** In classification problem, Classification accuracy, F1-Score, and the confusion matrix are the main evaluation metrics. While in regression, MSE, RMSE is the best evaluation metric available.

* ***Future Scope:*** The main change I would like to see is fixing the solution approach i.e. whether classification or regression. Thus, afterwards improving data and labels based on the approach, I can fine tune current models. Furthermore, I would like to try various other GBM, regression techniques and also would like to consider standard sentiment analysis techniques for this problem. In the end, the ensemble of various techniques will be something interesting to be carried out.
