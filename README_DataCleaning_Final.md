# UNIT 5: PREPROCESSING | DATA CLEANING → MISSING VALUES

## 1. Data Cleaning

Data cleaning is the process of identifying and correcting errors, inconsistencies and removing any missing, duplicate or irrelevant data in the data to ensure it is accurate and complete. The objective is to address issues that can distort analysis or model performance.

- Raw data (log file, transactions, audio/video recordings, etc.) is often **noisy, incomplete and inconsistent** which can negatively impact the accuracy of model.
- The goal of data cleaning is to ensure that the data is **accurate, consistent and free of errors**.
- Clean datasets also important in **EDA (Exploratory Data Analysis)** which enhances the interpretability of data so that the right actions can be taken based on insights.

**For example:**

- **Handling missing values:** Using strategies like mean/mode imputation, deletion, or predictive models to fill in or remove missing data.
- **Removing duplicates:** Eliminating duplicate records to ensure each entry is unique and relevant.
- **Correcting inconsistent formats:** Standardizing formats (e.g., date formats, string cases) to maintain consistency.

---

## 1.1. Exploring/Identifying Missing Values in the Dataset

### a. Method 1: Missing Values Analysis

### b. Method 2: Percentage of missing values

### c. Method 3: Visualizing Missing Values

### d. Method 4: DataFrame Info Missing Values Summary

---

## 1.2. Other Names of Missing Values

- **NaN (Not a Number):** Used in programming libraries like Python (pandas) to represent missing or invalid numeric data.
- **Null:** Commonly used in database systems such as SQL to indicate no value.
- **Undefined:** A value that has not been assigned or defined.
- **Blank / Empty:** A field with no entered value.
- **Placeholder Values:** Default values (e.g., −1, 0, 999) used to represent missing data.
- **Sentinel Values:** Special placeholder values indicating specific conditions, often used for missing data.
- **Dummy Data:** Artificial or test data that does not represent real observations.
- **Missing Data:** A general term used in statistics and research for unavailable values.

---

## 1.3. How to Identify Missing Values?

To identify missing values, we use some techniques. These techniques are called **Missing Value Detection Techniques**. Some of these techniques are given below:

- **Visual Inspection:** Missing values are identified by visualizing the data.
- **Descriptive Statistics:** Missing values are identified by calculating the descriptive statistics of the data.
- **Missingno Library:** Missing values are identified by using the Missingno library.

---

## 1.4. Why Is Handling Missing Values So Important?

- **Deep Impact on Model Accuracy:** The presence of missing values reduces the accuracy of machine learning models and negatively affects their overall performance.
- **Questions on Data Quality:** Missing values weaken the quality of data, which can lead to misunderstandings and incorrect conclusions in our analysis and decision-making.
- **Model Training Time Increases:** Sometimes, due to missing values, the model training time increases, resulting in a waste of both time and computational resources.

---

## 1.5. Deciding Whether to Remove a Column with Missing Values

Having missing values is common in any dataset, but when deciding whether a column should be removed or not, this decision depends on several important factors:

- **Data Quantity:**
  
  If you have a very large amount of data and a specific column contains a very high percentage of missing values (for example, 70% or 80%), then removing that column may be a better option, because it becomes difficult to extract meaningful value from it.

- **Column Importance:**
  
  If the column with missing values is very important for your analysis or model, then removing it would not be a good decision. In such cases, you can use different techniques to impute the missing values.

- **Nature of the Data:**
  
  Sometimes, the presence of missing values itself conveys important information. For example, in a survey, if a question is left unanswered, it may indicate that the participant was uncomfortable answering it. In such cases, removing or blindly replacing the missing value may not be appropriate.

- **Model Sensitivity:**
  
  Some machine learning models can handle missing values, while others are sensitive to them. If the chosen model is sensitive to missing values, then you must handle those missing values properly before training.

- **Type of Data:**
  
  For numerical data, missing values can be replaced using the mean, median, or mode. For categorical data, missing values can be replaced using the mode or by assigning a specific category.

- **General Rule (Not Absolute):**
  
  Generally, if more than **50%** of the data in a column is missing, you should consider whether removing that column would be a better option. However, this is not a hard-and-fast rule. Every dataset is unique and has different requirements. Therefore, the decision on how to handle missing values should always be made based on the context of the dataset.

---

## 1.6. Detailed Methods for Handling Missing Values

- **Re-Collecting Data from the Original Data Source:**
  
  If you have access to the original resource from where the data was collected, you can retrieve the missing values again from that source.

- **Imputing Data Using Mean, Median, or Mode:**
  
  If the data is numerical, missing values are commonly replaced using the mean or median. For categorical data, the mode is typically used to fill in missing values.

- **Using Forward or Backward Fill:**
  
  In some datasets, there is a sequence of time or dates. In such datasets, a missing value in one row is replaced with the value from the previous or the next row.

- **Using KNN Imputation:**
  
  This is an advanced technique in which a missing value is replaced with the average value of its neighboring data points. This method is available in libraries such as scikit-learn.

- **Using Deep Learning Techniques:**
  
  Deep learning techniques, such as autoencoders, can also be helpful in handling missing values.

- **Simply Deleting the Data:**
  
  If the number of missing values in your dataset is very small, you can delete the specific row or column containing those missing values.

### What If I Don't Handle Missing Values?

Then the model will definitely not work well—and that's not all, listen further!

If we ignore missing values, we may face many problems. Some of the issues that can arise are listed below:

- **Decrease in Model Accuracy:**
  
  The accuracy of machine learning models can decrease because the model does not receive complete information.

