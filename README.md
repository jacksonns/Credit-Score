<h1 align='center'> Credit Score Classification </h1>


## 1. Problem statement
You are working as a data scientist in a global finance company. Over the years, the company has collected basic bank details and gathered a lot of credit-related information. The management wants to build an intelligent system to segregate the people into credit score brackets to reduce the manual efforts.

**Task:** Given a person’s credit-related information, build a machine learning model that can classify the credit score. There are three possible classes: ```Good```, ```Standard``` and ```Poor```.


Data from https://www.kaggle.com/datasets/parisrohan/credit-score-classification


## 2. Solution strategy 

**2.1. Data Cleaning:** In this step, trailing characters were removed from numeric attributes to change colum type from object to numeric, some feature engineering was made to transform a categorical column into numeric and to extract two new features, and missing values were replaced by the mode of the values among the same customer.

**2.2. Exploratory Data Analysis:** This section consists of calculating descriptive statistics, visualizing data dispersion through boxplots, feature correlation through heatmap and categorical variables distributions through barplot. Outliers were detected and replaced by the mode of the values among the same customer (equivalent to the treatment for missing values).

**2.3. Data Preparation:** Irrelevant features were removed based on previous analysis, categorical attributes were One-hot encoded and the data was transformed using MinMax scaler.

**2.4. Feature Selection:** Using the MDI method, all selected features on the previous section were considered.

**2.5. Machine Learning:** Different machine learning algorithms were trained and evaluated through balanced accuracy, precision, recall and F1 metrics. Among all the four methods considered (Dummy Classification, Random Forest, XGBoost and Multinomial Logistic Regression), Random Forest had the best performance.

**2.6. Hyperparemeter Tuning:** Tuning hyperparameters for Random Forest Classifier, considering number of trees, maximum depth of tree,
minimum number of samples required to be at a leaf node and minimum number of samples required to split an internal node. The chosen method was Grid Search Cross-Validation.
