# Linear Regression - Diabetes 

Linear regression on diabetes data set from Scikit-learn with regularisation (Ridge, Lasso, Net Elastic Regression)

## Data

The data set is composed of baseline variables, age, sex, body mass index, average blood
pressure, and six blood serum measurements for each of n =442 diabetes patients, 
as well as the response of interest, a quantitative measure of disease progression one year after baseline.

## Feature scaling

Feature scaling has already been done on the source data. All features are mean centered and scaled by the standard 
deviation times the square root of

## Models

 Five different models are created and trained on the dataset:
 
- A uni-variate linear regression model using bmi as the sole feature 
- A multiple linear regression using all 10 features, without regularization
- A multiple linear regression using all 10 features, with Ridge regularization
- A multiple linear regression using all 10 features, with Lasso regularization
- A multiple linear regression using all 10 features, with Net Elastic Regression

## Model performance

The performances of all models are evaluated using the Coefficient of Determination (R^2 score)

10-fold cross validation is performed on all models and the mean R^2 score is taken as the
measure of performance. For models with regularisation GirdSearchCV method is used 
to find the best values of the regularisation parameter (alpha) and l1_ratio (in the case of Net 
Elastic Regression model). 

The multiple linear regression model with Lasso regularisation and Net Elastic Regression models show the best performance 
with a mean R^2 score of 0.465 (l1_ratio is equal to one) followed by 0.464 for Ridge regularisation, 0.462 for multiple 
linear regression model with no regularisation and 0.302 for univariate linear regression model. 