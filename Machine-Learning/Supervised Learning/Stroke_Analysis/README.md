
<h1 align="center">Stroke Prediction using Machine Learning</h1>

<hr>

<h2>Project Overview</h2>

This project focuses on predicting the likelihood of a <b>stroke</b> using machine learning models.  
The dataset contains demographic and medical information of patients, and the goal is to build models that can effectively identify individuals at risk of stroke.

Since the dataset is <b>highly imbalanced</b> (very few stroke cases compared to non-stroke cases), special techniques such as <b>SMOTE</b>, <b>pipelines</b>, and <b>threshold tuning</b> were used to improve model performance.

<hr>

<h2>Dataset Description</h2>

The dataset contains various health-related and demographic features.

<b>Features include:</b>

<ul>
<li>Gender</li>
<li>Age</li>
<li>Hypertension</li>
<li>Heart Disease</li>
<li>Ever Married</li>
<li>Work Type</li>
<li>Residence Type</li>
<li>Average Glucose Level</li>
<li>BMI</li>
<li>Smoking Status</li>
</ul>

<b>Target Variable:</b>

<ul>
<li>0 → No Stroke</li>
<li>1 → Stroke</li>
</ul>

<hr>

<h2>Project Workflow</h2>

The machine learning pipeline followed these steps:

<ol>
<li>Exploratory Data Analysis (EDA)</li>
<li>Handling missing values</li>
<li>Feature encoding using OneHotEncoder</li>
<li>Feature scaling</li>
<li>Handling class imbalance using SMOTE</li>
<li>Building machine learning pipelines</li>
<li>Hyperparameter tuning using GridSearchCV</li>
<li>Model evaluation and comparison</li>
<li>Probability threshold tuning</li>
</ol>

<hr>

<h2>Preprocessing Techniques</h2>

To ensure proper model training, the following preprocessing steps were applied:

<ul>
<li><b>SimpleImputer</b> – Handling missing values</li>
<li><b>OneHotEncoder</b> – Encoding categorical features</li>
<li><b>Feature Scaling</b> – Required for distance-based models</li>
<li><b>SMOTE</b> – Handling class imbalance</li>
<li><b>ColumnTransformer</b> – Applying transformations to different feature groups</li>
<li><b>Pipelines</b> – Preventing data leakage and organizing preprocessing steps</li>
</ul>

<hr>

<h2>Machine Learning Models Used</h2>

Several machine learning algorithms were tested and compared:

<ul>
<li>Logistic Regression</li>
<li>Decision Tree</li>
<li>Random Forest</li>
<li>Support Vector Machine (SVC)</li>
<li>K-Nearest Neighbors (KNN)</li>
</ul>

Hyperparameter tuning was performed using <b>GridSearchCV</b>.

<hr>

<h2>Handling Imbalanced Data</h2>

The dataset contained significantly fewer stroke cases.  
To address this issue, the following technique was used:

<b>SMOTE (Synthetic Minority Over-sampling Technique)</b>

This method generates synthetic examples of the minority class to improve model learning.

<hr>

<h2>Model Evaluation</h2>

Model performance was evaluated using:

<ul>
<li>Accuracy</li>
<li>Precision</li>
<li>Recall</li>
<li>F1-score</li>
</ul>

Special attention was given to <b>recall for the stroke class</b>, as detecting stroke cases is more important than maximizing overall accuracy.

<hr>

<h2>Model Comparison</h2>

<table border="1">
<tr>
<th>Model</th>
<th>Accuracy</th>
<th>Precision (Stroke)</th>
<th>Recall (Stroke)</th>
<th>Observation</th>
</tr>

<tr>
<td>Logistic Regression</td>
<td>~0.90</td>
<td>Low</td>
<td>Low–Moderate</td>
<td>Struggles with minority class detection</td>
</tr>

<tr>
<td>Random Forest</td>
<td>~0.94</td>
<td>Very Low</td>
<td>Very Low</td>
<td>Strong bias toward majority class</td>
</tr>

<tr>
<td>SVC</td>
<td>0.90</td>
<td>0.226</td>
<td>0.237</td>
<td>Poor stroke detection</td>
</tr>

<tr>
<td><b>KNN</b></td>
<td><b>0.83</b></td>
<td><b>0.188</b></td>
<td><b>0.50</b></td>
<td><b>Best detection of stroke cases</b></td>
</tr>

</table>

<hr>

<h2>Key Insights</h2>

<ul>
<li>The dataset is highly imbalanced.</li>
<li>Accuracy alone is not a reliable metric.</li>
<li>Recall for stroke cases is the most important metric.</li>
<li>KNN detected the highest number of stroke cases.</li>
</ul>

<hr>

<h2>Final Conclusion</h2>

Among the evaluated models, <b>K-Nearest Neighbors (KNN)</b> demonstrated the best performance in identifying stroke cases.  
Although its overall accuracy was slightly lower, it achieved a significantly higher recall for the minority class, making it more suitable for medical risk prediction.

<hr>

<h2>Technologies Used</h2>

<ul>
<li>Python</li>
<li>Pandas</li>
<li>NumPy</li>
<li>Matplotlib</li>
<li>Seaborn</li>
<li>Scikit-learn</li>
<li>Imbalanced-learn</li>
</ul>

<hr>

<h2>Future Improvements</h2>

Possible improvements for the project include:

<ul>
<li>ROC Curve analysis</li>
<li>Precision–Recall Curve</li>
<li>Feature importance analysis</li>
<li>Advanced ensemble models (XGBoost / LightGBM)</li>
<li>Model deployment</li>
</ul>

<hr>

<h3 align="center">Machine Learning Project – Stroke Prediction Analysis</h3>
