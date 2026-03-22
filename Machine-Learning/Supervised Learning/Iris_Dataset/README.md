#  Iris Classification using Logistic Regression

##  Overview

This project focuses on classifying iris flowers into three species  **Setosa, Versicolor, and Virginica** using machine learning techniques.

The dataset used is the classic **Iris dataset**, which is widely known for its simplicity and well-separated classes, making it ideal for classification tasks.

---

##  Dataset Description

The dataset contains **150 samples** with **4 features**:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

###  Target Variable

* Species (3 classes):

  * Setosa
  * Versicolor
  * Virginica

---

##  Approach

We implemented a machine learning pipeline consisting of:

* **StandardScaler** -> for feature scaling
* **Logistic Regression (Elastic Net)** -> for classification

```python
Pipeline(steps=[
    ('scaler', StandardScaler()),
    ('lg', LogisticRegression(penalty='elasticnet', solver='saga'))
])
```

---

##  Model Selection

We experimented with Logistic Regression using Elastic Net regularization.

* Hyperparameters tuned:

  * `C`
  * `l1_ratio`
  * `penalty = elasticnet`
  * `solver = saga`

---

##  Results

* Cross-validation accuracy: **~92%**
* Test set performance:

  * Precision: **1.0**
  * Recall: **1.0**
  * F1-score: **1.0**

 The model achieved **perfect classification on the test set**.

---

##  Why Only Logistic Regression?

Although multiple models can be applied, we **stopped at Logistic Regression** because:

* The dataset is **linearly separable**
* Logistic Regression already achieved **perfect performance (100%)**
* More complex models were **unnecessary**
* Using simpler models improves:

  * Interpretability
  * Efficiency
  * Generalization

 Therefore, further model experimentation was not required.

---

##  How to Use (Prediction)

Example for making predictions:

```python
import numpy as np

user_data = np.array([[5.1, 3.5, 1.4, 0.2]])
prediction = model.predict(user_data)

labels = ['setosa', 'versicolor', 'virginica']
print("Flower is:", labels[prediction[0]])
```

---

##  Conclusion

Logistic Regression with proper preprocessing is sufficient to achieve **excellent performance** on the Iris dataset.

This project demonstrates that:

* Simpler models can outperform expectations
* Understanding data is more important than using complex algorithms

---

##  Technologies Used

* Python
* NumPy
* Pandas
* Scikit-learn


---

##  Key Takeaway

> **Always start with simple models - if they work perfectly, there is no need to overcomplicate.**

---

