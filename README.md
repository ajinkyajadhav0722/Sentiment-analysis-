Process:
Data Loading and Initial Exploration:

Loaded the dataset and checked its shape and feature names.
Identified and handled any missing values, specifically dropping rows with null values.
Data Cleaning and Preprocessing:

Added a new column to calculate the length of the reviews.
Explored the distribution of ratings and feedback, visualizing them using bar charts and pie charts.
Text Analysis and Visualization:

Generated a word cloud for all reviews, as well as separate word clouds for positive and negative reviews.
Text Processing:

Preprocessed the reviews by removing non-alphabetic characters, converting to lowercase, and applying stemming and stopword removal.
Converted the cleaned text data into numerical format using CountVectorizer.
Feature Scaling:

Applied MinMaxScaler to the feature set to normalize the data.
Model Building:

Random Forest Classifier:
Trained on the preprocessed data and achieved high accuracy.
Performed cross-validation to validate the model's performance.
Conducted hyperparameter tuning using GridSearchCV to identify the best model parameters.
XGBoost Classifier:
Trained and evaluated the model, saving the model using pickle for future use.
Decision Tree Classifier:
Trained and evaluated the model, with results displayed through a confusion matrix.
Saved the model using pickle.
