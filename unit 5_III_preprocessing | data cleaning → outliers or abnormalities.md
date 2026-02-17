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

**Table 1.3.1.1.** Univariate Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table1dot3dot1dot1.png" alt="Demo Image" width="600">
</p>
<br>

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

**Table 1.3.2.1.** Multivariate Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot2dot1.png" alt="Demo Image" width="600">
</p>
<br>
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

**Table 1.3.3.1.** Global Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot3dot1.png" alt="Demo Image" width="600">
</p>
<br>
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

**Table 1.3.4.1.** Local (Contextual) Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot4dot1.png" alt="Demo Image" width="600">
</p>
<br>
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

**Table 1.3.5.1.** Point Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot5dot1.png" alt="Demo Image" width="600">
</p>
<br>
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

**Table 1.3.6.1.** Contextual Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot6dot1.png" alt="Demo Image" width="600">
</p>
<br>
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

**Table 1.3.7.1.** Collective Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot7dot1.png" alt="Demo Image" width="600">
</p>
<br>
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

**Table 1.3.8.1.** Recurrent Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot8dot1.png" alt="Demo Image" width="600">
</p>
<br>
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

**Table 1.3.9.1.** Periodic Outlier – Data Table
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/table%201dot3dot9dot1.png" alt="Demo Image" width="600">
</p>
<br>
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

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot5.png" alt="Demo Image" width="600">
</p>

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

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot6dot1dot1.png" alt="Demo Image" width="600">
</p>

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

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot6dot2dot2_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot6dot2dot2_II.png" alt="Demo Image" width="600">
</p>

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

<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot6dot2dot3_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot6dot2dot3_II.png" alt="Demo Image" width="600">
</p>

**Figure 1.6.2.3.** Boxplot showing the five-number summary and distribution skewness of the dataset.


### 1.6.3. Clustering Method (K-Means)

In the clustering method, we divide data points into clusters. This can be done using the **K-Means clustering algorithm.** Where we specify the number of clusters, we want to divide the data into. Then we assign each data point to a cluster.

Then we calculate the distance of each data point from the centroid of the cluster it belongs to.

Then we remove the data points that are farthest from the centroid of the cluster they belong to.
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot6dot3dot1_I.png" alt="Demo Image" width="600">
</p>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot6dot3dot1_II.jpg" alt="Demo Image" width="600">
</p>

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

# 📊 Outlier Detection and Removal Guide

### 1.9. Outlier Visualization/Detection and Removal


### 1.9.1. Visualization Method for Outlier Detections

### **Box Plot** ⭐⭐⭐⭐⭐

- **Best for univariate outliers**
- Shows quartiles, median, and outliers clearly
- Easy to interpret for non-technical audiences
- Industry standard for outlier visualization
- **Library**: `seaborn` / `matplotlib`

### **Violin Plot** ⭐⭐⭐⭐

- Combines box plot + distribution shape
- Shows data density
- Better for understanding overall distribution

### **Scatter Plot** ⭐⭐⭐⭐

- Good for seeing outliers in context
- Shows patterns and trends
- Useful for time-series or indexed data
- **Library**: `matplotlib`

### **Z-score Plot** ⭐⭐⭐⭐

- Shows standardized deviations
- Clear threshold visualization (±3σ)
- Good for statistical reporting

### **Histogram** ⭐⭐⭐

- Shows distribution shape
- Less precise for outlier identification
- Better for understanding data spread
- **Library**: `seaborn` / `matplotlib`

### **Heatmap/Correlation Matrix** ⭐⭐⭐

- For multivariate outlier detection
- Shows relationships between variables
- Useful for complex datasets

### **Pair Plot**

- Relationship-based outliers
- **Library**: `seaborn`

### 1.9.2. LIBRARIES FOR OUTLIER DETECTION

**Table 1.9.2.1.** Essential Python libraries for outlier detection: ratings, use cases, and key functions

