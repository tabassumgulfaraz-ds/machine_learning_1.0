# UNIT 5_III

# PREPROCESSING | DATA CLEANING → OUTLIERS/ABNORMALITIES

## 1. Outliers/Abnormalities

In machine learning, **outliers are data points that deviate significantly from the general distribution of the dataset.** They are unusual observations that don't follow the expected pattern of the majority of your data.

Anomaly detection, or outlier detection, is the identification of observations, events or data points that deviate from what is usual, standard or expected, making them inconsistent with the rest of a data set.

Other names for outliers include **deviants, abnormalities, anomalies** (or **anomalous points**), and **aberrant observations**.

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot1.png" alt="Demo Image" width="600">
</p>

**Figure 1.1.** Visual Representation of Outliers in Machine Learning. Outliers (Red Circles) Are Data Points That Deviate Significantly from Normal Data Clusters (Green Dots).

- **Green dots** = Normal data points that follow the expected pattern

- **Cluster 1 & 2** = Most data naturally group together (normal distribution)

- **Red circles** = Outliers - data points that are far away from the main clusters

- **Red arrows** = Point to the unusual observations

<!-- IMAGE WITH CAPTION (Figure caption BELOW image) -->

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot2.png" alt="Demo Image" width="600">
</p>

**Figure 1.2.** Impact Of Outliers on Data Distribution. Left: Outliers Distort Statistical Measures. Right: Clean Data After Outlier Removal.

**LEFT SIDE (With Outliers)**  
- Shows data distribution including extreme outlier values (2, 5, 95, 100)

- Red triangles mark the outliers

- Mean is **distorted** and pulled away from the true center

- Red dashed line shows how outliers skew the average

**RIGHT SIDE (Without Outliers)**  
- Shows the same data after removing outliers

- Mean and median are now close together

- Represents the data **accurately**

- Clean, reliable distribution

**a. Impact on ML models:** Can bias parameter estimation, increase variance and reduce model accuracy.

**b. Sources:** Data entry errors, measurement noise, genuine rare events.

**c. Handling methods:** Removal, transformation or robust algorithms less sensitive to outliers.

**d. Domain dependence:** What is considered an outlier in one domain (e.g., finance) may be normal in another.

Outliers are a type of data that can provide meaningful results, though they are mostly unmeaningful.

**Outliers are data points that fall outside the expected or valid range for a specific category.**

In the context of age categorization, an outlier occurs when a person's age doesn't match their assigned age group.

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.** Age outlier detection showing normal data (green circles) and outliers (red X) across four age categories in Islamabad city.

This chart displays all four age categories on a single graph, making it easy to compare outlier patterns across categories.

- **X-axis:** Four age categories (Child, Teenager, Adult, Senior)

- **Y-axis:** Age values from 0 to 100 years (marked at intervals: 0, 20, 40, 60, 80, 100)

- **Green circles:** Normal/valid data points that fall within the correct age range

- **Red X markers:** Outliers that fall outside the valid range

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure1dot4.png" alt="Demo Image" width="600">
</p>

**Figure 1.4.** Category-wise age outlier breakdown with valid ranges (green areas) and outlier statistics for each age group.

This chart breaks down each category into separate panels for detailed analysis of outliers in each age group.

- **Four separate panels:** One for each age category

- **Green shaded area:** Highlights the valid age range for that category

- **Statistics shown:** Number of normal records vs. outliers for each category

- **Green box annotation:** Shows the exact valid range in years


### 1.1. Reasons That Can Cause Outliers

1. Data collection mistakes.

2. If the data is collected by a machine, the machine may have a problem or malfunction.

2. Typographical mistakes.

4. Issues with measurement or measuring instruments in the original data.

5. Data entry errors.

6. Sampling errors.

7. Natural variation in the data.

8. Incorrect data processing or coding errors.

9. Experimental errors.

10. Fraudulent or intentionally altered data.


### 1.2. Why Identifies Outliers?

**1.** **Machine learning models may not perform properly** – Outliers can reduce model accuracy and distort predictions.

**2.** **They pull the center (mean/median) toward themselves** – Extreme values can shift measures of central tendency.

**3.** **They create skewness in the data** – Outliers can make the distribution uneven or biased.

**4.** **They lead to incorrect results** – Statistical analysis may give misleading conclusions.


### 1.3. Types of Outliers

### 1.3.1. Univariable Outlier

A Univariate outlier is an extreme value that **relates to just one variable.**

These are outliers that **occur in only one variable.**

