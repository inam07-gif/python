<h1 align="center">Diabetes Prediction using Machine Learning</h1>

<hr>

<h2>1. Introduction</h2>

<p>
This project applies <strong>Machine Learning techniques</strong> to predict whether a patient has diabetes 
based on selected health-related measurements.
</p>

<p>
The dataset was originally provided by the 
<strong>National Institute of Diabetes and Digestive and Kidney Diseases</strong>.
</p>

<p>
The objective is to build a <strong>Binary Classification Model</strong> that predicts:
</p>

<ul>
  <li><strong>0</strong> → Non-Diabetic</li>
  <li><strong>1</strong> → Diabetic</li>
</ul>

<p>
This problem falls under <em>Supervised Learning (Classification)</em>.
</p>

<hr>

<h2>2. Dataset Description</h2>

<p>
The dataset contains structured patient records. Each row represents 
<strong>one patient</strong>, and each column represents a 
<strong>feature (input variable)</strong> used for prediction.
</p>

<h3>Features Included</h3>

<table border="1" cellpadding="8" cellspacing="0">
<tr>
<th>Feature</th>
<th>Description</th>
</tr>

<tr>
<td><strong>Pregnancies</strong></td>
<td>Number of times the patient has been pregnant</td>
</tr>

<tr>
<td><strong>Glucose</strong></td>
<td>Blood glucose level measured after a glucose tolerance test</td>
</tr>

<tr>
<td><strong>BloodPressure</strong></td>
<td>Diastolic blood pressure value</td>
</tr>

<tr>
<td><strong>SkinThickness</strong></td>
<td>Skin fold thickness measurement</td>
</tr>

<tr>
<td><strong>Insulin</strong></td>
<td>Serum insulin level measured after testing</td>
</tr>

<tr>
<td><strong>BMI</strong></td>
<td>Body Mass Index calculated using weight and height</td>
</tr>

<tr>
<td><strong>DiabetesPedigreeFunction</strong></td>
<td>Score indicating family history influence</td>
</tr>

<tr>
<td><strong>Age</strong></td>
<td>Age of the patient (in years)</td>
</tr>

<tr>
<td><strong>Outcome</strong></td>
<td>Target Variable (0 = Non-Diabetic, 1 = Diabetic)</td>
</tr>

</table>

<hr>

<h2>3. Dataset Constraints</h2>

<ul>
  <li>All patients are <strong>female</strong></li>
  <li>All patients are <strong>21 years or older</strong></li>
  <li>All patients belong to <strong>Pima Indian heritage</strong></li>
</ul>

<p>
Therefore, this dataset represents a specific demographic group 
and not the entire population.
</p>

<hr>

<h2>4. Project Objectives</h2>

<ul>
  <li>Perform <strong>Data Cleaning and Preprocessing</strong></li>
  <li>Handle missing or invalid values</li>
  <li>Apply Machine Learning classification algorithms</li>
  <li>Evaluate model performance using standard metrics</li>
  <li>Predict diabetes status for new input data</li>
</ul>

<hr>

<h2>5. Limitations</h2>

<ul>
  <li><strong>Gender Limitation:</strong> Includes only female patients. Results may not generalize to males.</li>
  <li><strong>Ethnic Limitation:</strong> Data represents one specific ethnic group only.</li>
  <li><strong>Age Restriction:</strong> Applicable only to individuals aged 21 and above.</li>
  <li><strong>Limited Feature Scope:</strong> Lifestyle and other health factors are not included.</li>
  <li><strong>Zero Values:</strong> Some features contain unrealistic zero values that require preprocessing.</li>
</ul>

<hr>

<h2>6. Conclusion</h2>

<p>
This project demonstrates the structured application of 
<strong>Machine Learning in healthcare prediction</strong>. 
However, due to dataset constraints, model results should be interpreted 
carefully and not considered as a medical diagnosis.
</p>
