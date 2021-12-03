# Challenge Number 02
**Release Date:** 03-Dec-2021 10:00 PM GMT+8
**Time Duration:** 96 Hours (4 days)
**Level of Difficulty:** Intermediate
**Number of Items:** 7

Submit a jupyter notebook file (.ipynb) with your team name. Follow the format: **C2-UPDSS-[TEAM NAME].ipynb**. 
Example: `C2-UPDSS-Team Titans`. 
If a library is specifically indicated to be used, your code is restricted to be only using such. Otherwise, any library is allowed.

Any form of data pre-processing is allowed but one-hot encoding or other data augmentation techniques are strictly prohibited. The goal of this challenge is to yield the least root mean square error and/or the greatest R2 score. Thus, it is up to the team to do the necessary data pre-processing methods in order to achieve that goal.
Link to submission form: `https://forms.gle/GDc2NQWMdFqguqez9`

Maximum points that can be earned: `2500 points`
Point distribution 
- `2000 pts` accuracy of answers 
- `500 pts` punctuality/speed of submission

## Challenge Background
Download the dataset provided:
`https://drive.google.com/file/d/1PA6zcwXGcQxPZsaMBaQ273PKpwrBOju9/view?usp=sharing`

Your task is to investigate and analyze the difference between instance-based and model-based learning. In instance-based learning, the system learns the examples then generalizes to new cases by using a similarity measure to compare them to the learned examples. On the other hand, model-based learning generalizes from a set of examples by building a model of these examples, which would later on be used to make predictions.

In the dataset, your main task is to predict the final grade (G3) of the student’s Mathematics subject. As the task’s output or target variable, it is a numeric data with a range from 0 to 20.

The following contains the dataset’s metadata or information:
- `sex` - student’s sex (binary: F for female or M for male)
- `age` - student’s age (numeric: from 15 to 22)
- `address` - student’s home address type (binary: U for urban or R for rural)
- `famsize` - family size (binary: LE3 for less or equal to 3 or GT3 for greater than 3)
- `pstatus` - parent's cohabitation status (binary: T for living together or A for apart)
- `traveltime` - home to school travel time (numeric: 1 for less than 15 min., 2 for 15 to 30 min., 3 for 30 min. to 1 hour, or 4 for more than 1 hour)
- `studytime` - weekly study time (numeric: 1 for less than 2 hours, 2 for 2 to 5 hours, 3 for 5 to 10 hours, or 4 for more than 10 hours)
- `failures` - number of past class failures (numeric: n if n is greater than or equal to 1 but less than 3, else 4)
- `schoolsup` - extra educational support (binary: yes or no)
- `famsup` - family educational support (binary: yes or no)
- `paid` - extra paid classes within the course subject (binary: yes or no)
- `activities` - extracurricular activities (binary: yes or no)
- `nursery` - attended nursery school (binary: yes or no)
- `higher` - wants to take higher education (binary: yes or no)
- `internet` - Internet access at home (binary: yes or no)
- `romantic` - with a romantic relationship (binary: yes or no)
- `famrel` - quality of family relationships (numeric: from 1 meaning very bad to 5 meaning excellent)
- `freetime` - free time after school (numeric: from 1 meaning very low to 5 meaning very high)
- `goout` - going out with friends (numeric: from 1 meaning very low to 5 meaning very high)
- `Dalc` - workday alcohol consumption (numeric: from 1 meaning very low to 5 meaning very high)
- `Walc` - weekend alcohol consumption (numeric: from 1 meaning very low to 5 meaning very high)
- `health` - current health status (numeric: from 1 meaning very bad to 5 meaning very good)
- `absences` - number of school absences (numeric: from 0 to 93)
- `G1` - first period grade (numeric: from 0 to 20)
- `G2` - second period grade (numeric: from 0 to 20)

## Number 01: Exploratory Data Analysis `[300 pts]`
Plot and display the histograms of the following: G1, G2, and G3. Select gender as hues.

## Number 02: Model Building, Training, and Inference `[300 pts]`
- Shuffle the dataset first by doing the following: `df.sample(frac=1, random_state=42)`. Display the first 10 rows of the shuffled dataset.
- After that, split the data into train and test. Test size is `0.20`. Set the random state equal to `42`.

## Number 03:  Linear Regression `[400 pts]`
For model-based learning, use `sci-kit learn` `linear model` library and import `LinearRegression`. Report two metrics: root mean squared error and R2 score.

## Number 04:  Feature Importance (Linear Regression) `[150 pts]`
- Display the top five predictors (or attributes) with the highest weights.
- Customize the data frame such that the only attributes are these top five predictors.
- Train the model and predict the test values again. Did the RMSE and R2 scores improve? Compare the new weights of these top five predictors with respect to their old weights.

## Number 05: K-Nearest Neighbors Regressor `[400 pts]`
For instance-based learning, use `sci-kit learn` `neighbors` and import `KNeighborsRegressor`. Set the number of neighbors equal to `15`. Report two metrics: root mean squared error and R2 score.

## Number 06:  Hyperparameter Tuning (K-Neighbors Regressor) `[150 pts]`
Change the number of neighbors to 30, 45, and 60. Train the model and predict the test values again. Did the RMSE and R2 scores improve? Record and plot the metric scores (RMSE and R2 score) as the number of neighbors increased from 2 to 5.

## Number 07: Comparing the predicted and actual scores `[300 pts]`
- Plot the actual vs. predicted scores of the original linear regression model.
- Plot the actual vs. predicted scores of the original k-nearest neighbors regression model.
- Display these two plots (side-by-side or top-bottom). Which model yielded the best scores?
