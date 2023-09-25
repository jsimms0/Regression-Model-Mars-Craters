# Mars Crater Analysis
This project analyzes and visualizes the geographical distribution of Mars' craters, establishes correlations among various features of the craters, and develops a predictive model to estimate the depth of the craters based on other features.

## Skills Used
The following project demonstrates the following skills: Data Collection and Pre-processing, Exploratory Data Analysis, Feature Engineering, Data Splitting and Predictive Modeling (using linear regression, ridge regression, and gradient boosting regression), Model Evaluation (using MAE and R^2), Model Enhancement, Interactive Data Visualization (creating interactive dashboards), Correlation Analysis, and Results Interpretation and Communication.

## Project Summary
** Goals:**
1. Analyze and visualize the geographical distribution of Mars' craters, focusing on named craters.
2. Establish correlations among various features of the craters.
3. Develop a predictive model to estimate the depth of the craters based on other features.

## Key Steps:
** Data Collection and Pre-processing: **
* Acquired the Mars crater data, which included information about crater names, diameters, depths, and other related features.
* Cleaned the dataset by handling missing values and performing necessary transformations.

** Exploratory Data Analysis: **
* Plotted the geographical distribution of named craters on Mars, using `plotly` to visualize longitude vs. latitude.
* Examined the distribution of various categorical and integer features specific to named craters.

** Feature Engineering and Modelling: **
* Replaced blank spaces in the dataset with NaN for proper handling.
* Set up a data preprocessing pipeline that scaled numerical features and one-hot encoded categorical variables.
* Split the data into training and test sets.
* Trained a Linear Regression model to predict crater depth

** Model Enhancement: **
* Tested other models such as Ridge Regression and Gradient Boosting Regressor.
* Utilized GridSearchCV for hyperparameter tuning for both the models.
* Compared their performance to identify the best model based on the negative mean absolute error.

** Interactive Data Visualization: **
Created two interactive dashboards using `Dash`:
* Mars Crater Dashboard: Feature Comparison: This dashboard allows users to compare multiple features using a scatter matrix.
* Mars Crater Dashboard: Feature Filtering: This dashboard enables users to filter craters based on various features and view them on a scatter plot.

** Correlation Analysis: **
* Computed the correlation matrix to establish relationships between features.
* Visualized the correlations using a heat-map.
* Identified a moderately strong positive correlation between crater depth and diameter. 
* Identified a moderate positive correlation between crater depth and the number of layers.

## Results:
* The data was able to be effectively visualized to represent correlations between features, and see the geographical distribution of Mars Craters (see visuals below)
* Linear Regression, Ridge Regression, and Gradient Boosting Regressor were tested to develop a predictive model to estimate the craters depth
  * Linear Regression Model Results:
      * Best Score (Mean Absolute Error):  0.0567
      * R² Score: 0.629
  * Ridge Regression Model Results:
      * Best Parameters: alpha = 0.01, solver = 'auto'
      * Best Score (Mean Absolute Error): 0.0566
      * R² Score: 0.629
  * Gradient Boosting Regressor Results:
      * Best Parameters: learning_rate = 0.05, max_depth = 5, n_estimators = 200
      * Best Score (Mean Absolute Error): 0.0389
      * R² Score: 0.774
* The Gradient Boosting Regressor outperformed the Ridge Regression and Linear Regression models, achieving the highest R² score and the lowest mean absolute error
* The correlation analysis revealed key relationships, notably the correlation between crater depth and diameter, and crater depth and the number of layers.
* The interactive dashboards provided valuable insights into the distribution and relationships of Mars craters based on various features.

