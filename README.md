Income classifier

This repos contains my machine learning model which classifies census data to predict whether an individual makes at least $50,000. Answering these types of question is important because our model predictions can help us understand our customer base which means we can improve a campaign or process and better target the population.

There are 2 main files in this repo. A Jupyter Notebook and a .py script.

The jupyter notebook is used to visually explore the data and build the model while the .py script is a 1 shot application that builds the final model and saves it automatically.

This is a high level overview of the building/design process

In the Jupyter Notebook: 
1. I explore the data and features to visually understand them and get a feel for what I'm working on.
2. I apply a log transformation to some of the data that is heavily skewed, this helps our model perform better.
3. I normalize numerical features. This is to ensure that each numerical feature is treated equally (for example: if column A is between 1 and 1,000,000 but column B is between 1-5, the model might add unreasonable weight and focus on column A because the numbers are larger. Normalizing the features solves this issue.
4. I one-hot-encode categorical features in order to use them in my model. This allows us to use numerical and categorical information together: for example, we can use someone's Age and his Job to help us with our prediction.
5. I ran 3 different types of classifiers (Decision Tree Classifier, Bagging Classifier and Random Forest CLassifier) and I ended up choosing the best one for tuning.
6. Once I chose the best performing model with the default values, I ran a grid-search which is an optimization technique aimed at improving the accuracy and f-score of my chosen model, the Random Forest.
7. Finally, a graph showing importance of each feature  is displayed. This graph can help us understand and explain to others which features are the most important. In our case, the capital-gain information, the marital status and the age of the individual helped account for to 40% of the importance of our features.

Henry
