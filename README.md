E‑Commerce Analytics Project
A complete end‑to‑end data analytics solution built using Python, MySQL, Streamlit, and Power BI. This project demonstrates how to clean raw e‑commerce data, load it into a SQL database, generate insights, create interactive dashboards, and manage the workflow using GitHub.
________________________________________
1. Project Overview
This project analyzes e‑commerce transactions to extract insights such as: - Revenue trends - Customer behavior - Product‑level performance - Geographic distribution of sales - Time‑based patterns
It includes: - Data Cleaning & Preprocessing - Database Setup in MySQL - Automated Data Loading Scripts - Interactive Streamlit Dashboard - Power BI Live Dashboard - Mock Data Generation for Testing
________________________________________
2. Directory Structure
ecom-analytics/
│
├── data/
│   └── ecom_dataset.csv
│
├── scripts/
│   ├── load_dataset.py
│   ├── load_to_mysql.py
│   ├── analyze_views.py
│   ├── dashboard.py
│   ├── generate_mock_sales.py
│   ├── check_dataset_quality.py
│   └── test_mysql_conn.py
│
├── mysqlworkbench/
│   ├── db creation.txt
│   └── user privileges.txt
│
├── README.md
└── requirements.txt
________________________________________
3. Technologies Used
•	Python 3.10+
•	MySQL 8+
•	Streamlit (Interactive Dashboard)
•	Power BI
•	Pandas, Plotly, Matplotlib
•	Git & GitHub
________________________________________
4. Setup Instructions
4.1 Clone the repository
git clone https://github.com/Bhargav054/ecom-analytics.git
cd ecom-analytics
4.2 Create & activate a virtual environment
python -m venv .venv
.venv\Scripts\activate
4.3 Install dependencies
pip install -r requirements.txt
________________________________________
5. MySQL Setup
5.1 Create database & user
Use MySQL Workbench or CLI:
CREATE DATABASE ecom_analytics;
CREATE USER 'datauser'@'localhost' IDENTIFIED BY 'Data@123';
GRANT ALL PRIVILEGES ON ecom_analytics.* TO 'datauser'@'localhost';
FLUSH PRIVILEGES;
5.2 Test connection
python scripts/test_mysql_conn.py
________________________________________
6. Load Dataset Into MySQL
Run the loader script:
python scripts/load_to_mysql.py
This automatically: - Reads dataset - Cleans missing/invalid values - Creates SQL table dynamically - Inserts all rows safely
________________________________________
7. Dataset Quality Check
To inspect missing values, duplicates, and anomalies:
python scripts/check_dataset_quality.py
________________________________________
8. Generate Mock Sales Data (Optional)
Useful for dashboards needing larger datasets:
python scripts/generate_mock_sales.py
________________________________________
9. Analyze Insights Using SQL Views
Run:
python scripts/analyze_views.py
This script retrieves insights such as: - Sales per country - Top revenue products - Monthly sales trends
________________________________________
10. Streamlit Dashboard
To launch:
streamlit run scripts/dashboard.py
Features: - Interactive revenue charts - Product & customer filters - Time‑based trend visualizations
________________________________________
11. Power BI Dashboard (Optional)
You can connect Power BI directly to MySQL using the MySQL connector. Dashboard includes: - Real‑time sales trends - Customer segmentation - Geo‑based revenue heatmaps - Profitability analysis
________________________________________
12. GitHub Version Control Workflow
Stage changes:
git add .
Commit changes:
git commit -m "Updated dashboard and README"
Push to GitHub:
git push
________________________________________
13. .gitignore Included
Project ignores: - .venv/ - __pycache__/ - .DS_Store - .ipynb_checkpoints - Secrets & temp files
________________________________________
14. License
This project is released under the MIT License.
________________________________________
15. Author
Bhargav
Data Analyst & Developer
GitHub: https://github.com/Bhargav054
________________________________________
16. Contribution Guidelines
Contributions are welcome!
Fork → Edit → Pull Request.
________________________________________
17. Future Enhancements
•	ML‑powered revenue forecasting
•	Customer segmentation using clustering
•	Automated ETL pipelines
•	Deployment on AWS / Azure
