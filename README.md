# 🚀 Fraudulent Claims Detection Using SQL & Python  
Detecting fraudulent insurance claims using SQL queries and data analysis.

---

## 🔍 Project Overview  
This project analyzes **insurance claims data** to identify potential **fraudulent claims**.  
We use **SQL for fraud detection**, **Python (pandas, matplotlib, seaborn) for visualization**, and **Jupyter Notebooks for analysis**.

---

## 📁 Project Structure  


---

## 📊 Key Insights & Findings  
✅ **Fraudulent Claims Rate**: 📈 **18.5%** of claims in the dataset were flagged as fraudulent.  
✅ **High-Risk Incident Types**: 🚗 **Hit-and-run** and **theft** had the highest fraud rate.  
✅ **Suspiciously High Claim Amounts**: 💰 Claims over **$15,000** were more likely to be fraudulent.  
✅ **Policy Deductibles & Fraud**: Higher deductibles (**$1,000+**) had a **30% increase in fraud cases**.  

### 📝 Example SQL Query Used for Fraud Analysis:
```sql
SELECT 
    policy_deductable, 
    COUNT(*) AS total_claims, 
    SUM(CASE WHEN fraud_reported = 'Y' THEN 1 ELSE 0 END) AS fraudulent_cases,
    (SUM(CASE WHEN fraud_reported = 'Y' THEN 1 ELSE 0 END) * 100.0) / COUNT(*) AS fraud_rate
FROM insurance_claims
GROUP BY policy_deductable
ORDER BY fraud_rate DESC;


⚡ Technologies Used
SQL (SQLite) → For fraud pattern analysis
Python (pandas, matplotlib, seaborn) → For data visualization
Jupyter Notebook → For interactive analysis
GitHub → For version control and project management


🚀 How to Use This Project

1️⃣ Clone the Repository

git clone https://github.com/bzmaggie/fraudulent-claims-detection.git
cd fraudulent-claims-detection

2️⃣ Install Dependencies

pip install -r requirements.txt

3️⃣ Open Jupyter Notebooks

jupyter notebook
Run EDA.ipynb to explore the dataset.
Run SQL_Analysis.ipynb to execute fraud detection queries.
📄 Future Improvements
🔹 Machine Learning Model: Build a fraud detection model using ML algorithms.
🔹 API Integration: Create an API for real-time fraud detection.
🔹 Dashboard: Develop a dashboard to visualize fraud trends.

📩 Connect With Me
🔗 GitHub: github.com/bzmaggie
📧 Email: mjohnson@learnexcelgrow.org
💼 LinkedIn: linkedin.com/in/margaretjohnson180