**Example:** If your data has only an age variable and someone's age is 150 years which is very unlikely, then this would be a univariate outlier.
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table1dot3dot1dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.1.1.** Univariate Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot1dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot1dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.1.1.** Univariate Outlier – Box Plot, Distribution View and Bar Chart


### 1.3.2. Multivariate Outlier

A multivariate outlier is a combination of unusual or extreme result for **at least two variables.**

These are outliers that occur in a **combination of more than one variable.**

**Example:** A person's age is 25 years but income is 10 million - this combination is unusual and can be a multivariate outlier (but confirmation is necessary).
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot2dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.2.1.** Multivariate Outlier – Data Table

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot2dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot2dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.2.1.** Multivariate Outlier – Box Plot, Distribution View and Bar Chart


### 1.3.3. Global Outlier

A global outlier is a **data point that shows an unusual or extreme result** when compared to the **entire dataset.**

These are outliers that are abnormal in the context of the entire dataset.

**Example:** If the average height of students in a school is 5 feet, and one student's height is 11 feet, then this would be a global outlier.
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot3dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.3.1.** Global Outlier – Data Table

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot3dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot3dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.3.1.** Global Outlier – Box Plot, Distribution View and Bar Chart


### 1.3.4. Local (Contextual) Outlier

A local (contextual) outlier is a data point that shows an unusual or extreme result only **within a specific cluster, group, or context**, but may appear normal when compared to the entire dataset.

These are outliers that are abnormal only in the context of a specific cluster or group.

**Example:** In summer, a temperature of 35°C is normal, but 35°C in January would be a local outlier based on the winter season in Pakistan.
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot4dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.4.1.** Local (Contextual) Outlier – Data Table

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot4dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot4dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.4.1.** Local (Contextual) Outlier – Box Plot, Distribution View and Bar Chart


### 1.3.5. Point Outliers

A point outlier is a **single data point that shows an unusual or extreme value compared to the rest of the dataset.**

These are **individual data points that are completely different from the rest of the data.**

**Example:** In a class, all students' marks are between 60-80/100, but one student's marks are 2/100 - this is a point outlier.
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot5dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.5.1.** Point Outlier – Data Table

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot5dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot5dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.5.1.** Point Outlier – Box Plot, Distribution View and Bar Chart


### 1.3.6. Contextual Outliers

A **contextual outlier** is a data point that appears normal in general but becomes unusual or extreme within a **specific context such as time, location, or condition.**

These are outliers that are abnormal in a **specific context.**

**Example:** A $10 transaction on a credit card is normal, but a $10,000 transaction at 3 AM could be a contextual outlier which banks use fraud detection applications for.
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot6dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.6.1.** Contextual Outlier – Data Table

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot6dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot6dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.6.1.** Contextual Outlier – Box Plot, Distribution View and Bar Chart


### 1.3.7. Collective Outliers

A **collective outlier** is a group of data points that **may appear normal when observed individually** but **form an unusual or abnormal pattern when considered together.**

This is a **group of data points** that may be **individually normal** but are **collectively abnormal.**

**Example:** If a website suddenly receives 1000 visits from the same IP address in one day, this is a collective outlier (possible bot attack or DDoS (Distributed Denial of Service) attack).
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot7dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.7.1.** Collective Outlier – Data Table

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot7dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot7dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.7.1.** Collective Outlier – Box Plot, Distribution View and Bar Chart


### 1.3.8. Recurrent Outliers

A **recurrent outlier** is a data point or pattern that appears unusual but **occurs repeatedly over time in a consistent manner.**

These are outliers that **occur repeatedly.**

**Example:** Money comes into someone's salary account on the 1st of every month - this is a recurring pattern.
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot8dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.8.1.** Recurrent Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot8dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot8dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.8.1.** Recurrent Outlier – Box Plot, Distribution View and Bar Chart


### 1.3.9. Periodic Outliers

These are outliers that occur **regularly in a specific period.**

A **periodic outlier** is a data point or pattern that appears extreme but **occurs regularly during a specific time period or season.**

**Example:** On Black Friday or Eid, shopping websites have very high traffic - this is a periodic outlier and cannot be compared with regular days.
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot9dot1.png" alt="Demo Image" width="600">
</p>

**Table 1.3.9.1.** Periodic Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot9dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot3dot9dot1_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.3.9.1.** Periodic Outlier – Box Plot, Distribution View and Bar Chart


### 1.4. Causes of Outliers

Outliers can be caused by anything. Some common causes are given below:

### 1.4.1. Data Entry Errors