| Library | Rating | Category | Best For | Key Functions | When to Use |
|---------|--------|----------|----------|---------------|-------------|
| **NumPy** | ⭐⭐⭐⭐ | Computation | Array operations | `percentile()`, `std()`, `mean()` | Basic statistics, mathematical operations |
| **Pandas** | ⭐⭐⭐⭐⭐ | Data Manipulation | Data preprocessing | `describe()`, `quantile()`, `filter()` | IQR method, data cleaning, exploration |
| **SciPy** | ⭐⭐⭐⭐⭐ | Statistics | Statistical tests | `stats.zscore()`, `stats.iqr()` | Z-score method, advanced statistics |
| **Scikit-learn** | ⭐⭐⭐⭐⭐ | Machine Learning | ML detection | `IsolationForest`, `LocalOutlierFactor` | Multivariate detection, production ML |
| **Matplotlib** | ⭐⭐⭐⭐ | Visualization | Custom plots | `boxplot()`, `scatter()`, `hist()` | Publication plots, custom visualization |
| **Seaborn** | ⭐⭐⭐⭐⭐ | Visualization | Statistical plots | `boxplot()`, `violinplot()`, `heatmap()` | Quick statistical visualization |
| **PyOD** | ⭐⭐⭐⭐ | Specialized | Algorithm research | 40+ algorithms | Comparing methods, research projects |

> **💡 Golden Rule:** *"Outliers are not always errors. Errors are always outliers. Know the difference."*


### 1.9.3. METHOD SELECTION MATRIX

**Table 1.9.3.1.** Method selection matrix showing recommended outlier detection approaches based on data characteristics and distribution types.

| Scenario | Best Method | Why | Libraries |
|----------|-------------|-----|-----------|
| **Normal distribution** | Z-Score (3σ) | Statistically sound, well-understood | `scipy.stats` |
| **Skewed distribution** | IQR or Modified Z-Score | Robust to skewness | `pandas`, `scipy` |
| **Multivariate data** | Isolation Forest, Mahalanobis Distance | Captures complex patterns | `sklearn`, `scipy` |
| **Time-series data** | LSTM Autoencoder, Prophet | Temporal dependencies | `tensorflow`, `prophet` |
| **High-dimensional** | Isolation Forest, PCA + Z-Score | Curse of dimensionality | `sklearn` |
| **Streaming/Real-time** | Incremental algorithms, EWMA | Memory efficient | `river`, `online-learning` |
| **Small datasets (<100)** | IQR, Domain knowledge | Statistical power issues | `pandas` |
| **Large datasets (>1M)** | Isolation Forest, Sampling + IQR | Computational efficiency | `sklearn`, `dask` |
| **Mixed data types** | Isolation Forest, HBOS | Handles categorical + numerical | `pyod` |
| **Explainability required** | IQR, Z-Score, Domain rules | Stakeholder understanding | `pandas`, `numpy` |
| **Black-box OK** | Deep learning autoencoders, IF | Maximum performance | `tensorflow`, `sklearn` |
| **Imbalanced data** | Isolation Forest, One-Class SVM | Designed for rare events | `sklearn` |
| **Clustered data** | DBSCAN, LOF | Respects local density | `sklearn` |



![Python Libraries for Outlier Detection - Comprehensive Comparison](https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot9dot3dot1.png)
**Figure 1.9.3.1.** Comparative analysis of nine popular Python libraries for outlier detection across five key evaluation dimensions.

Quantitative comparison of nine widely-used Python libraries for outlier detection and data analysis, evaluated across five critical dimensions: ease of use, performance, scalability, feature richness, and documentation quality. Each library is rated on a 5-point scale (1=poor, 5=excellent) across all dimensions, presented as grouped bar charts for direct comparison. This multi-dimensional analysis enables practitioners to select libraries aligned with their specific project requirements, balancing factors such as ease of implementation, computational efficiency, scalability needs, algorithmic variety, and learning curve considerations.


![Outlier Detection Method Effectiveness Matrix](https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit5_III/figure%201dot9dot3dot2.png)
**Figure 1.9.3.2.** Effectiveness heatmap showing performance of eight outlier detection methods across eight common data scenarios.


Comprehensive effectiveness matrix visualizing the performance of eight outlier detection methodologies across eight distinct data scenarios, presented as a color-coded heatmap with quantitative ratings (1=poor, 5=excellent). The methods evaluated include statistical approaches (Z-Score, IQR), machine learning techniques (Isolation Forest, Local Outlier Factor, DBSCAN, One-Class SVM), distance-based methods (Mahalanobis), and deep learning approaches (Autoencoder). The color gradient (red=poor, yellow=moderate, green=excellent) provides immediate visual indication of method suitability.



