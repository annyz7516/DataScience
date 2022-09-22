# Replective Report - Portfolio_4
## The process of solving problems and learning to use notebooks
In Portfolio_4 I was trying to explore using data science models in the field of medical diagnostics.

This dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases.

The data is provided as a CSV file, downloaded from [here](https://www.kaggle.com/datasets/mathchi/diabetes-data-set/download).

The objective is to predict based on diagnostic measurements whether a patient has diabetes.

### Step 1. Explore Data
At first glance, this dataset is clean without any missing data for each feature according to data information, and all data types are numerical.

After visualization of the numerical data distribution, we observed '0' values for some features, e.g. Glucose, BloodPressure, Skin Thickness, Insulin and BMI in distribution plots.

Based on common sense and some basic medical knowledge, '0' for those features is impossible, which can be proved by the their abnormal density in distribution plots. So those value '0' may refer to zero record instead of the actual measured value. They are outliers in this case.

### Step 2. Clean Data
Remove outliers Remove rows with '0' value of either Glucose, BloodPressure, Skin Thickness, Insulin or BMI.

Data Normalization Because actual measured values for different features are on drastically different scales, the feature with the larger scale may completely dominate the other, where normalization is necessary. Here, we used min-max normalization method.

Change data type into float After normalization all data will be between 0 and 1, which is float datatype, which do not able to fit data type in original dataset. So before normalization, convert datatype of those column is a must.

### Step 3. Select and Train Models
So, what model should we use?

What we are trying to predict is whether or not a patient has diabetes ——"is 'Outcome' yes or no？". 'Outcome' is the label, supervised learning algorithms can be used to deal with this sort of problems —— probabilistic statistical classification.

tried logistic regression model first
tried KNN model then
train two models separately
### Step 4. Evaluation of Models
Evaluation of logistic regression model
accuracy score gives a score for the proportion correct
confusion matrix shows
use REF to select features
Evaluation of KNN classifier
accuracy score gives a score for the proportion correct
Cross Validation (CV) method to tun the hyperparameter 𝐾
GridSearchCV to find the best 𝐾
## Discussion
### From this unit, I have learned some of the tools that data scientist use.
using Python language to code for data science and machine learning models
fundamental Python Libraries: Pandas,Python Data Analysis Library, SCIKIT-Learn, Machine learning library, NumPy and SciPy for numeric and scientific computation, Matplotlib and Seaborn for visualization.
Web Integrated Development Environment (WIDE): Jupyter
Github, the website and cloud-based service that helps developers store and manage their code, as well as track and control changes to their code.
### What can these toolboxes be used in the future?
With these toolboxes, dataset can be easily transformed in the way we want, by reshaping it, adding or removing columns or rows; we can create static and visulize data, thus have a depth understanding of a dataset; common tasks in data analysis, such as classification, regression, clustering, dimensionality reduction, model selection and preprocessing, can be done with simple and efficient tools provided by machine learning libraries in Python.

### Why I choose Diabetes dataset?
this dataset has good size, not to big to load.
to compare two different classes of supervised models, classification, and regression analysis, of a probabilistic classification problem.
to explore the use of data science and machine learning in the field of clinic research and medical diagnostics.
### Is data preprocessing the most important phase of a machine learning project?
The answer of mine is yes. Even though, I chose a relatively small and clean dataset, the time costed in cleaning data in the whole process is the longest.

because of many issues of data collection, e.g., inconsistent standard, different context, human errors, etc., clean data is impossible, especially when the dataset is huge.
analyzing data that has not been carefully screened can be misleading.
when cleaning data, we can use common sense as well as background knowledge to rule out or drop impossible data combinations, missing values, improper code.
take advantage of visualization tools to get more knowledge of dataset is important which helps to tell stories by curating data into a form easier to understand, highlight the trends and the outliers.