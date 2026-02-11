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

<ul>Data integration refers to the process of combining and harmonizing data from multiple sources into a unified, coherent format that can be put to use for various analytical, operational and decision-making purposes.</ul>
<ul>
<a href="https://www.ibm.com/think/topics/data-integration#763338456" target="_blank">
  <img src="https://img.shields.io/badge/IBM-Data%20Integration-0062CE?logo=ibm&logoColor=white" />
  <strong>Open IBM Data Integration Topic</strong>
</a>
</ul>


<ul>
  <ul>
    <li>Remove Duplicates/Data Redundancy</li>
    <li>Fixing Inconsistencies</li>
    <li>Data Cleaning (<b>Data cleaning</b> is necessary because after collecting data through multiple methods, new data may arrive, and therefore it must be cleaned.)</li>
    <li>Merge data</li>
    <li>Data consolidation</li>  
  </ul>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
3.	Data Transformation 
</h3>

<ul>Data transformation is at the heart of data analysis and machine learning. In a machine learning pipeline, which includes modifying the raw data and converting raw data into a more suitable format or structure for analysis and model training purpose, to improve its quality, performance and make it compatible with the requirements of a particular task or system. In data transformation, we usually deal with issues such as noise, missing values, outliers, and non-normality.</ul>

<ul><a href="https://www.geeksforgeeks.org/machine-learning/data-transformation-in-machine-learning/" target="_blank">
  <img src="https://img.shields.io/badge/GeeksforGeeks-ML%20Data%20Transformation-2DBE4F?logo=geeksforgeeks&logoColor=white" />
  <strong>Data Transformation in Machine Learning</strong>
</a>
</ul>

<ul><a href="https://www.geeksforgeeks.org/data-analysis/what-is-data-transformation/" target="_blank">
  <img src="https://img.shields.io/badge/GeeksforGeeks-Data%20Transformation%20(Analysis)-2DBE4F?logo=geeksforgeeks&logoColor=white" />
  <strong>What Is Data Transformation?</strong>
</a>
</ul>

<ul><a href="https://www.geeksforgeeks.org/dbms/data-transformation-techniques-in-data-mining/" target="_blank">
  <img src="https://img.shields.io/badge/GeeksforGeeks-Data%20Mining%20Transformation-2DBE4F?logo=geeksforgeeks&logoColor=white" />
  <strong>Data Transformation Techniques in Data Mining</strong>
</a>
</ul>

<ul>
  <ul>
    <li>Scaling</li>
    <li>Normalization</li>
    <li>Aggregation (combining two or more variable/features)</li>
    <li>Generalization</li>
    <li>Data Transformation Techniques are:</li>
      <ul>
        <li>Smoothing</li>
        <li>Aggregation</li>
        <li>Discretization</li>
        <li>Attribute Construction</li>
        <li>Generalization</li>
        <li>Normalization</li>
          <ul>
            <li>Min-Max Normalization</li>
            <li>Z-Score Normalization</li>
            <li>Decimal Scaling</li>
          </ul>
        <li>Data Reduction</li>
        <li>Encoding Techniques</li>
          <ul>
            <li>One-Hot Encoding</li>
            <li>Label Encoding</li>
            <li>Binary Encoding</li>
            <li>Frequency Encoding</li>
          </ul>
        <li>Feature Scaling</li>
        <li>Data Integration</li>
          <ul>
            <li>Handling schema mismatch</li>
            <li>Resolving naming conflicts</li>
            <li>Merging tables</li>
          </ul>
        <li>Data Encoding for Text (Text Transformation)</li>
        <ul>
          <li>Tokenization</li>
          <li>Stemming / Lemmatization</li>
          <li>TF-IDF</li>
          <li>Word embeddings</li>
        </ul>
        <li>Data Binarization</li>
        <li>Data Scaling and Standardization for Outliers</li>
        <ul>
          <li>Log transformation</li>
          <li>Square root transformation</li>
          <li>Reciprocal transformation</li>
        </ul>
        <li>Higher Level Concepts</li>
      </ul>
  </ul>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
4.	Data Reduction
</h3>

<ul>Data reduction is the process of reducing the size of a dataset while still preserving the most important information, to improve the efficiency and performance of machine learning algorithms and other data-driven processes.<br>
This can be beneficial in situations where the dataset is too large to be processed efficiently, or where the dataset contains a large amount of irrelevant or redundant information.
</ul>


<!-- TABLE WITH CAPTION (Table caption ABOVE table) -->
<p style="color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; text-align:center;">
<ul><b>Table 8.1:</b> Input Feature Matrix for Col51 Prediction.</ul>
</p>
<ul>
  <table>
  <thead>
    <tr>
      <th>Col1</th>
      <th>Col2</th>
      <th>Col3</th>
      <th>Col4</th>
      <th>...</th>
      <th>Col50</th>
      <th>Predict the Col51 based on Col1 to Col50</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>2</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>...</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>100</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>
</ul>

<ul>
  50 (feature) x 100 (rows) = 5000 <br>
  25 (feature—top priority) x 100 (rows) = 2500
</ul>

<ul>
    <a href="https://www.geeksforgeeks.org/dbms/data-reduction-in-data-mining/" target="_blank">
  <img src="https://img.shields.io/badge/GeeksforGeeks-Data%20Reduction%20in%20Data%20Mining-2DBE4F?logo=geeksforgeeks&logoColor=white" />
  <strong>Data Reduction in Data Mining</strong>
</a>
</ul>

<ul>
  <li>Dimensionality Reduction
    <a href="https://www.datacamp.com/tutorial/understanding-dimensionality-reduction" target="_blank">
    <img src="https://img.shields.io/badge/DataCamp-Dimensionality%20Reduction%20Tutorial-0DC9F5?logo=datacamp&logoColor=white" />
    </a> &nbsp;<a href="https://www.geeksforgeeks.org/dbms/data-reduction-in-data-mining/" target="_blank">
    <img src="https://img.shields.io/badge/GeeksforGeeks-Data%20Reduction%20in%20Data%20Mining-2DBE4F?logo=geeksforgeeks&logoColor=white" />
    </a>
  </li>
  <li>Numerosity Reduction</li>
</ul>