### 1.9.4. FINAL RECOMMENDATION MATRIX

**Table 1.9.4.1.** Role-based recommendations for outlier detection tools, methods, and visualization approaches tailored to different data professional roles.

| Your Role | Primary Tool | Secondary Tool | Visualization |
|-----------|--------------|----------------|---------------|
| **Data Analyst** | IQR (Pandas) | Z-Score | Box plots, Histograms |
| **Data Scientist** | Isolation Forest | LOF, IQR | Box plots, Scatter plots |
| **ML Engineer** | Isolation Forest | Autoencoders | Dashboards, Monitoring |
| **Data Engineer** | Dask + IF | Spark + Sampling | Streaming dashboards |
| **Research Scientist** | Custom methods | Multiple ensemble | Academic plots |
| **Business Analyst** | IQR (Excel/BI) | Percentiles | Interactive dashboards |

Role-specific recommendation matrix for outlier detection implementation across six distinct data professional roles. The matrix provides tailored guidance considering the unique requirements, technical capabilities, and organizational contexts of each role. This role-based framework acknowledges that effective outlier detection requires not only technical accuracy but also alignment with organizational workflows, stakeholder communication needs, and available technical infrastructure.



### 1.9.5. Resources for Deep Dive

1. **PyOD**: https://github.com/yzhao062/pyod (40+ algorithms)
2. **Anomaly Detection Resources**: https://github.com/yzhao062/anomaly-detection-resources
3. **Isolation Forest Paper**: Liu et al., 2008
4. **Industry Survey**: Anomaly Detection in Practice (2023)
5. **Visualization**: Network graphs, engagement timelines



### 📝 **Remember: The best method depends on:**

- ✅ Data characteristics
- ✅ Domain requirements
- ✅ Computational resources
- ✅ Explainability needs
- ✅ Production constraints


### 1.9.6. SCALABILITY CONSIDERATIONS

**Table 1.9.6.1.** Scalability analysis of outlier detection methods showing recommended approaches, tools, and expected processing times across different dataset sizes.

| Data Size | Method | Tool | Processing Time |
|-----------|--------|------|-----------------|
| **< 10K rows** | Any method | Pandas + NumPy | Seconds |
| **10K - 100K** | IQR, IF, LOF | Pandas + Sklearn | Seconds - Minutes |
| **100K - 1M** | Isolation Forest | Sklearn + sampling | Minutes |
| **1M - 10M** | IF + sampling, DBSCAN | Dask, Vaex | Minutes - Hours |
| **10M - 100M** | Distributed IF | PySpark | Hours |
| **> 100M** | Sampling + streaming | Spark, Flink | Hours - Days |

Performance and scalability analysis of outlier detection methodologies across six data volume categories ranging from small datasets (<10K rows) to big data scenarios (>100M rows). The table systematically evaluates computational complexity and processing efficiency by mapping dataset sizes to appropriate detection methods, computational frameworks, and expected execution times. This analysis provides critical guidance for infrastructure planning and method selection in production environments.



### 🎯 Quick Start Guide

### **Step 1: Select Appropriate Libraries**
```python
import pandas as pd
import numpy as np
from scipy import stats
from sklearn.ensemble import IsolationForest
```
<ul>
  <!-- Live Jupyter Notebook (Binder) -->
  <a href="https://mybinder.org/v2/gh/tabassumgulfaraz-ds/machine_learning_1.0/HEAD?filepath=files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://mybinder.org/badge_logo.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Live Jupyter - Binder)</strong>
  </a><br>
  ⏳ This will take a few seconds or minutes, so you need to be patient.
  <br></br>
  
  <!-- Open in Google Colab -->
  <a href="https://colab.research.google.com/github/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Colab)</strong>
  </a>
  <br>

  <!-- Open in Kaggle -->
  <a href="https://kaggle.com/kernels/welcome?src=https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://img.shields.io/badge/Kaggle-Open%20Notebook-20BEFF?logo=kaggle&logoColor=white" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Kaggle)</strong>
  </a>
</ul>

