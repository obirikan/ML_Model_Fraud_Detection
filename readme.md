# 💳 Logistic Regression Fraud Detection Project

This project demonstrates how to use **Logistic Regression** to detect fraudulent transactions using the `transactions.csv` dataset.

---

## 📂 Dataset

We assume the dataset `transactions.csv` contains financial transaction logs with features such as:

* `type`: transaction type (e.g., PAYMENT, DEBIT, CASH\_OUT, TRANSFER)
* `amount`: amount transferred
* `oldbalanceOrg` / `oldbalanceDest`: original balances before transaction
* `isFraud`: label (1 if fraud, 0 otherwise)

---

## ⚙️ Project Workflow

### 1. Load & Explore the Data

* Display the first few rows
* Check datatypes and missing values
* Describe the `amount` column for statistics

### 2. Feature Engineering

* **isPayment**: 1 if type is PAYMENT or DEBIT, else 0
* **isMovement**: 1 if type is CASH\_OUT or TRANSFER, else 0
* **accountDiff**: difference between origin and destination balances

### 3. Model Training

* **Features used**:

  * `amount`
  * `isPayment`
  * `isMovement`
  * `accountDiff`
* **Label**:

  * `isFraud`
* Data split: 70% training, 30% testing
* Normalize features using `StandardScaler`
* Train a `LogisticRegression` model

### 4. Model Evaluation

* Accuracy on training and test data
* Print the learned model coefficients

### 5. Fraud Prediction on New Data

Four new transactions are evaluated:

* `transaction1`, `transaction2`, `transaction3`, and `your_transaction`

We:

* Normalize them using the previously fit `StandardScaler`
* Predict whether each transaction is fraudulent
* Output prediction probabilities

---

## 📈 Example Output

```
Training accuracy: 0.98
Test accuracy: 0.97
Model coefficients: [[...]]
Predictions: [0 0 1 0]
Probabilities:
[[0.98 0.02]
 [0.95 0.05]
 [0.30 0.70]
 [0.97 0.03]]
```

---

## ✅ Libraries Used

* `pandas`, `numpy`
* `matplotlib`, `seaborn`
* `sklearn` (LogisticRegression, train\_test\_split, StandardScaler)

---

## 📎 How to Use

1. Clone the repo and add your `transactions.csv` file inside a `dataset/` folder
2. Run the script with your Python environment
3. Add your own transactions to test fraud detection

---

## 🧠 Main Stuff
* Feature engineering for fraud detection
* Building logistic regression from a real-world financial dataset
* Interpreting model coefficients and predictions
* Using sklearn's `predict_proba` for probability scores

---

## 📌 To-Do

* Add confusion matrix and classification report
* Try other models: Random Forest, XGBoost
* Handle class imbalance with oversampling / weighting

---

> beginner-friendly✨