While entering data, outliers can occur due to human error.

For example, if your data has an age variable, and someone enters age as 1000 years instead of 100 years, then this would be an outlier.

### 1.4.2. Measurement Errors

While measuring data, outliers can occur due to equipment or human error.

For example, if your data has a height variable, and due to a faulty measuring tape, someone's height is measured as 50 feet instead of 5 feet, then this would be an outlier.

### 1.4.3. Experimental Errors

While conducting experiments with data, outliers can occur due to faulty procedures or equipment.

For example, if while measuring the quantity of a chemical in a lab the scale malfunctions, the readings can become outliers.

### 1.4.4. Intentional Outliers

In some cases, people intentionally enter incorrect data.

For example, in online surveys if someone enters their income as $10,000,000 instead of $10,000 to maintain privacy, then this would be an outlier.

### 1.4.5. Data Processing Errors

Outliers can appear due to technical errors while processing, transforming, or merging data.

For example, if the decimal point is placed incorrectly during currency conversion ($10050 instead of $100.50), then this becomes an outlier.

### 1.4.6. Sampling Errors

While collecting data, unusual cases can be sampled due to faulty sampling methods.

For example, if you are conducting a middle-class income survey and accidentally include a billionaire's data as well, then this would be an outlier.

### 1.4.7. Natural Outliers

In the real world, there are some genuine unusual events or cases that are naturally outliers.

For example, the sudden spike in hospital visits during the COVID-19 pandemic, or an athlete's exceptional performance that breaks records - these are natural outliers that are genuine and represent real phenomena.


### 1.5. Why should we care about Outliers?

Here you can see a complete understanding about outliers in this figure.

**Figure 1.5.** A comprehensive understanding of outliers and their impact on data analysis

### 1.5.1. Hidden Clues

Outliers give us hidden clues. By identifying them, we can discover hidden patterns.

Outliers are not always wrong; sometimes they can really enhance your understanding, and they can even inspire great research questions.

### 1.5.2. Data Quality

Data quality decreases due to outliers. By identifying them, we can improve data quality.

### 1.5.3. Impact Analysis

Errors occur in our analysis due to outliers. By identifying them, we can improve our analysis.

### 1.5.4. Better Decisions

Our decisions are also affected by outliers. By identifying them, we can make better decisions.

### 1.5.5. Better Models

The accuracy of our models decreases due to outliers. By identifying them, we can build better models.

### 1.5.6. Better Insights

Our insights are also affected by outliers. By identifying them, we can extract better insights.

### 1.5.7. Better Visualization

The quality of our visualizations decreases due to outliers. By identifying them, we can create better visualizations.

### 1.5.8. Better Storytelling

Our storytelling is also affected by outliers. By identifying them, we can create better stories.

### 1.5.9. Better Data Products

The quality of our data products decreases due to outliers. By identifying them, we can create better data products.

### 1.5.10. Better Data Science

The quality of our data science decreases due to outliers. By identifying them, we can do better data science.


### 1.6. Detect and Remove Outliers

To identify outliers, we use some techniques. We call these techniques 'Outlier Detection Techniques'. Some of these techniques are given below:

1. Z-Score
2. IQR
3. DBSCAN
4. Isolation Forest
5. Local Outlier Factor
6. Elliptic Envelope
7. One-Class SVM
8. Mahala-Nobis Distance
9. Robust Random Cut Forest
10. Histogram-based Outlier Score
11. K-Nearest Neighbors
12. K-Means Clustering
13. Local Correlation Integral
14. and many more…

We will only look at **Z-Score, IQR,** and **K-Means Clustering.**


### 1.6.1. Z – Score Method

In the Z-Score method, we see how many standard deviations (SD) a data point is away from the mean.

The formula for Z-Score is:

**z = (x − μ) / σ**

**Where:**

- **Z** – is the Z-Score

- **x** – is the data point

- **μ** – is the mean of the data

- **σ** – is the standard deviation of the data

- **(x - μ):** is the difference between the data point and the mean

- **Z** – is the difference between the data point and the mean in terms of standard deviations

**Figure 1.6.1.1.** Normal Distribution and Z-Score Standardization

#### 1.6.1.1. Properties of Z-Score

1. The mean of Z-Score is 0 and standard deviation is 1.

2. The higher the Z-Score value, the farther the data point is from the mean.

3. The lower the Z-Score value, the closer the data point is to the mean.

4. If the Z-Score value is greater than 3 or less than -3, then the data point is an outlier.

**Table 1.6.1.1.** Z-Score Thresholds for Outlier Detection

