# 📘 Revenue Leakage Detection & 3-Way Reconciliation System
Identifying Missing Settlements, Refund Errors & Anomalies in Digital Payments

This project implements a finance-grade reconciliation and revenue-leakage detection workflow using Python and machine learning.
It mirrors real operational challenges in African digital ecosystems where payments, settlements, and refunds sit in different systems, creating opportunities for:

- Lost revenue

- Over-refunds

- Duplicate refunds

- Refunds applied to failed transactions

- Misallocated customer accounts

- Fraud and process failures

The system turns scattered financial data into structured, auditable, decision-ready insights.

---

# Key Features
## 1. Full 3-Way Reconciliation

Compares:

- payments_system.xlsx

- bank_statement.xlsx

- refunds.xlsx

Detects:

- Missing settlements

- Amount mismatches

- Payments without settlement

- Refunds without originating transactions

---

##2. Revenue Leakage Detection

Flags and quantifies:

- Over-refunds

- Refunds on failed transactions

- Unmatched refunds

- Duplicate refunds

- Misallocated refunds

- Suspiciously large refunds (rule-based)

Outputs exported as Excel/CSV for finance & audit teams.

---

## 3. Machine Learning: Refund Anomaly Detection

Using Isolation Forest on engineered features:

- Refund ratio

- Time-to-refund duration

- Channel code

- Amount deviation

Produces:

    anomaly_top20.csv

    refunded_with_anomalies.csv

---

## 4. Financial Waterfall Summary

Shows overall flow:

- Total processed

- Total refunds

- Missing settlements

- Net collected revenue

      Folder Structure
      /data               → raw inputs  
      /notebooks          → Jupyter workflows  
      /outputs            → generated reports  
      /src                → future Python scripts  
      README.md
      requirements.txt
      .gitignore

--- 

# Notebooks
    02_reconciliation.ipynb

- Loads & standardizes raw datasets

- Detects missing settlements

- Flags refund issues

- Produces waterfall and summary files

      03_leakage_detection.ipynb

- Duplicate refund detection

- Misallocation checks

- Suspicious refund rule checks

- Isolation Forest anomaly scoring

--- 

📂 Sample Outputs (from /outputs)

    missing_settlements.xlsx
    
    reconciliation_summary.xlsx
    
    refunded_detailed.xlsx
    
    refunds_unmatched.xlsx
    
    duplicate_refunds_summary.csv
    
    refunds_misallocated.csv
    
    suspicious_refund_amounts.csv
    
    revenue_waterfall.csv
    
    anomaly_top20.csv

---

▶️ How to Run Locally

Clone this repository:

    git clone https://github.com/YOUR-USERNAME/revenue-leakage-detection.git
    cd revenue-leakage-detection
    

Install dependencies:

    pip install -r requirements.txt


Place your raw .xlsx files in /data.

Run notebooks:

    /notebooks/02_reconciliation.ipynb
    /notebooks/03_leakage_detection.ipynb


View outputs under /outputs.

    Requirements
    pandas
    numpy
    scikit-learn
    openpyxl

--- 

Why This Project Matters

African organizations—especially those running digital payments—face:

- Fragmented systems

- Poor settlement visibility

- Manual refund processing

- Weak governance and audit trails

This project shows how to turn that chaos into:

✔️ Clean reconciled datasets
✔️ Leakage quantification
✔️ Finance-friendly reports
✔️ Machine-learning-driven anomaly detection
✔️ A pipeline that can be automated into production

👩🏽‍💻 About the Author
Joy Mukami — Data Analyst (Finance & Nonprofit Systems)
Passionate about transforming messy operational data into clean insights that improve accountability, revenue assurance, and decision-making for African organizations.