### **Step 2: Choose Your Visualization Method**
```python
# Select numeric columns
df.select_dtypes(include=[np.number]).columns

# Set up subplot grid
n_cols = 2   # number of plots per row
n_rows = int(np.ceil(len(df) / n_cols))

plt.figure(figsize=(18, 5 * n_rows))

for i, col in enumerate(df, 1):
    plt.subplot(n_rows, n_cols, i)
    sns.boxplot(y=df[col])
    plt.title(f'Outliers in {col}')
    plt.ylabel(col)

plt.tight_layout()
plt.show()
```
<ul>
  <!-- Live Jupyter Notebook (Binder) -->
  <a href="https://mybinder.org/v2/gh/tabassumgulfaraz-ds/machine_learning_1.0/HEAD?filepath=files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://mybinder.org/badge_logo.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Live Jupyter - Binder)</strong>
  </a><br>
  ⏳ This will take a few seconds or minutes, so you need to be patient.
  <br></br>
  
  <!-- Open in Google Colab -->
  <a href="https://colab.research.google.com/github/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Colab)</strong>
  </a>
  <br>

  <!-- Open in Kaggle -->
  <a href="https://kaggle.com/kernels/welcome?src=https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://img.shields.io/badge/Kaggle-Open%20Notebook-20BEFF?logo=kaggle&logoColor=white" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Kaggle)</strong>
  </a>
</ul>


### **Step 3: Apply Detection Method**
```python
1.	IQR
2.	Z-Score
3.	K-Means Clustering
4.	Isolation Forest
5.	DBSCAN
6.	Local Outlier Factor
7.	Elliptic Envelope
8.	One-Class SVM
9.	Mahala-Nobis Distance
10.	Robust Random Cut Forest
11.	Histogram-based Outlier Score
12.	K-Nearest Neighbors
13.	Local Correlation Integral
14.	and many more…

# Select numeric columns only
numeric_df = df.select_dtypes(include=[np.number])

# Create empty boolean mask
outlier_mask = pd.DataFrame(False, index=df.index, columns=numeric_df.columns)

# Apply IQR column-wise
for col in numeric_df.columns:
    Q1 = numeric_df[col].quantile(0.25)
    Q3 = numeric_df[col].quantile(0.75)
    IQR = Q3 - Q1
    
    lower = Q1 - 1.5 * IQR
    upper = Q3 + 1.5 * IQR
    
    outlier_mask[col] = (numeric_df[col] < lower) | (numeric_df[col] > upper) 

# Detect rows where ANY column has outlier
df[outlier_mask.any(axis=1)]
```
<ul>
  <!-- Live Jupyter Notebook (Binder) -->
  <a href="https://mybinder.org/v2/gh/tabassumgulfaraz-ds/machine_learning_1.0/HEAD?filepath=files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://mybinder.org/badge_logo.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Live Jupyter - Binder)</strong>
  </a><br>
  ⏳ This will take a few seconds or minutes, so you need to be patient.
  <br></br>
  
  <!-- Open in Google Colab -->
  <a href="https://colab.research.google.com/github/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Colab)</strong>
  </a>
  <br>

  <!-- Open in Kaggle -->
  <a href="https://kaggle.com/kernels/welcome?src=https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://img.shields.io/badge/Kaggle-Open%20Notebook-20BEFF?logo=kaggle&logoColor=white" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Kaggle)</strong>
  </a>
</ul>

### **Step 4: Validate and Document**
```python
# Store detected outliers from Step 3
outliers = df[outlier_mask.any(axis=1)]

# Total number of outlier rows
len(outliers)

# Percentage of dataset flagged as outlier
{round((len(outliers)/len(df))*100, 2)}

# Column-wise outlier count
outlier_mask.sum()

# Display detected outlier rows
outliers
```
<ul>
  <!-- Live Jupyter Notebook (Binder) -->
  <a href="https://mybinder.org/v2/gh/tabassumgulfaraz-ds/machine_learning_1.0/HEAD?filepath=files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://mybinder.org/badge_logo.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Live Jupyter - Binder)</strong>
  </a><br>
  ⏳ This will take a few seconds or minutes, so you need to be patient.
  <br></br>
  
  <!-- Open in Google Colab -->
  <a href="https://colab.research.google.com/github/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Colab)</strong>
  </a>
  <br>

  <!-- Open in Kaggle -->
  <a href="https://kaggle.com/kernels/welcome?src=https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://img.shields.io/badge/Kaggle-Open%20Notebook-20BEFF?logo=kaggle&logoColor=white" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Kaggle)</strong>
  </a>
