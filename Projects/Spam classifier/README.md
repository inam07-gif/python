<h1>📩 Spam Message Classifier</h1>

<h2>📌 Overview</h2>
<p>
This project implements a machine learning–based spam message classification system.
The objective is to automatically identify whether a given text message is 
<strong>Spam</strong> or <strong>Ham (Not Spam)</strong> using Natural Language Processing (NLP) techniques and supervised learning.
The model is trained on labeled data and supports prediction for new user-input messages.
</p>

<hr>

<h2>🚀 Key Features</h2>
<ul>
<li>Accepts raw text message as input</li>
<li>Performs structured text preprocessing</li>
<li>Transforms text into numerical features using TF-IDF</li>
<li>Classifies messages as <strong>Spam</strong> or <strong>Not Spam</strong></li>
<li>Provides probability-based predictions</li>
</ul>

<hr>

<h2>⚙️ Project Workflow</h2>

<h3>1️⃣ Text Preprocessing</h3>
<ul>
<li>Convert text to lowercase</li>
<li>Remove punctuation and special characters</li>
<li>Tokenization</li>
<li>Stopword removal</li>
<li>Stemming</li>
</ul>

<h3>2️⃣ Feature Extraction – TF-IDF</h3>
<p>
TF-IDF (Term Frequency–Inverse Document Frequency) converts cleaned text into 
weighted numerical vectors, highlighting important words while reducing the impact of common terms.
</p>

<h3>3️⃣ Model Training</h3>
<p>
The system uses <strong>Multinomial Naive Bayes</strong>, selected for its efficiency,
performance on sparse text data, and strong precision in spam detection tasks.
</p>

<h3>4️⃣ Probability-Based Prediction</h3>
<ul>
<li>Outputs spam and ham probabilities</li>
<li>Applies configurable decision threshold</li>
<li>Improves control over false positives and false negatives</li>
</ul>

<h3>5️⃣ User Input Support</h3>
<ul>
<li>Accepts custom messages</li>
<li>Returns classification result</li>
<li>Displays spam probability score</li>
</ul>

<hr>

<h2>🛠 Technologies Used</h2>
<ul>
<li><strong>Python</strong></li>
<li><strong>scikit-learn</strong></li>
<li><strong>NLTK</strong></li>
<li><strong>pandas</strong></li>
<li><strong>NumPy</strong></li>
</ul>

<hr>

<h2>📊 Conclusion</h2>
<p>
This project demonstrates how classical machine learning techniques, combined with structured NLP preprocessing and feature engineering,
can effectively solve real-world spam detection problems. Multinomial Naive Bayes proved to be a reliable, interpretable, and computationally efficient model for this task.
</p>
