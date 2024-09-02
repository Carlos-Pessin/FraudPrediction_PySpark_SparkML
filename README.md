# FraudPrediction_PySpark_SparkML
Fraud Prediction Case using PySpark, SparkML

## Libraries
- Pyspark
- Pydequu - for quality assessment
- Ngrok - for performance assessment

# **PIX Transactions Analysis**

## Business Understanding
You work at a bank where the primary payment method used is Pix.

Using the Pix transaction database, the bank wants to understand the profile of customers who use Pix, as well as identify potential fraudulent transactions. However, there is one specific customer who has a very good relationship with the bank. Therefore, you have received the customer's transaction data for the past two years and need to create a report containing the main characteristics of these transactions.

To summarize, we have two main objectives for this case:

## Objectives
Clean and preprocess PIX transaction data
Analyze PIX usage patterns, such as the most used channels and the most common transaction values
Use PySpark MLlib to train and evaluate a fraud detection model
Evaluate the model's performance and provide recommendations for future improvements

## Data
The dataset includes the following information for each transaction:
- id_transacao: transaction ID;
- valor: value;
- remetente: sender data (name, bank, type);
- destinatario: recipient data (name, bank, type);
- categoria: transfer category;
- chave_pix: type of pix key;
- transaction_date;
- fraude: dataset label, is this a fraudulent transaction?
The dataset you will read is in JSON format.

## Tasks
### Exploratory Data Analysis:
Use PySpark to analyze PIX usage patterns:
- most used PIX keys;
- most common transaction values;
- distribution of transaction values by hour and day;
- which banks received the most transfers per day;
- to which type of person (PF or PJ) more transactions were made
- To which bank does this customer transfer the most?
- What is the number of transfers made by this customer over time?
- Based on the value of the transfers, could a credit increase be justified?
- What does this customer use transfers for the most?

### Data quality
Define at least five quality metrics for your data.

### Feature Engineering:
Present new features that may be useful for fraud detection, such as the number of transactions made by the same sender within a specific time period.

### Modeling:
Use PySpark MLlib to train and detect potential fraudulent transactions.

# Final report
We could found that this client has a large amount of transfers, especially for PJ accounts. He may be using his personal account for business purposes, we may approach him to get a better understanding/account.

It was possible to identify that all frauds were made in transfer category and were worth more than 10.000. Therefore, we recommend to reduce his fixed limit to avoid frauds. Whenever he needs to transfer this values he can manually unblock.

Our Machine Learning model detected all frauds and had only 3,3% of false alerts. It runs in less than 4s.





