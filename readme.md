
# 💳 Logistic Regression Fraud Detection 

This dataset provides a small but representative sample of anonymized financial transactions intended for building and testing **fraud detection models**.

Each record represents a **single transaction**, including:
- Transaction type (e.g., `CASH_OUT`, `TRANSFER`)
- Transaction amount
- Sender and receiver account balances before and after the transaction
- Fraud indicator flags

It is suitable for:
- Binary classification
- Anomaly detection
- Machine learning tasks related to **financial security**

---

## 📦 Dataset Structure

| Column Name     | Description                                                  |
|------------------|--------------------------------------------------------------|
| `step`           | Time step of the transaction                                 |
| `type`           | Type of transaction (e.g., `TRANSFER`, `CASH_OUT`)           |
| `amount`         | Amount involved in the transaction                           |
| `nameOrig`       | ID of sender account                                         |
| `oldbalanceOrg`  | Sender’s balance before the transaction                      |
| `newbalanceOrig` | Sender’s balance after the transaction                       |
| `nameDest`       | ID of receiver account                                       |
| `oldbalanceDest` | Receiver’s balance before the transaction                    |
| `newbalanceDest` | Receiver’s balance after the transaction                     |
| `isFraud`        | **Target variable**: 1 if fraudulent, 0 otherwise            |
| `isPayment`      | Indicates if the transaction is a payment                    |
| `isMovement`     | Indicates if it involved a balance change                    |
| `accountDiff`    | Difference in account balances (derived feature)             |

---

## ⚠️ Class Imbalance Notice

> **Important:**  
> This dataset is **highly imbalanced** — the number of fraudulent transactions (`isFraud = 1`) is much lower compared to non-fraudulent ones.  
> This reflects real-world financial data and may affect model performance if not handled properly.

To improve results, consider:
- **Resampling techniques** like SMOTE or undersampling
- Using **evaluation metrics** like precision, recall, F1-score, or ROC-AUC instead of just accuracy

---

## 💡 Inspiration

This dataset can help you explore:
- How fraud differs from legitimate behavior
- Techniques to detect rare but critical patterns
- How to evaluate models fairly when fraud is rare

---


