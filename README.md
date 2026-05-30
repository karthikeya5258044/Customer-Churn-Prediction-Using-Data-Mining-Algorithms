
🔄 Customer Churn Prediction Using Data Mining Algorithms
A machine learning system to predict customer churn for a telecom provider using Data Mining techniques including Apriori association rule mining, Decision Tree classification, and advanced feature engineering — achieving ~80% prediction accuracy on a real-world dataset of 7,043 records.

🚀 Project Overview
Customer churn — when subscribers cancel their service — is one of the most costly problems in the telecom industry. This project builds a complete churn prediction pipeline on the Telco Customer Churn dataset, using Data Mining and ML techniques to identify at-risk customers and enable proactive retention strategies.

🧰 Tech Stack
CategoryToolsLanguagePython 3.xData ManipulationPandas, NumPyVisualizationMatplotlib, SeabornMachine LearningScikit-learn (Decision Tree, Random Forest)Data MiningApriori (mlxtend), Association Rule MiningFeature EngineeringLabel Encoding, Feature Importance (C4.5 entropy)EnvironmentJupyter Notebook

📂 Project Structure
Customer-Churn-Prediction-Using-Data-Mining-Algorithms/
│
├── churn_prediction.ipynb    # Main notebook — EDA, modelling, evaluation
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation

📊 Dataset

Source: Telco Customer Churn Dataset (publicly available on Kaggle)
Size: 7,043 customer records
Target Variable: Churn (Yes / No)
Key Features: Tenure, contract type, monthly charges, fiber optic usage, payment method, tech support, and more


🔬 Methodology
1. Data Preprocessing

Handled missing values and converted TotalCharges to numeric
Encoded categorical variables (Label Encoding and One-Hot Encoding)
Balanced class distribution to address churn/non-churn imbalance

2. Exploratory Data Analysis (EDA)

Analyzed churn rate across contract types, tenure segments, and monthly charges
Key finding: month-to-month contracts with fiber optic plans showed the highest churn rate (~85%)
Visualized feature correlations and churn distribution using heatmaps and bar charts

3. Association Rule Mining (Apriori)

Applied Apriori algorithm to discover behavioral patterns among churning customers
Mined association rules linking contract type, monthly charges, and fiber optic usage to churn
Identified: customers on month-to-month contracts + fiber optic plan are the highest-risk segment

4. Classification — Decision Tree (C4.5 / Entropy)

Trained a Decision Tree classifier using entropy-based splitting (C4.5 approach)
Applied pruning to prevent overfitting
Evaluated using accuracy, precision, recall, F1-score, and confusion matrix

5. Feature Importance Analysis

Top churn drivers identified: tenure, contract type, and monthly charges
Used feature importance scores to reduce noise and improve model performance


📈 Results
MetricScoreModel Accuracy~80%Key Churn SegmentMonth-to-month + Fiber OpticTop Predictive FeaturesTenure, Contract Type, Monthly ChargesBusiness OutputHigh / Medium / Low risk customer segments

🗂️ Business Insights

High-Risk Segment: Month-to-month contract + fiber optic + monthly charges > ₹65 → churn rate ~85%
Retention Strategy: Target high-risk customers with contract upgrade offers and loyalty discounts
Low-Risk Segment: 2-year contract customers with < 12 months tenure rarely churn
Results exported to CSV to enable CRM-based retention campaigns


⚙️ Setup & Installation
1. Clone the repository
bashgit clone https://github.com/karthikeya5258044/Customer-Churn-Prediction-Using-Data-Mining-Algorithms.git
cd Customer-Churn-Prediction-Using-Data-Mining-Algorithms
2. Install dependencies
bashpip install -r requirements.txt
3. Run the notebook
bashjupyter notebook churn_prediction.ipynb

📦 Requirements
pandas
numpy
matplotlib
seaborn
scikit-learn
mlxtend
jupyter

🛠️ Future Improvements

 Experiment with XGBoost and LightGBM for improved accuracy
 Add SMOTE oversampling to better handle class imbalance
 Deploy as a REST API using Flask/FastAPI for real-time scoring
 Build an interactive churn risk dashboard with Streamlit


👤 Author
Kompella Kartikeya
B.Tech CSE – Data Analytics | VIT-AP University
