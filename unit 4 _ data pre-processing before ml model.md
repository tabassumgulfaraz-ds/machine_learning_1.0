<!-- UNIT -->
<h1 style="color:#6EC1E4; font-family:Arial, Helvetica, sans-serif; font-size:18px;">
UNIT 4
</h1>

<!-- TITLE -->
<h2 style="color:#6EC1E4; font-family:Arial, Helvetica, sans-serif; font-size:16px;">
DATA PRE-PROCESSING BEFORE ML MODEL
</h2>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
A.	Data
</h3>

<ul style="list-style-type:'■'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Where does data come from, and why does it come? Behind data, there is always a science — an <b>aim or a question.</b> Based on that aim, we work and collect data, or obtain it from different sources. Basically, an aim or question is the reason why we collect data.</li>
  <li><b>Metadata explains the details of data,</b> such as where the data came from, how it was collected, when it was created, its format, and how it should be used.</li>
  <li><b>Data preprocessing</b> means making data capable of being used effectively by a machine learning model so that it performs in the best possible way. Even if the data is correct and safe, preprocessing is still required. Preprocessing is always necessary.<br>
If the data is already correct, there are still some steps needed to further improve it so that a machine learning model can work properly and efficiently.
</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
B.	Data Preprocessing
</h3>

<ul style="list-style-type:'■'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Data preprocessing is the process of evaluating, filtering, manipulating, and encoding data so that a machine learning algorithm can understand it and use the resulting output. The major goal of data preprocessing is to eliminate data issues such as missing values, errors, noise, inconsistencies, improve data quality, and make the data useful for machine learning purposes.<br>
Data practitioners spend ~80% of their time on data preprocessing and management, as raw data is messy, coming from diverse sources.<br>
Structured sequence for preprocessing:
<!-- BULLETS: Numeric -->
<ol style="color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Acquire the dataset</li>
  <li>Import libraries </li>
  <li>Load/import datasets</li>
  <li>Check for missing values</li>
  <li>Encode non-numerical data</li>
  <li>Scale the features</li>
  <li>Split into training, validation, evaluation sets</li>
</ol>
</li>
</ul>

<ul style="list-style-type:'■'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li><b>Why is data preprocessing important?</b><br>
  Data preprocessing is required for almost all types of data analysis, data science, and AI development to produce trustworthy, precise, and resilient findings for corporate applications.<br>
Machine learning and deep learning algorithms perform best when data is presented in a way that streamlines the solution to a problem.<br>
Data wrangling, data transformation, data reduction, feature selection, and feature scaling are all examples of data preprocessing approaches teams use to reorganize raw data into a format suitable for certain algorithms. This can significantly reduce the processing power and time necessary to train a new machine learning or AI system or perform an inference against it.<br>
Most of the current data science packages and services now contain preprocessing libraries that automate many of these activities.
<br></br>
<a href="https://lakefs.io/blog/data-preprocessing-in-machine-learning/" target="_blank">
  <img src="https://img.shields.io/badge/LakeFS-Data%20Preprocessing-FF6B35?logo=data&logoColor=white" />
  <strong>Read Data Preprocessing in Machine Learning</strong>
</a>    
</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
C.	Data Preprocessing Key Steps and Techniques in Machine Learning
</h3>
<ul style="list-style-type:' '; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <a href="https://www.datacamp.com/courses/preprocessing-for-machine-learning-in-python" target="_blank">
  <img src="https://img.shields.io/badge/DataCamp-Preprocessing%20Course-0DC9F5?logo=datacamp&logoColor=white" />
  <strong>Preprocessing for Machine Learning (Python) by DataCamp Free</strong>
</a>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
1.	Data Cleaning
</h3>

<ul style="list-style-type:' '; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
Data cleaning, also called data cleansing or data scrubbing, is the process of identifying and correcting errors and inconsistencies in raw data sets to improve data quality.<br></br>
  <a href="https://www.ibm.com/think/topics/data-cleaning" target="_blank">
  <img src="https://img.shields.io/badge/IBM-Data%20Cleaning-0062CE?logo=ibm&logoColor=white" />
  <strong>Open IBM Data Cleaning Guide</strong>
</a>
</ul>

<ul style="list-style-type:'■'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
<ul style="list-style-type:'■'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Handling/Impute Missing/Null Values</li>
  <li>Remove Noisy Data</li>
  <li>Outlier Detection and Removal</li>
  <li>Remove Duplicates </li>
  <li>Noise Reduction</li>
  <li>Fixing Inconsistencies</li>
  <li>Data Validation</li>
  <li>Data Standardization</li>
  <li>Data Normalization</li>
  <li>Data Type Correction</li>
  <li>Handling Invalid Values</li>
  <li>Data Smoothing</li>
  <li>Error Correction</li>
  <li>Removing Irrelevant Data</li>
  <li>Data Integrity Checks</li>
  <li>Handling Imbalanced Data</li>
</ul>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
2.	Data Integration 
</h3>

<!-- IMAGE WITH CAPTION (Figure caption BELOW image) -->
<ul>
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit4/figure_2dot1.png" alt="Demo Image" width="600">
</p>
</ul>

<ul>
<p style="color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; text-align:center;">
<b>Figure 2.1:</b> Data Integration via Triangulation.
</p>
</ul>







