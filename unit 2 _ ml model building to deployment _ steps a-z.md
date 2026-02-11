<!-- UNIT -->
<h1 style="color:#6EC1E4; font-family:Arial, Helvetica, sans-serif; font-size:18px;">
UNIT 2
</h1>

<!-- TITLE -->
<h2 style="color:#6EC1E4; font-family:Arial, Helvetica, sans-serif; font-size:16px;">
ML MODEL BUILDING TO DEPLOYMENT | STEPS A-Z
</h2>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
1.	Define the Problem
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Aim (The aim of this project is to design and develop an AI-based application that can accurately recognize and understand doctors’ handwritten text.)
</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
2.	Data Collection (Primary) and Gathering (Secondary—online available)
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Remove errors during collection</li>
  <li>Maintain the quality of data</li>
  <li>Many more…</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
3.	Data Preprocess
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Data preprocessing is the most important step, where a machine learning engineer spends about 80% of the time, while only 20% is spent on model development and the subsequent steps.
</li>
  <li>Raw data → Data Explore and Exploratory Data Analysis EDA (anomalies, outliers, missing or null values, feature engineering, etc.) → Data Wrangling/Tidy up → Machine Learning 
</li>
  <li>Data preprocessing is the transformation of raw data into a format that is more suitable and meaningful for analysis and model training. Data preprocessing plays a vital role in enhancing the quality and efficiency of ML models by addressing issues such as missing values, noise, inconsistencies, and outliers in the data.
</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
4.	Choose a Model
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>A machine learning (ML) model is a computer program that has been trained on a specific dataset to recognize patterns or make predictions on new, unseen data.</li>
  <li>First, we identify the datatype of the variable we want to predict. For example, if we want to predict gender (male or female) from data, the target variable is categorical, which makes it a classification problem.<br>On the other hand, if we want to predict the price of a mobile phone, the target variable is numeric, which makes it a regression problem.</br>Classification and regression algorithms are designed separately to handle these types of problems.</br>Another type of problem is clustering, which falls under unsupervised learning.</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
5.	Split/Splitting the Data
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>In machine learning, we have two types of data:<br>X and Y. X is used to predict Y, which means X is the independent variable and Y depends on X. X can be a single variable or multiple variables. Independent variables (X) are also called predictors. X represents the input, while Y represents the output. In ML terminology, X is referred to as features, and Y is referred to as labels. Typically, X is denoted by a capital letter, and Y by a small letter.</br><!-- IMAGE WITH CAPTION (Figure caption BELOW image) -->
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit2/Figure%205dot1.png" alt="Demo Image" width="600">
</p>
<p style="color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; text-align:center;">
<b>Figure 5.1</b> Train and Test Split.
</p></li>
<li>In this figure, if the newly arrived predicted data point is 7, it is slightly far from the known data. In such cases, we have some metrics, which are called evaluation metrics, that help us judge how far the predicted value is from the original value. For example, R-squared (R²), RMSE (root mean square error), and MSE (mean square error) are commonly used.</li>
<li>The train–test split ratio can be 80:20, 75:25, or 70:30, depending on the requirement.</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
6.	Model Evaluation
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>A metric is a numerical measure used to evaluate the performance of a machine learning model by comparing predicted values with actual values, means a metric is a way to measure how good or bad a model’s predictions are. In simple term matric means to check the machine learning prediction.</li>
  <li>Metrics are important because they help us evaluate and compare the performance of different machine learning models. For example, suppose we have three models: A, B, and C. If the R² values are 0.6 for model A, 0.7 for model B, and 0.75 for model C, and the MSE values are 1.22 for model A, 0.99 for model B, and 0.001 for model C, we can compare these values to decide which model performs best. Higher R² values and lower MSE values indicate better model performance. </li>
  <li>Model evaluation is important because it measures the accuracy and overall performance of a model. It allows us to understand how well the model performs, identify whether it performs well or poorly, and compare different models to select the best one.</li>
  <li>If a model’s performance is not good, we need to perform tuning. For model tuning, we use hyperparameters.</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
7.	Hyperparameter Tuning
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Suppose we train three models: <b>A, B, and C,</b> and evaluate them <b>before tuning:</b><ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Model A: R² = 0.6, MSE = 1.22</li>
  <li>Model B: R² = 0.7, MSE = 0.99</li>
  <li>Model C: R² = 0.75, MSE = 0.001</li>
</ul>At this stage, <b>model C looks best</b> because it has <b>higher R²</b> and <b>lower MSE.</b></li></ul>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Now we apply <b>hyperparameter tuning</b> (for example, changing learning rate, depth, number of neighbors, etc.) and <b>re-train the models.</b><br>After tuning, the results may change:</br><ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Model A: R² = 0.85, MSE = 0.002</li>
  <li>Model B: R² = 0.78, MSE = 0.010</li>
  <li>Model C: R² = 0.76, MSE = 0.020</li>
