# 🍫 ChocoCrunch Analytics

Data-Driven Insights on the Global Chocolate Industry

# 🧭 Abstract

This project aims to analyze and visualize comprehensive data from the global chocolate market using data science methodologies. The study focuses on understanding nutritional characteristics, brand performance, and ingredient composition patterns.
Data was collected from the OpenFoodFacts API, processed with Python, structured in a MySQL database, and visualized using Streamlit. The project demonstrates an end-to-end data pipeline encompassing data extraction, transformation, storage, analysis, and dashboard deployment.

# 🎯 Project Goals

- To collect authentic, large-scale chocolate product data using an open-source API.
- To clean, organize, and normalize the dataset for analytical use.
- To perform feature engineering and derive health-based insights.
- To store structured data in a relational MySQL database for efficient querying.
- To visualize findings interactively through a Streamlit application.

# ⚙️ Tools and Technologies

| Component                  | Technology                         |
| -------------------------- | ---------------------------------- |
| **Programming Language**   | Python                             |
| **Libraries Used**         | Pandas, NumPy, Matplotlib, Seaborn |
| **Database Management**    | MySQL (via SQLAlchemy)             |
| **Visualization Platform** | Streamlit                          |
| **Data Source**            | OpenFoodFacts API                  |

# 📊 Workflow Overview

1. Data Acquisition
- Retrieved chocolate-related entries using OpenFoodFacts API.
- Extracted details: product name, brand, ingredients, nutritional values, additives, allergens, and country of origin.
- Collected ~14,000+ records globally.

2. Data Preprocessing
- Removed incomplete and duplicate entries.
- Standardized measurement units and formatted numerical attributes.
- Handled null and inconsistent values to ensure analytical consistency.

3. Feature Engineering
Derived analytical variables include:
- Sugar-to-Carbohydrate Ratio
- Calorie Category (Low / Medium / High)
- Sugar Category
- Ultra-Processed Classification (NOVA-based)

4. Database Integration
Created MySQL relational schema with three key tables:
- product_info
- nutrient_info
- derived_metrics
Data insertion performed using Python–SQLAlchemy integration.

5. Exploratory Data Analysis (EDA)
- Conducted statistical summaries and univariate analysis.
- Generated nutrient distributions, category comparisons, and brand-level summaries.
- Visualized patterns using Matplotlib and Seaborn.

6. Dashboard Visualization (Streamlit)
- Designed an interactive interface for exploring key insights.
- Implemented filters, brand comparisons, and categorical distributions.
- Integrated query-based visual outputs directly from MySQL tables.

💡 Key Insights

- Most commercial chocolates fall under high-calorie and ultra-processed categories.
- Distinct variation found between sugar-to-carb ratios across brands.
- Only a small fraction of products align with low-sugar nutritional profiles.

# 🧱 Project Architecture

ChocoCrunch-Analytics/
│
├── data/
│   ├── raw_data.csv
│   ├── cleaned_data.csv
│   └── engineered_data.csv
│
├── src/
│   ├── extract_data.py
│   ├── clean_data.py
│   ├── feature_engineering.py
│   ├── load_to_sql.py
│   └── streamlit_app.py
│
├── notebooks/
│   └── exploratory_analysis.ipynb
│
├── app.py
├── schema.sql
├── requirements.txt
└── README.md

## 🚀 Getting Started

#### Prerequisites
- Python 3.10+
- MySQL Database (running locally or on a server)
- Git

#### Clone Repository
```
https://github.com/Maryam-Feroz/-ChocoCrunch-Analytics.git
cd ChocoCrunch-Analytics
```

#### Install Dependencies
```
pip install -r requirements.txt
```
#### Configure Secrets
Create .streamlit/secrets.toml with your MySQL credentials:
```
[database]
db_host="127.0.0.1"
db_user="root"
db_password="your_password"
db_name="choco_crunch"
```
#### Run the Streamlit App
```
streamlit run app.py
```
The app will open in your default browser at ```http://localhost:8501```.

# 🚀 Future Scope
- Incorporate predictive modeling for nutrient-based classification.
- Add country-wise analytics to compare nutritional trends geographically.
- Integrate real-time API updates for dynamic dashboards.
- Enhance visualization with additional libraries (Plotly, Altair).

# 📚 References

- OpenFoodFacts API Documentation
- NOVA Food Classification System
- Streamlit Official Docs
- MySQL and SQLAlchemy Documentation
