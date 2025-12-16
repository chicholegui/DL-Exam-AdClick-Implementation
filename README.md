# Deep Learning Exam: Ad Click Prediction 📝➡️💻

Code implementation of the neural network architecture designed during my written Deep Learning exam.

---

**🛠 Tech Stack:** ![Python](https://img.shields.io/badge/Python-3.x-blue) ![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange) ![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)

## 🎓 About This Project

This repository contains the practical part of my **University Deep Learning Exam**.

The exam format was:
1.  **Written Part:** I was given the *Ad Click* dataset statistics (features, imbalance, etc.) and had to **manually design** a Neural Network on paper to solve it. I had to justify every layer, activation function, and regularization choice without running any code.
2.  **Implementation (This Notebook):** After handing in the paper, I had to code exactly what I designed using **Keras/TensorFlow** to prove it worked.

## 📓 What's in the Notebook

*   **Data Analysis:** Quick check of the features I analyzed on paper.
*   **Preprocessing:** Converting the dataset into the tensor format I planned.
*   **The Model:** The exact architecture I wrote down in the exam (MLP with Dropout).
*   **Results:** Training logs showing how the "paper design" performed in reality.

It's a straightforward implementation, kept exactly as it was submitted for grading.

## 💡 Key Learnings & Methodology

This project demonstrates specific competencies in Applied Deep Learning:

*   **Metric Selection for Imbalanced Data:** Given the dataset's class skew, I moved beyond standard *Accuracy* metrics. I implemented **Precision, Recall, and F1-Score** monitoring to ensure the model wasn't just predicting the majority class.
    *   *Result:* Achieved a balanced **F1-Score of 0.83** and **Accuracy of 82%** on the test set, proving the model learned the minority class patterns effectively.
*   **Temporal Feature Engineering:** Raw timestamps are rarely useful in Neural Networks. I decomposed time data into cyclical features (*Hour, Day of Week, Month*) to capture user behavior patterns, transforming a noise feature into a predictive signal.
*   **Architecture Design:** Bridging theory and practice, I manually calculated layer dimensions to validate the Keras implementation, ensuring the tensor shapes (310 features -> Hidden Layers -> Scalar Output) aligned perfectly with the theoretical design.