| Z-Score | Data Point | Interpretation |
|---------|-----------|----------------|
| < -3 | More than 3 SDs below the mean | Outlier |
| -3 to -2 | 2-3 SDs below the mean | Not an outlier (threshold) |
| -2 to -1 | 1-2 SDs below the mean | Not an outlier |
| -1 to 0 | 0-1 SD below the mean | Not an outlier |
| 0 | Mean | Not an outlier |
| 0 to 1 | 0-1 SD above the mean | Not an outlier |
| 1 to 2 | 1-2 SDs above the mean | Not an outlier |
| 2 to 3 | 2-3 SDs above the mean | Not an outlier (threshold) |
| > 3 | More than 3 SDs above the mean | Outlier |


### 1.6.2. Interquartile Range (IQR)

In **machine learning**, the **Interquartile Range (IQR)** method is a simple and effective statistical technique to detect **outliers** in a dataset.

The interquartile range, in short **IQR**, is a measure of **descriptive statistics**, which determines the range between the lower and the upper quartile, which can also be described as the middle 50% of a sample. A quartile is a type of **quantile**, which divides a sample into 4 same-sized groups of 25% each.
<p align="center">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot6dot2dot1.png" alt="Demo Image" width="600">
</p>

**Figure 1.6.2.1.** Quartile division of a sample illustrating Q1, median (Q2), and Q3 under the IQR framework.

**Figure 1.6.2.2.** Boxplot with interquartile range and probability density function of a Normal N(0, σ²) distribution.

**Outlier Detection using IQR**

- **Lower Bound = Q1 - 1.5 × IQR**

- **Upper Bound = Q3 + 1.5 × IQR**

- Any data point below the Lower Bound or above the Upper Bound is considered an outlier.

IQR measures the spread of the middle 50% of the data.

In the IQR method, we see how many IQRs a data point is away from the median.

The formula for IQR is:

**IQR = Q3 − Q1**

**Where:**

- **IQR** = is the Interquartile Range

- **Q1** = 25th percentile (lower quartile i.e., first quartile)

- **Q3** = 75th percentile (upper quartile i.e., third quartile)

- **(Q3 - Q1)** = is the difference between the third quartile and the first quartile

**Outlier Rule**

- **Lower bound = Q1 − 1.5 × IQR**

- **Upper bound = Q3 + 1.5 × IQR**

- Any value outside these bounds is considered an outlier.

### 1.6.2.1. Properties of IQR

1. IQR represents the range of the middle 50% of the data.

2. The higher the IQR value, the more spread out the middle 50% of the data is.

3. The lower the IQR value, the more concentrated the middle 50% of the data is around the median.

**Figure 1.6.2.3.** Boxplot showing the five-number summary and distribution skewness of the dataset.


### 1.6.3. Clustering Method (K-Means)

In the clustering method, we divide data points into clusters. This can be done using the **K-Means clustering algorithm.** Where we specify the number of clusters, we want to divide the data into. Then we assign each data point to a cluster.

Then we calculate the distance of each data point from the centroid of the cluster it belongs to.

Then we remove the data points that are farthest from the centroid of the cluster they belong to.

**Figure 1.6.3.1.** Outliers' detection - Illustration


### 1.7. Handling Outliers

To handle outliers, we use some techniques. We call these techniques 'Outlier Handling Techniques'. Some of these techniques are given below:

### 1.7.1. Removing the outlier

This is the most common method where all detected outliers are removed from the dataset.

### 1.7.2. Transforming and binning values

Outliers can be transformed to bring them within a range. Techniques like log transformation or square root transformation can be used.

### 1.7.3. Imputation

Outliers can also be replaced with mean, median, or mode values.

### 1.7.4. Separate treatment

In some use-cases, it's beneficial to treat outliers separately rather than removing or imputing them.

### 1.7.5. Robust Statistical Methods

Some of the statistical methods to analyze and model the data are less sensitive to outliers and provide more accurate results in the data.


### 1.8. Conclusion

1. Outliers in a dataset are observations that deviate dramatically from the rest of the data points. They might arise as a result of data gathering mistakes or abnormalities, or they can be real findings that are just infrequent or extraordinary.

2. If outliers are not appropriately accounted for, they might produce misleading, inconsistent, and erroneous findings. As a result, identifying and dealing with outliers is critical in order to produce accurate and useful data analysis findings.

3. Outliers may be detected using a variety of methods, including the percentile approach, IQR method, and z-score method. Outliers can be dealt with in a variety of methods, including removal, transformation, imputation, and so on.
