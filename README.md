
# Transaction Analysis
Fraud analysis is crucial due to the rising incidence of fraud in transactions, aiming to detect patterns and anomalies. It helps mitigate risks, ensuring financial security and compliance with regulations. Enhancing customer trust is vital by demonstrating a commitment to secure transactions. Operational efficiency improves through streamlined processes and resource optimization. The financial industry faces challenges with the increasing complexity of digital transactions. Data-driven insights enable informed decisions for continuous improvement in fraud prevention. Adaptation to evolving threats is essential to stay ahead in the dynamic landscape of financial transactions.

# Procedure 
## How we proceed the Transaction Fraud analysis.
### Data Exploration

**Step 1: Uniques & NAs**

**Objective:** To know if there is any duplicate data and if at all there are any missing values.

* Unique Values:

 1.Pick out how many different values each column has.
 

* Null Values:

 1.Check whether the fields have missing data in them or not.

 2.Find out if the missing data is important in our analysis.

**Step 2: Distribution Among Classes**

**Objective:** Check percentage split between normal and fraud transactions.

* Class Distribution:

 1.Number of classes represented by transactions needs to be counted.

 2.Make a bar graph that simply shows how different normal transactions are from fraud cases graphically represented by a bar    chart.

**Step 3: Amount Transfer Per Class**

**Objective: How much money is involved in various types of transactions?**

* Amount Distribution:

 1.Adding up the amounts for each group is essential.

 2.Show on a bar chart what would be the financial impact of fraud versus normal transactions.

**Step 4: Distribution Among Classes for Flagged Fraud**

**Objective:** Transactions identified as frauds through flagging

* Flagged Fraud Distribution:

 1.Find out how many among the given number of cases were flagged as fraud by an existing system.

 2.Revisit class distribution methodology while considering flagged fraud.
 
**Step 5: Amount Transfer Per Class for Flagged Fraud**
**Objective:** Understand the money involved in transactions flagged as fraud.

* Flagged Fraud Amount Distribution:
 1.Sum up the amounts for transactions flagged as fraud.
 2.Visualize with a bar chart to see the financial impact of flagged fraud transactions.

**Step 6: Cash Flows from Various Transactions**
**Objective:** Understand how money moves around in different types of transactions.

* Cash Flow Analysis:
 1.Look at the flow of money for each type of transaction.
 2.Identify patterns and anomalies in the movement of funds.

**Step 7: Major Types Involved in Fraud**
**Objective:** Identify the main types of transactions associated with fraud.

* Fraud Type Identification:
 1.Analyze which types of transactions are frequently associated with fraud.
 2.Identify patterns or common characteristics of fraudulent transactions.
 
**Step 8: Concise Data - Remove Unwanted Columns**
**Objective:** Streamline the dataset by removing unnecessary columns.

* Identify Unwanted Columns:

 1.Look for columns that do not contribute significantly to the analysis or contain redundant information.

**Step 9: Likelihood of Fraud - Recipient vs. Initiator**
**Objective:** Understand if the recipient or initiator of a transaction is more likely to engage in fraud.

* Fraud Likelihood Analysis:

 1.Consider creating a new feature indicating whether the recipient or initiator is involved in the fraud.
   Analyze the distribution of fraud cases based on this new feature.
* Visualize the Results:

 1.Use visualizations bar charts to compare the likelihood of fraud between recipients and initiators.
   This provides insight into which party is more frequently associated with fraudulent activities.
   
### Accuracy by existing Fraud detector

Evaluate the performance of the current fraud detector using custom accuracy functions and a confusion matrix. Identify True Positives (TP), True Negatives (TN), False Positives (FP), and False Negatives (FN). Utilize custom functions for Accuracy, Precision, Recall, and F1 Score. Create a confusion matrix for visual representation. Apply the fraud detector to a test set and calculate accuracy metrics to gain insights into its effectiveness.

### Data Pre-Processing
Perform the nessesary processing on data to make data ready for ML Models.

### Generating Sample Data from the fraud data 
Generating sample data from fraud data is done to expedite the training of machine learning models and streamline the fine-tuning process.
By using a sample, machine learning models can be trained more efficiently and fine-tuned with less computational burden, while still capturing the essential characteristics of the data.

### ML Models
#### Train ML models for better Fraud detections.
##### Algorithm used :
**1. KNN**

**2. SVM**

**3. Logistic Regression**

**4. Random Forest Classification**

### Train the Best Performing Models on Entire Dataset.
##### Finally we Trained The best performing model on the entire dataset and obtain a better performing fraud detector than the exsisting one.


# Summary

### Distribution of Classes:
* The majority of transactions are normal (non-fraudulent), indicating a class imbalance.
* The percentage of fraud transactions is notably low, emphasizing the rarity of fraudulent activities.

### Cashflow Analysis:
* The analysis reveals that the largest sum of money flows through Transfer and Cash-out transactions.
* Cash-ins and Payments follow, with significantly lower amounts involved.
  Debit transactions have the least monetary flow.
  
### Amount Transfer Range:
* Fraud analysis indicates that fraudulent transactions often occur within a lower total amount transfer range.
* Understanding this pattern can aid in setting thresholds for anomaly detection and enhancing fraud prevention measures.

### Transaction Types Involved in Frauds:
* Only two transaction types, Transfer (4116 instances) and Cash-out (4097 instances), are associated with fraud.
* Both types occur with similar frequencies, suggesting a potential pattern in fraudulent activities related to these transaction types.

### Recipient Analysis in Frauds:

* Examining fraud occurrences reveals whether fraud tends to occur more frequently on the recipient side.
* It investigates whether recipients receive less or more money than expected, shedding light on potential patterns in fraudulent activities.

### Accuracy of Existing Fraud Detector:

* The existing fraud detection model exhibits low accuracy, as it tends to classify nearly every transaction as valid.
* The model's performance raises concerns about its effectiveness in distinguishing between fraudulent and legitimate transactions.

### Performance of ML Models:

* Out of four ML models evaluated, Random Forest demonstrates the highest accuracy.
* On the sample dataset, Random Forest achieves an accuracy of 99.93%, while on the entire dataset, it maintains a high accuracy of 99.76%.
* The superior performance of Random Forest suggests its effectiveness in accurately classifying transactions in this context.