</ul>

### Step 5: Remove Outliers
```python
In this step, we deal with outliers present in the dataset. Outliers can negatively impact model performance, especially for algorithms sensitive to extreme values (e.g., linear regression, k-means).

There are multiple ways to handle outliers:

   1. Remove outlier rows completely
   If the outliers are due to data entry errors or are not meaningful, we can remove those rows from the dataset.

   2. Cap or Winsorize values
   Replace extreme values with upper and lower threshold limits (e.g., using IQR or percentile method).

   3. Transform the data
   Apply transformations such as log, square root, or Box-Cox to reduce the impact of extreme values.

   4. Use robust models or scaling techniques
   Some algorithms (e.g., tree-based models) and robust scalers are less sensitive to outliers.
```
<ul>
  <!-- Live Jupyter Notebook (Binder) -->
  <a href="https://mybinder.org/v2/gh/tabassumgulfaraz-ds/machine_learning_1.0/HEAD?filepath=files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://mybinder.org/badge_logo.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Live Jupyter - Binder)</strong>
  </a><br>
  ⏳ This will take a few seconds or minutes, so you need to be patient.
  <br></br>
  
  <!-- Open in Google Colab -->
  <a href="https://colab.research.google.com/github/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Colab)</strong>
  </a>
  <br>

  <!-- Open in Kaggle -->
  <a href="https://kaggle.com/kernels/welcome?src=https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://img.shields.io/badge/Kaggle-Open%20Notebook-20BEFF?logo=kaggle&logoColor=white" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Kaggle)</strong>
  </a>
</ul>

### 📊 Summary Matrix

| **What** | **When** | **Tool** |
|----------|----------|----------|
| Quick visual check | Always start here | Box Plot (Seaborn) |
| Statistical detection | Normal distribution | Z-Score (SciPy) |
| Robust detection | Skewed data | IQR (Pandas) |
| ML-based detection | Multivariate patterns | Isolation Forest (Sklearn) |
| Big data | Datasets > 1M | Dask/PySpark |


### 🚀 Best Practices

1. **Always visualize first** - Use box plots or scatter plots
2. **Combine methods** - Statistical + ML + Domain knowledge
3. **Document decisions** - Log which outliers removed and why
4. **Validate results** - Compare before/after statistics
5. **Consider context** - Not all outliers are errors


### 📚 Additional Resources

- **Documentation**: See individual library documentation for detailed API reference
- **Tutorials**: Check GitHub repositories for practical examples
- **Community**: Join data science forums for discussions
- **Papers**: Read original research papers for theoretical foundations


### 📞 Contact & Support

For questions or clarifications about outlier detection methods, consult:
- Official library documentation
- Academic papers on anomaly detection
- Data science community forums
- Domain experts in your field

**Last Updated:** 2025  
**Version:** 1.0  
**Status:** Comprehensive Guide


> **⚡ Pro Tip:** Start with IQR for baseline detection, add Isolation Forest for ML enhancement, and always validate with domain knowledge. This approach works for 90% of real-world projects!

## 1.10. Outlier Visualization, Detection, Validation & Document, and Removal
### 1.10.1.	Interquartile Range (IQR)

### 1.10.2.	Z-Score

### 1.10.3.	K-Means Clustering

### 1.10.4.	Isolation Forest


<ul>
  <!-- Live Jupyter Notebook (Binder) -->
  <a href="https://mybinder.org/v2/gh/tabassumgulfaraz-ds/machine_learning_1.0/HEAD?filepath=files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://mybinder.org/badge_logo.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Live Jupyter - Binder)</strong>
  </a><br>
  ⏳ This will take a few seconds or minutes, so you need to be patient.
  <br></br>
  
  <!-- Open in Google Colab -->
  <a href="https://colab.research.google.com/github/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Colab)</strong>
  </a>
  <br>

  <!-- Open in Kaggle -->
  <a href="https://kaggle.com/kernels/welcome?src=https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_III/preprocessing_datacleaning_outlers.ipynb" target="_blank">
    <img src="https://img.shields.io/badge/Kaggle-Open%20Notebook-20BEFF?logo=kaggle&logoColor=white" />
    <strong>Outlier Visualization, Detection and Removal Method Notebook (Kaggle)</strong>
  </a>
</ul>