- **Incorrect Analysis:**
  
  Wrong results may be produced during data analysis, which can negatively affect decision-making.

- **Model Confusion:**
  
  Some models cannot handle missing values, causing the model to fail during training or make incorrect predictions.

- **Bias in the Model:**
  
  Missing values increase the risk of introducing bias into the model.

- **Incorrect Interpretation of Data:**
  
  Due to missing values, the available information may be incomplete or incorrect, leading to wrong interpretation of the data.

- **Storage Issues:**
  
  If missing values are not replaced, storage-related issues may occur because some systems cannot properly store missing values.

- **Data Integration Problems:**
  
  When integrating data from different sources, missing values can create serious integration issues.

- **Incorrect Feature Selection:**
  
  In the presence of missing values, some important features that should influence the model may be ignored.

- **Incorrect Experimental Results:**
  
  In scientific or research projects, missing values can lead to incorrect experimental outcomes.

- **Stress and Extra Work:**
  
  Data scientists may have to do extra work during analysis because missing values need to be identified and handled.

---

## 1.7. How to Perform Data Cleaning

The process begins by identifying issues like missing values, duplicates and outliers. Performing data cleaning involves a systematic process to identify and remove errors in a dataset. The following steps are essential to perform data cleaning:

- **Remove Unwanted Observations:** Eliminate duplicates, irrelevant entries or redundant data that add noise.
- **Fix Structural Errors:** Standardize data formats and variable types for consistency.
- **Manage Outliers:** Detect and handle extreme values that can skew results, either by removal or transformation.
- **Handle Missing Data:** Address gaps using imputation, deletion or advanced techniques to maintain accuracy and integrity.

---

## 1.8. Dealing/Impute Missing Values Using Pandas Library

### Calculate median for age column

Median is less affected by outliers as compared to mean.

### Mean or Median Imputation

### Drop or remove the deck column with high missing values

### Calculate mode for embarked column

### Calculate mode for embark_town column

### Value counts for embarked columns

### Mode Imputation for categorical columns

Embarked and embark_town are categorical columns with few missing values, we can use Mode Imputation to fill missing values.

### Using dropna method to remove rows with missing values

**See more ways…**

---

## 1.9. Impute age column missing values using forward fill method

Forward fill is a data imputation technique used to handle missing values, by replacing a missing value with the most recent non-missing value in rows that appears before it in the dataset.

---

## 1.10. Impute age column missing values using backward fill method

Backward fill is a data imputation technique used to handle missing values, by replacing a missing value with the next available non-missing value in rows that appears after it in the dataset.

---

## 1.11. Imputation of Missing Values Using scikit-learn Library

[Link to documentation]

There are **four types of imputation** for handling missing values:

### 1. Univariate Feature Imputation (SimpleImputer)

The **SimpleImputer** class provides basic strategies for imputing missing values. Univariate imputation is a missing-value handling approach in which missing values are filled using a single column's own information. As described, the SimpleImputer replaces missing values with a constant value or a statistical measure (mean, median, or most frequent) calculated from the same column where the missing values occur, without using information from other features.

The SimpleImputer class also supports categorical data represented as string values or pandas categoricals when using the `'most_frequent'` or `'constant'` strategy.

### 2. Multivariate Feature Imputation (IterativeImputer)

Multivariate feature imputation is an advanced missing-value handling technique in which the missing values of a feature are estimated using information from other related features in the dataset. Instead of treating each column independently, this approach models each feature with missing values as a function of the remaining features.

Using the **IterativeImputer**, each feature is taken one by one as the target variable, while the other features are used as predictors. A regression model is trained on the observed values and then used to predict the missing values. This process is performed iteratively in multiple rounds, refining the estimates at each step, until the final imputed values are produced.

### 3. Nearest Neighbors Imputation (KNNImputer)

Nearest Neighbors Imputation is a method for handling missing values, in which each missing feature value is estimated using the values of the **k nearest samples = rows (neighbors – data point)** that have observed values for that feature.

Distances between samples = rows (data points) are computed using a **Euclidean metric** that supports missing values, and the imputed value is obtained by taking a uniform or distance-weighted average of the neighbors' feature values.

### 4. Marking Imputed Values (SimpleImputer, MissingIndicator)

Marking imputed values means adding extra columns that show whether a value was originally missing or not.

The **MissingIndicator** transformer creates a binary matrix:
- **1** → value was missing
- **0** → value was present

This is useful because after imputation, the model cannot naturally know which values were originally missing. Sometimes, the fact that a value was missing itself carries important information.

**Table: Marking Missing Values Example**

<table>
  <thead>
    <tr>
      <th>Original Data</th>
      <th>After Imputation (Age filled)</th>
      <th>After adding MissingIndicator</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Age</strong><br>25<br>NaN</td>
      <td><strong>Age</strong><br>25<br>26</td>
      <td><strong>Age</strong>&nbsp;&nbsp;&nbsp;<strong>Age_missing</strong><br>25&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0<br>26&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1</td>
    </tr>
  </tbody>
</table>

MissingIndicator adds binary features that indicate which values were originally missing, so this information is preserved after imputation.

- It only marks missing positions
- Imputation still fills the values

---

## 1.12. Conclusion

### Missing Values – A Major Challenge but Also a Valuable Opportunity

Dealing with missing values is certainly a challenge for every data scientist, but it also provides an important learning opportunity. It helps us understand how to improve data quality and make our datasets more reliable. In the end, high-quality data leads to more accurate, intelligent insights and better-performing models.