</ul>After tuning, <b>model A becomes better than model C</b> because:</b><ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Model A now has a <b>higher R²</b></li>
  <li>Model A has a <b>lower MSE</b></li>
</ul></ul>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>Hyperparameter tuning is important because a model that initially performs poorly (like model A) can become the best-performing model after proper tuning.</li>
  <li>Every model has the potential to perform well if we have a deep understanding of its background. A model is basically like an equation, for example, A = mX + b. If we understand the components—A, m, X, and b—well, we can fully grasp the theoretical foundation of the model and use it effectively.</li>
  <li>As an alternative to hyperparameter tuning, we can enhance model performance and ensure better accuracy by applying cross-validation, which evaluates the model on different subsets of the training and test data.</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
8.	Cross Validation
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>We can enhance model performance and ensure better accuracy by applying cross-validation, which evaluates the model on different subsets of the training and test data.</li><!-- TABLE WITH CAPTION (Table caption ABOVE table) -->
<p style="color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; text-align:center;">
  <b>Table 8.1:</b> Cross Validation for Train and Test.
</p>

<table border="1" cellpadding="8" cellspacing="0"
       style="border-collapse:collapse; font-family:Arial, Helvetica, sans-serif; font-size:13px; width:80%; margin:auto;">
  <tr style="background-color:#E6F2FF;">
    <th>Overall Data</th>
    <th>First</th>
    <th>Second</th>
    <th>Third</th>
    <th>Forth</th>
    <th>Fifth</th>
  </tr>

  <tr>
    <td rowspan="5" style="text-align:center; font-weight:bold;">80% train and 20% test</td>
    <td>20% test</td>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% train</td>
  </tr>
  <tr>
    <td>20% train</td>
    <td>20% test</td>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% train</td>
  </tr>
  <tr>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% test</td>
    <td>20% train</td>
    <td>20% train</td>
  </tr>
  <tr>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% test</td>
    <td>20% train</td>
  </tr>
  <tr>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% train</td>
    <td>20% test</td>
  </tr>
</table>
  <li>This process is called cross-validation. We divide the data into five equal parts (each 20%). In each iteration, one part is used as the test set and the other four parts are used as the training set. We rotate the parts each time to test the model’s performance on all subsets. By training the same model on different subsets of data, we can evaluate its performance more reliably. At the end, the model’s accuracy may be good, bad, or optimal, depending on how well it generalizes.</li>
  <li>Why is cross-validation needed? In preprocessing, the top 80% of the data (training set) may be well-represented, but the remaining 20% (test set) may not be. This can lead to errors if we rely on a single train-test split. Cross-validation helps reduce this error by rotating the data, so every subset gets a chance to be tested. This ensures that the model’s performance is measured reliably and that there is no bias in the selection of data.</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
9.	Model Finalization
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>During model finalization, we aim to ensure the model’s performance meets the required standards. We evaluate it using multiple validation datasets, and if the model performs well, we proceed to the next step.</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
10.	Deploy the Model
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>We deploy the model within a mobile app, web app, website, software, or any other platform. For example, models are deployed in applications like Adobe Photoshop, Excel, and ChatGPT, which are used across different platforms.</li>
  <li>For deployment, we require both frontend and backend development. Within the company, we work on <b>MLOps</b> alongside senior team members to handle the frontend and backend integration of the model.</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
11.	Restart, Update, Version Controls and Monitor the Model (MLOps)
</h3>

<ul style="list-style-type:'●'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li><b>MLOps</b> stands for <b>Machine Learning Operations.</b> MLOps means that after deploying a model, we continuously <b>retest, update, and manage it,</b> along with <b>version control.</b>
For example, ChatGPT has different versions such as <b>3.5, 4.0, 5.0, and now 5.2.</b> As new data becomes available, the model is updated and improved.<br>Nowadays, <b>LLM (Large Language Model)–based systems</b> like <b>ChatGPT, Gemini, and Claude</b> work on the same concept. In many cases, no coding is required; we can directly ask questions and get responses.</br>
</li>
  <li><b>When we deploy a model, we must have a clear understanding of the market.</b> It should not happen that the product has no users or demand.<br>During deployment, we also need to invest in resources such as <b>hosting, domain services, computational power, and other infrastructure.</b> These resources are essential to fully utilize and understand the model’s capacity and performance.</br></li>
</ul>



<p align="center">
  <a href="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/pdf_notes/Unit%202_ML%20Model%20Building%20to%20Deployment%20(Steps%20a-z).pdf" target="_blank">
    <img src="https://cdn-icons-png.flaticon.com/512/337/337946.png" 
         alt="PDF Logo" 
         width="100"/>
  </a>
</p>

<p align="center">
  <a href="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/pdf_notes/Unit%202_ML%20Model%20Building%20to%20Deployment%20(Steps%20a-z).pdf" target="_blank">
    <b>Ml Model Building to Deployment | Steps A-Z</b>
  </a>
</p>






