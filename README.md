# Customer Segmentation — Mall Customers

## Overview
This project performs **customer segmentation** using the Mall Customer dataset from Kaggle.  
The goal is to **group customers** based on their **annual income** and **spending score** to understand customer behavior patterns.  
We use **unsupervised learning** techniques (K-Means and DBSCAN) and visualize the clusters for analysis.

---

## Dataset
- **Source:** [Mall Customers Dataset on Kaggle](https://www.kaggle.com/datasets/shwetabh123/mall-customers)  
- **Description:** The dataset contains 200 records of mall customers with the following columns:
  - `CustomerID`: Unique identifier for each customer
  - `Genre`: Gender of the customer
  - `Age`: Age of the customer
  - `Annual Income (k$)`: Customer annual income in thousand dollars
  - `Spending Score (1-100)`: Score assigned by the mall based on customer behavior

> **Note:** The dataset is **not included** in this repo. Place the CSV file in the `data/` folder.

---

## Project Structure
customer-segmentation-mall/
│
├── data/ ← Place Mall Customers CSV dataset here
├── notebooks/ ← Jupyter notebooks
│ └── customer_segmentation.ipynb
├── outputs/ ← Plots, models, or generated files
├── src/ ← Optional Python scripts
├── README.md ← Project description and instructions
├── requirements.txt ← Python dependencies for pip
├── environment.yml ← Conda environment file
└── .gitignore ← Files/folders to ignore in Git

---

## Tools & Libraries
- **Python 3**
- **Pandas** — data manipulation
- **NumPy** — numerical operations
- **Matplotlib & Seaborn** — data visualization
- **Scikit-learn** — clustering algorithms
- **Joblib** — save/load models
- **JupyterLab / Jupyter Notebook** — interactive coding

---

## Features / Steps Implemented
1. **Data Loading and Cleaning**  
   - Load CSV into a pandas DataFrame
   - Check for missing values and data types

2. **Exploratory Data Analysis (EDA)**  
   - Visualize distribution of Age, Annual Income, and Spending Score
   - Scatter plots to explore relationships between income and spending

3. **Preprocessing & Scaling**  
   - Selected features: `annual_income_(k$)` and `spending_score_(1-100)`
   - Scaled features using `StandardScaler` for clustering

4. **K-Means Clustering**  
   - Determined optimal number of clusters using **Elbow Method** and **Silhouette Score**
   - Applied K-Means clustering
   - Visualized clusters in 2D plots
   - Analyzed cluster characteristics (mean income, spending score, age)

5. **DBSCAN Clustering (Bonus)**  
   - Applied DBSCAN to explore density-based clustering
   - Compared results with K-Means

6. **Model Saving**  
   - Saved K-Means model and scaler using Joblib
   - Outputs saved in the `outputs/` folder

---

## How to Run ### 1. Clone the repository
bash
git clone https://github.com/areeba_munir/customer-segmentation-mall.git
cd customer-segmentation-mall
2. Install dependencies
pip install -r requirements.txt
3. Using conda
conda env create -f environment.yml
conda activate custseg
3. Launch Jupyter Notebook
jupyter notebook
4. Run the notebook

Follow the step-by-step cells to:

Explore data

Scale features

Apply clustering

Visualize and analyze clusters
5. Run the notebook

Follow the step-by-step cells to:

Explore data

Scale features

Apply clustering

Visualize and analyze clusters

