# Wine-Classifiation

**Wine Quality Classification Code Analysis**



**Summary**

This Python code aims to predict wine quality using several machine learning models (Linear Regression, Logistic Regression, Random Forest Classifier, and Multi-Layer Perceptron Classifier). The models are trained based on several wine characteristics, including Fixed acidity, Volatile acidity, Citric acid, Residual sugar, Chlorides, Free sulfur dioxide, Total sulfur dioxide, Density, pH, Sulfates, and Alcohol.

------------------------------------------------------------------------------------------------------------------

**Step by Step Overview:**

Environment Setup: 
First, it installs necessary Python packages NumPy and scikit-learn, and imports other required libraries and functions.

Data Uploading and Reading: 
It then automatically retrieves the 'winequality-red.csv' file from the Google Colab library (for first time users, you need to upload the file manually in the “Files” tab first. After retrieving the file, it converts it into the pandas DataFrame variable named ‘wine.’ To evaluate that the dataset was imported correctly, it displays the first five rows of the dataset.

Data Exploration: 
The first few rows of the DataFrame are printed, followed by a check for missing values. Then, it visualizes the distribution of the 'quality' variable using a count plot and creates bar plots to show the relationships between 'quality' and 'volatile acidity' and 'alcohol'. A correlation heatmap is also generated to understand the relationships between distinctive features.

Feature Preparation: 
It then separates the input features and target variable ‘quality.’ The input features are standardized, which helps to improve the machine learning models' performance. Any wine with a quality score of 7 or higher is classified as 'peak quality' (1), and the rest as 'poor quality' (0).



Data Splitting: 
It then splits the data into training and testing sets, with 80% of the data used for training and the remaining 20% used for testing.

------------------------------------------------------------------------------------------------------------------

**Model Building, Training, Evaluation, and Prediction:**

Four different machine learning models (Linear Regression, Logistic Regression, Random Forest Classifier, and MLP Classifier) are trained on the training data and evaluated on the test data. The accuracy of each model is printed, along with the model's weights and bias. For Logistic Regression, RandomForest, and MLP, it also prints a classification report and a confusion matrix for both the training and testing sets.

Linear Regression: It builds and trains a linear regression model, calculates the accuracy score on the test set, and displays the weights (coefficients) and bias (intercept) of the model.

Logistic Regression: Similarly, it builds and trains a logistic regression model, and calculates the accuracy score. Additionally, it performs in-sample validation by predicting both on training and test sets and evaluating the performance using classification metrics (precision, recall) and confusion matrices.

Random Forest Classifier: It then applies the Random Forest Classifier model to the data, predicts on the test set, calculates the accuracy, and evaluates the model using the classification report.

Multi-Layer Perceptron (MLP) Classifier: The script also uses a Multi-Layer Perceptron Classifier with a maximum of 1000 iterations, predicts on the test set, and evaluates the model using the classification report.

------------------------------------------------------------------------------------------------------------------

**Results:**

Linear Regression: 
Accuracy: 25%
[ 3.82599382e-02 -1.72451012e-01 1.21607472e-01 3.11841975e-02 -6.75218942e-01 -2.82438201e-04 -8.31753076e-04 3.92475224e+01 8.06682245e-02 3.32728860e-01 7.02569385e-02]
Bias: [37.80]


Logistic Regression: 
Accuracy: 93%
Weights: [[-0.02156077 -2.84550084 0.03079697 0.11003986 -1.54769821 0.01937214 -0.0186238 -1.36903285 -2.17154586 2.01494187 0.88489152]]
Bias: [-2.41383229]

Random Forest Classifier: 
Accuracy: 92.8%

Multi-Layer Perceptron (MLP) Classifier: 
Accuracy: 90%

------------------------------------------------------------------------------------------------------------------

**User Interaction for Wine Quality Testing:**
After the models are trained and evaluated, the script enters a while loop where it interacts with the user to input their wine's characteristics and uses the Random Forest Classifier model to predict the quality of their wine. The user has the option to assess another wine or exit the program.


