🚀 Fraudulent Claims Detection Using SQL & Python

Detecting fraudulent insurance claims using SQL queries and data analysis.

🔍 Project Overview

This project analyzes insurance claims data to identify potential fraudulent claims.I use SQL for fraud detection, Python (pandas, matplotlib, seaborn) for visualization, and Jupyter Notebooks for analysis.

💁 Project Structure

fraudulent-claims-detection/
├── data/                  # Contains dataset
├── notebooks/             # Jupyter notebooks for EDA & SQL analysis
├── reports/               # Final summary report
├── scripts/               # Any Python helper scripts
├── README.md              # Project documentation
├── requirements.txt       # Required dependencies
└── LICENSE                # Open-source license

📂 Dataset Source

The dataset used in this project was sourced from Mendeley Data.

🔗 Link to Dataset: Fraudulent Claims Dataset - Mendeley Data

📝 Citation:Nnamoko, N., & Korkontzelos, I. (2019). Synthetic auto insurance dataset for fraud detection. Mendeley Data, V2. https://doi.org/10.17632/992mh7dk9y.2

📌 Usage Notice:This dataset is provided for research and educational purposes only. If you use this dataset in your project, ensure proper citation as per the original source guidelines.

📊 Key Insights & Findings

✅ Fraudulent Claims Rate: 📈 18.5% of claims in the dataset were flagged as fraudulent.

✅ High-Risk Incident Types: 🚗 Hit-and-run and theft had the highest fraud rate.

✅ Suspiciously High Claim Amounts: 💰 Claims over $15,000 were more likely to be fraudulent.

✅ Policy Deductibles & Fraud: Higher deductibles ($1,000+) had a 30% increase in fraud cases.

🗒️ Example SQL Query Used for Fraud Analysis

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

🔥 Challenges & Lessons Learned

🚧 Difficulties Encountered

🔹 Git & Version Control Issues: Faced initial difficulties with Git commands, tracking changes, and handling .gitignore.

🔹 Jupyter Notebook Errors: Encountered issues launching Jupyter Notebook and linking it properly to the virtual environment.

🔹 SQL Queries Debugging: Ran into missing column errors due to incorrect table schema and inconsistent column names.

🔹 Formatting README for GitHub: Ensuring proper markdown formatting (e.g., using triple backticks for code blocks).

🎯 How I Overcame These Challenges

✅ Resolved Git Issues: Learned proper Git workflow (git add, git commit, git push), staged files correctly, and fixed .gitignore.

✅ Fixed Jupyter Notebook Errors: Activated the virtual environment properly (source venv/Scripts/activate) and reinstalled dependencies.

✅ Debugged SQL Queries: Used PRAGMA table_info(insurance_claims); to inspect table structure and adjust column names accordingly.

✅ Mastered Markdown Formatting: Understood how GitHub renders markdown and formatted code blocks, headings, and bullet points correctly.

🎓 Key Takeaways

📌 GitHub & Version Control: Gained confidence in using Git commands, staging changes, and handling repositories.

📌 SQL Query Debugging: Learned how to check schema details, fix column mismatches, and optimize queries for accuracy.

📌 Markdown Best Practices: Understood how to format a professional README file for clear presentation and recruiter appeal.

📌 Perseverance & Learning: Most importantly, learned that problem-solving, patience, and continuous learning are crucial in real-world tech projects.

📩 Connect With Me

🔗 GitHub: github.com/bzmaggie

📧 Email: mjohnson@learnexcelgrow.org

🌟 LinkedIn: linkedin.com/in/margaretjohnson180 

