<!-- UNIT -->
<h1 style="color:#6EC1E4; font-family:Arial, Helvetica, sans-serif; font-size:18px;">
UNIT 3
</h1>

<!-- TITLE -->
<h2 style="color:#6EC1E4; font-family:Arial, Helvetica, sans-serif; font-size:16px;">
ALGORITHMS, TRAINING & TESTING DATA | FEATURES | MODLE, IMPORTANT PYTHON LIBRARIES FOR MACHINE LEARNING AND INSTALLATION STEPS
</h2>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
1.	Algorithms 
</h3>

<ul style="list-style-type:' ■ ' ; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>An algorithm is a set of rules or instructions given to an AI system to help it learn form data.<br>Example: Decision Tree is an algorithm used for classification and regression task.</br>2 * 2 = 4<br>4 * 2 = 8</br>6 * 2 = 12<br>8 * 2 = 16</br>x * 2 = x + x   (rule)<br>2x = x + x   (rule)</br>3x = x + x + x   (rule)<br>2x, 3x   (algorithm)</br>2x + 3y - 4y = z	(algorithm)</li>
<p style="text-align:center; font-family:Arial, Helvetica, sans-serif; font-size:13px;">
  <b>Table 1.1</b> Relationship between x, y, and z
</p>

<table border="1" cellpadding="8" cellspacing="0"
       style="border-collapse:collapse; width:70%; margin:auto; font-family:Arial, Helvetica, sans-serif; font-size:13px;">
  <tr style="background-color:#E6F2FF;">
    <th>x</th>
    <th>y</th>
    <th>= z</th>
  </tr>
  <tr>
    <td>2(x) + 3</td>
    <td>-14(y)</td>
    <td>z</td>
  </tr>
</table>

<p style="text-align:center; font-family:Arial, Helvetica, sans-serif; font-size:13px;">
  <b>Table 1.2</b> Classification Dataset (y is a categorical variable)
</p>

<table border="1" cellpadding="8" cellspacing="0"
       style="border-collapse:collapse; width:80%; margin:auto; font-family:Arial, Helvetica, sans-serif; font-size:13px;">
  <tr style="background-color:#E6F2FF;">
    <th>Hair (cm)</th>
    <th>Height</th>
    <th>Bia</th>
    <th>= Gender (y)</th>
  </tr>
  <tr>
    <td>24</td>
    <td>160</td>
    <td>Yes</td>
    <td>Female</td>
  </tr>
  <tr>
    <td>36</td>
    <td>165</td>
    <td>Yes</td>
    <td>Female</td>
  </tr>
  <tr>
    <td>48</td>
    <td>170</td>
    <td>Yes</td>
    <td>Female</td>
  </tr>
  <tr>
    <td>8</td>
    <td>175</td>
    <td>No</td>
    <td>Male</td>
  </tr>
</table>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
2.	Training Data, Testing Data, Features and Model
</h3>

<ul style="list-style-type:' ■ '; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li><b>Training Data:</b> The dataset used to train the machine learning model. It’s labeled data for supervised learning.<br>Example: A set of images of cat and dog, each labeled with "cat " and "dog ".</br> </li>
  <li><b>Testing Data:</b> Data used to evaluate the performance of a model after training. It’s unseen by the model during training.<br>Example: A new set of images not included in the training data, used to check the accuracy of a trained model.</br> </li>
  <li><b>Features:</b> Individual measurable properties or characteristics of a phenomenon being observed, used as input variables in a model.<br>Input (features like x1, x2, x3) and output (labeled like y)</br>Example: In a dataset for house price prediction (labeled), features might include square footage, number of bedrooms, and age of the house (features). </li>
  <li><b>Model:</b> In machine learning, a model refers to the specific representation (like 2x + 3y - 4y = z) learned from data, based on which predictions or decisions are made.<br>Example: A neural networks trained to identify objects in an image.</br> </li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
3.	Overfitting vs Underfitting
</h3>

<ul style="list-style-type:'  '; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
<!-- IMAGE WITH CAPTION (Figure caption BELOW image) -->
<p align="left">
  <img src="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/figures/unit3/figure_3dot1.png" width="600">
</p>

<p style="color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; text-align:left;">
<b>Figure 3.1</b> Overfitting vs Underfitting.
</p>
<li><b>Overfitting:</b> A modeling error, that occurs when a model is too complex and learns the noise and details in training data to the extent that it negatively impacts the performance of the model on new data.<br>Example: A model that performs exceptionally well on the training data but poorly on the testing data.</br></li>
<li><b>Underfitting:</b> This occurs when a model is too simple, unable to capture the underlying pattern of the data, and therefore performs poorly on both training and new data.<br>Example: A liner regression model trying to fit non-liner data..</br></li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
4.	Important Python libraries for Machine Learning
</h3>

- [Scikit-learn](https://scikit-learn.org/) — Machine learning library
- [TensorFlow](https://www.tensorflow.org/) — Deep learning framework
- [Keras](https://keras.io/) — High-level neural networks API
- [PyTorch](https://pytorch.org/) — Deep learning library
- [NLTK (Natural Language Toolkit)](https://www.nltk.org/) — NLP library
- [OpenCV](https://opencv.org/) — Computer vision library
- **Many more…**

<ul style="list-style-type:'■'; color:#000000; font-family:Arial, Helvetica, sans-serif; font-size:13px; margin-left:40px;">
  <li>All models are available within libraries, along with their user guides, documentation, code, and definitions. The scikit-learn library is widely used for data preprocessing. Feature extraction is also provided by the scikit-learn library. Classification, regression, clustering, dimensionality reduction, model selection, and preprocessing all come under the scikit-learn library.</li>
</ul>

<!-- HEADING -->
<h3 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
5.	Installation steps for machine learning environment
</h3>

<h4 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
5.1.	Bash Terminal Commands 
</h4>

<a href="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds3/pytho_environment_setup.ipynb" target="_blank">
  <img src="https://img.shields.io/badge/Bash-4EAA25?logo=gnu-bash&logoColor=white" />
    <strong>Open Environment Setup Notebook</strong>
</a>

<h4 style="color:#003366; font-family:Arial, Helvetica, sans-serif; font-size:15px;">
5.2.	Jupyter Notebook Cell
</h4>

<a href="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds3/pytho_environment_setup_jupyter.ipynb" target="_blank">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white" />
  <strong>Open Environment Setup Notebook</strong>
</a>
<br><br>
<a href="https://mybinder.org/v2/gh/tabassumgulfaraz-ds/machine_learning_1.0/main?filepath=files_and_datasets/f_ds3/pytho_environment_setup_jupyter.ipynb" target="_blank">
  <img src="https://img.shields.io/badge/Jupyter-Live%20Notebook-F37626?logo=jupyter&logoColor=white" />
  <strong>Open Environment Setup Notebook (Live)</strong>
</a>

# 🖥️ Run Jupyter Notebook Locally

<a href="#" target="_blank">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white" />
  <strong>Open Environment Setup Notebook (Local)</strong>
</a>














