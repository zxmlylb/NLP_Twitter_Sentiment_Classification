# NLP_Twitter_Sentiment_Classification
Statistical Learning Project RandomForest

The research question we want to address using random forest is: Can I predict whether the coronavirus tweets considered extremely positive or extremely negative. This question is important, because it allows for the detection of extremely negative and flamatory tweets that are related to coronavirus and help caution the public about the validity of such tweets in getting information about covid. A random forest is practically meaningful because it mimics the human cognitive process and behavior of speaking on tweeter.

For example, certain negative tweets would be very likely to include certain words that best categarizes the sentiments, and thus using a decision tree to predict the sentiment help identify which words best distinguish between the positive and negative sentiment by making splits in the trees. 

The Random Forest Model
After final data manipulation, we can finally train random forest model. The model is trained using the caret library, which allows us to select the model and its tuning parameters in an easy fashion. We decide to evaluate our model using specificity and false discovery rate. In our sentiment classification scenario, specificity measures how well our model can identify positive emotion tweets and false discovery rate measure our model’s performance on classifying negative emotion tweets.Finally, we also added a computational time parameter as we want to train our model within a reasonable time. So, eventually we want our classification random forest to have high specificity, low false discovery rate and reasonable computation time. Considering the number of words in a given tweets in trimmed after our pre-process, we decide to limit our mtry value range from 1 to 20 and our minimum node size from 1 to 5.

We selected “ranger” package to implement the random forest algorithm. The “ranger” method allows us to tune three model parameters mtry, splitrule, and minimum node size. The mtry parameter allow us to determine the number of randomly selected predictors in each tree. The minimum node size allow us to determine the complexity of each individual tree and we fixed the split rule parameter for classification to “gini”.

<img width="680" alt="Screen Shot 2022-01-15 at 11 41 42 PM" src="https://user-images.githubusercontent.com/93837295/149647542-e60075c9-463d-4c35-9d6b-23e1991cd91c.png">

<img width="706" alt="Screen Shot 2022-01-15 at 11 41 59 PM" src="https://user-images.githubusercontent.com/93837295/149647549-6a472ecf-112f-4437-8cb8-b446c7aee75c.png">
