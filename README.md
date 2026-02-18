🔐 Cybersecurity Threat Detection using Deep Learning

🚀 End-to-end Deep Learning pipeline for anomaly detection in real-world cybersecurity data.

---

##  Project Overview

This project develops a Deep Learning model to detect cybersecurity threats using the **BETH Dataset**, a real-world anomaly detection dataset designed for cybersecurity research .

The objective is to classify system activity as **benign (0)** or **malicious (1)** using supervised learning techniques and evaluate model generalization across predefined dataset splits.

---

##  Dataset

* **Source:** BETH Dataset (Kaggle) 
* **Type:** Real-world cybersecurity anomaly detection data
* **Task:** Binary Classification (Threat Detection)
* **Provided Splits:**

  * Training Set
  * Validation Set
  * Testing Set

The dataset contains labeled system activity logs used to train and evaluate the neural network model.

---

##  Model Architecture

The model was implemented using a Deep Learning approach:

* Fully Connected Neural Network
* Binary Classification Framework
* Cross-Entropy-based Loss Function
* Optimizer-based Gradient Descent
* Train / Validation / Test pipeline
* Feature preprocessing and normalization

---

##  Technologies Used

* Python
* PyTorch
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

---

##  Model Performance

* **Training Accuracy:** 92.10%
* **Validation Accuracy:** 94.16%
* **Testing Accuracy:** 7.56%

The model achieves strong performance on training and validation data, demonstrating its ability to learn patterns from historical cybersecurity activity.

However, test performance drops significantly due to distribution differences across the provided dataset splits.

---

##  Dataset Distribution Misalignment

The provided train and validation sets contain predominantly **benign samples (class 0)**, whereas the test set contains a significantly higher proportion of **malicious samples (class 1)**.

This creates a **distribution shift** between training and testing environments.

As a result:

* The model primarily learns benign activity patterns.
* When evaluated on a test set dominated by malicious samples, overall accuracy declines.
* This reflects dataset misalignment rather than purely a model architecture limitation.
