# 📟 Fraudulent Claims Detection

This project applies exploratory data analysis and SQL pattern matching to identify potentially fraudulent insurance claims. It demonstrates foundational data analytics skills using Python, Pandas, SQL, and real-world-like datasets.

---

## 📌 Project Objectives

- Clean and preprocess raw insurance claims data
- Explore data relationships and identify suspicious patterns
- Engineer new features to help distinguish fraud vs. non-fraud
- Visualize insights using Pandas, Seaborn, and Matplotlib
- Deliver reproducible analysis via Jupyter Notebooks and SQL queries

---

## 🔀 Dataset Source

The dataset used in this project was sourced from Mendeley Data.

- 🔗 [Fraudulent Claims Dataset - Mendeley Data](https://doi.org/10.17632/992mh7dk9y.2)
- 📉 Citation: Nnamoko, N., & Korkontzelos, I. (2019). Synthetic auto insurance dataset for fraud detection. Mendeley Data, V2. https://doi.org/10.17632/992mh7dk9y.2
- 📌 Usage Notice: This dataset is provided for research and educational purposes only. If you use this dataset in your project, ensure proper citation as per the original source guidelines.

---

## 🔧 Tools & Technologies Used

- **Python** (Pandas, NumPy)
- **SQL** (SQLite for fraud pattern analysis)
- **Jupyter Notebook**
- **Matplotlib & Seaborn** (for data visualization)
- **GitHub** (for version control and sharing)

---

## 📁 Folder Structure

```
fraudulent-claims-detection/
│
├── data/                  # Contains the original CSV dataset
├── notebooks/             # Jupyter notebooks with analysis and SQL queries
├── LICENSE
├── .gitignore
└── README.md              # Project overview and instructions
```
---

## 🖼️ Key Output Snapshots

- 📊 [EDA Notebook](https://github.com/Margaret-Johnson-ai/fraudulent-claims-detection/blob/main/notebooks/EDA.ipynb) — Includes fraud rate visualization, bar charts, and correlation heatmaps.

- 🧾 [SQL Analysis Notebook](https://github.com/Margaret-Johnson-ai/fraudulent-claims-detection/blob/main/notebooks/SQL_Analysis.ipynb) — Shows fraud detection query logic and SQL result tables.

---

## 🔍 Key Insights & Findings

- 📊 **Fraudulent Claims Rate**: 18.5% of claims in the dataset were flagged as fraudulent
- 🚗 **High-Risk Incident Types**: Hit-and-run and theft had the highest fraud rates
- 💰 **Suspiciously High Claim Amounts**: Claims over $15,000 were more likely to be fraudulent
- 🛋️ **Policy Deductibles & Fraud**: Higher deductibles ($1,000+) showed a 30% increase in fraud cases

---

## 🗒️ Example SQL Query Used for Fraud Analysis

```sql
SELECT policy_deductable,
       COUNT(*) AS total_claims,
       SUM(CASE WHEN fraud_reported = 'Y' THEN 1 ELSE 0 END) AS fraudulent_cases,
       (SUM(CASE WHEN fraud_reported = 'Y' THEN 1 ELSE 0 END) * 100.0) / COUNT(*) AS fraud_rate
FROM insurance_claims
GROUP BY policy_deductable
ORDER BY fraud_rate DESC;
```

---

## 🚀 How to Use This Project

1. Clone the Repository

```bash
git clone https://github.com/Margaret-Johnson-ai/fraudulent-claims-detection.git
cd fraudulent-claims-detection
```

2. Install Dependencies

```bash
pip install -r requirements.txt
```

3. Open Jupyter Notebooks

```bash
jupyter notebook
```
- Run `EDA.ipynb` to explore the dataset
- Run `SQL_Analysis.ipynb` to execute fraud detection queries

---

## 📚 Challenges & Lessons Learned

### ⚠️ Difficulties Encountered
- Git & Version Control Issues: Initial confusion with Git commands and `.gitignore`
- Jupyter Notebook Errors: Problems launching the notebook within the virtual environment
- SQL Query Debugging: Encountered errors due to incorrect column names and schema structure
- Markdown Formatting: Learned to properly format professional README files

### ✅ How I Overcame Them
- Learned proper Git workflow (`add`, `commit`, `push`), resolved staging errors
- Activated virtual environment properly (`source venv/Scripts/activate`) and managed packages
- Used `PRAGMA table_info()` to debug SQL structure and fixed schema mismatches
- Practiced markdown syntax for clear formatting, headers, and code blocks

---

## 🎓 Key Takeaways

- 📚 **Version Control**: Gained confidence using Git commands to manage projects
- 📈 **SQL Debugging**: Learned to analyze and fix schema-based query errors
- 📄 **README Writing**: Understood how to present technical projects clearly for recruiters
- ✨ **Persistence Pays Off**: Learned that overcoming frustration leads to real growth in tech projects

---

## 👩‍💻 Author

**Margaret Johnson**  
[GitHub Profile](https://github.com/Margaret-Johnson-ai) | [LinkedIn](https://www.linkedin.com/in/margaretjohnson)
