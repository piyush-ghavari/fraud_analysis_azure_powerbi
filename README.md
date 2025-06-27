# Fraud_Analysis

This is a complete **end-to-end data analytics project** focused on detecting fraudulent credit card transactions.
Using real-world style transaction data, the project replicates how analysts identify patterns in fraud using cloud-integrated workflows and interactive dashboards.

The project simulates a financial institution’s effort to monitor, analyze, and prevent fraudulent behavior — through data exploration, trend analysis, and visual storytelling.

**Project Overview**
The goal of this project is to simulate how actual data analysts in the financial and banking sectors work behind the scenes to analyze transactions and detect fraud using cloud-based infrastructure and business intelligence tools.

In this end-to-end project, we:

✅ **Ingest real-world transaction data** and securely store it in **Azure Blob Storage**

✅ Use **Python** for **data exploration** and **data cleaning**, including handling nulls, fixing data types, and preparing the data for analysis

✅ Create a cleaned dataset and **upload it back to Azure** to establish a **cloud-based data pipeline**

✅ Use **Power BI** to develop an interactive dashboard that enables users to filter by fraud status, merchant category, and more

✅ Derive **business-driven fraud insights**, including high-risk months, customer demographics, merchant risk, and payment vulnerabilities


## 📦 Dataset Overview

The dataset contains **transaction-level credit card data** used for fraud analysis.  
Each row represents a single transaction along with customer demographics, merchant details, transaction timestamp, and fraud label.

### 🔑 Key Columns:

| Column Name                  | Description |
|-----------------------------|-------------|
| `merchant_name`             | Name of the merchant involved in the transaction |
| `merchant_category`         | Category/type of merchant |
| `transaction_amount`        | Amount spent in the transaction |
| `customer_gender`           | Gender of the customer (`Male`/`Female`) |
| `customer_city`             | City where the customer resides |
| `city_population`           | Population of the customer's city |
| `customer_job`              | Occupation of the customer |
| `fraud_status`              | Indicates whether the transaction was fraudulent (`1` = fraud, `0` = non-fraud) |
| `transaction_year`          | Year of the transaction |
| `transaction_month`         | Month of the transaction |
| `transaction_day`           | Day of the transaction |
| `transaction_hour`          | Hour of the transaction |
| `transaction_minute`        | Minute of the transaction |
| `transaction_second`        | Second of the transaction |
| `date_of_birth_year`        | Customer's year of birth |
| `date_of_birth_month`       | Customer's birth month |
| `date_of_birth_day`         | Customer's birth day |
| `customer_state_state_full` | Full name of the customer's state |
| `customer_age`              | Age of the customer (derived from DOB) |

#🔧 Project Workflow

It follows an end-to-end analytics workflow — from raw data to business-ready insights.

  ### 1️ Raw File Upload to Azure Blob Storage
- The original CSV file was uploaded to a container in **Azure Blob Storage**
- This made the file accessible for cloud-based processing and dashboard development
- 
![Screenshot 2025-06-27 181725](https://github.com/user-attachments/assets/8fedcf54-8981-4161-88cb-8545fc84326a)

### 🧹2 Jupyter Notebook: Cleaning with Azure Integration

The complete data cleaning process was done using **Python in Jupyter Notebook**, which includes:

- 📥 Fetching raw data directly from Azure Blob Storage
- 🧼 Handling null values, fixing formats, and deriving new columns
- 📤 Uploading the cleaned dataset back to Azure for Power BI analysis

📄 **Notebook File**: [`credit_card_fraud_cleaning.ipynb`](./credit_card_fraud_cleaning.ipynb)
[Uploading Credit_card_fraud.ipynb…]()

📸 Azure + Python integration Preview:  
![Screenshot 2025-06-27 184102](https://github.com/user-attachments/assets/c436442d-ea1e-47dd-b21a-2f7ec69d6e76)

### 3️ Cleaned File Re-uploaded to Azure
- After cleaning, the final dataset was saved as a new CSV
- This cleaned file was re-uploaded to the **same Azure container** to keep the pipeline organized

  ![Screenshot 2025-06-27 184332](https://github.com/user-attachments/assets/59b19ec1-4e9d-46ec-9539-194c33ac25a4)

### 4️⃣ Power BI Dashboard Development
- Connected **Power BI** to Azure Blob Storage using built-in connectors
- ![Screenshot 2025-06-27 161541](https://github.com/user-attachments/assets/110fe2a9-543b-4243-b483-0ab279ba581e)
![Screenshot 2025-06-27 161727](https://github.com/user-attachments/assets/b11c75cd-8faa-45d9-bb9b-d541d3687be8)

- **Created an interactive dashboard**

![Screenshot 2025-03-08 212429](https://github.com/user-attachments/assets/8aee16cb-c1e4-479e-ac55-9fe9124f5aa3)


## Key Insights
- **Fraud Peaks in April-June & November**: Fraud rates are highest in these months.
- **Male Users Have Higher Fraud Rates**: More fraudulent transactions are linked to male users.
- **Certain Merchant Categories Are High-Risk**: Industries like *Material Engineering* have higher fraud occurrences.
- **Credit Cards Are More Vulnerable**: Fraud cases are more common in online credit card transactions.

## Recommendations
### 1- Address Seasonal Fraud Spikes
- Strengthen fraud detection measures during April-June and November.
- Implement AI-driven anomaly detection for real-time alerts.

### 2- Focus on High-Risk Demographics
- Increase security measures for male users based on fraud trends.
- Require additional authentication for suspicious transactions.

### 3- Secure High-Risk Merchant Categories
- Work with high-risk industries to improve security measures.
- Monitor transactions in Material Engineering & similar sectors closely.

### 4- Enhance Payment Security
- Promote two-factor authentication for online credit card transactions.
- Educate users on secure payment methods to prevent fraud.
