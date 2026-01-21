# 🩺 Diabetes Prediction - Logistic Regression Study

This repository contains the implementation and technical documentation of a **Logistic Regression** algorithm to classify the probability of a patient developing diabetes. The primary goal is to demonstrate how linear models are applied to binary classification problems.

## 🚀 Application Scenario
Logistic Regression is used to answer "Yes or No" questions:
* **Healthcare**: Does the patient have diabetes? (0 = No, 1 = Yes).
* **Finance**: Is this transaction fraudulent?
* **Marketing**: Is the customer likely to cancel their subscription (Churn)?

---

## 🧠 The Algorithm: Logistic Regression
**Logistic Regression** uses the logistic function (or sigmoid) to map any real-valued number into a range between 0 and 1.



[Image of sigmoid function graph]


* **Probability**: The model outputs a decimal value (e.g., 0.85).
* **Threshold**: We define that if the probability is > 0.5, the class is "1" (Diabetes).
* **Cross-Entropy (Log Loss)**: This is the cost function that Scikit-Learn minimizes to adjust variable weights during training.

---

## 🛠️ Tech Stack
* **Python 3.x**
* **Pandas**: Data manipulation.
* **Scikit-Learn**: Machine Learning library.
* **Matplotlib / Seaborn**: Data visualization.
* **Jupyter Notebook**: Development environment.

---

## 📊 Model Performance & Evaluation
Key classification metrics differ from standard regression. In this study, we focus on:

* **Accuracy**: The ratio of correct predictions to total predictions.
* **Confusion Matrix**: A table showing where the model confused "False Positives" with "False Negatives."



### Key Insights from Step 6:
Based on the model evaluation:
1. **Overall Accuracy (75%)**: The model has solid global performance, but accuracy alone can hide failures in specific disease detection.
2. **True Negatives (78)**: The model is very good at identifying healthy patients.
3. **True Positives (37)**: The model successfully detected 37 real cases of diabetes.
4. **False Negatives (18)**: This is the most critical area; these are sick people the model considered healthy.
5. **Recall (0.67)**: Of all actual diabetics, the model found 67%, suggesting a "conservative" diagnostic approach.

---
## ⚙️ How to Run in Visual Studio Code

Since the project uses a fixed dependency file (`freeze`), follow these steps to set up your environment:

1.  **Clone the repository**:
2.  **Create and Activate a Virtual Environment (VENV)**:
    ```bash
    python -m venv venv
    # On Windows: .\venv\Scripts\activate
    # On Mac/Linux: source venv/bin/activate
    ```
3.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
4.  **Select the Kernel**: In VS Code, open the `.ipynb` file, click on **"Select Kernel"** in the top right corner, and choose the `venv` environment you just created.

---

## 📊 How to Run in Google Colab
1.  Access [Google Colab](https://colab.research.google.com/).
2.  Go to `File > Upload Notebook` and upload the `.ipynb` file from this repository.
3.  Colab comes with the necessary libraries pre-installed; simply run the cells.