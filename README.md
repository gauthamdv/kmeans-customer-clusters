# K-Means Customer Clusters 🛍️

A complete customer segmentation project using **K-Means Clustering** in Python. This project helps malls and retail businesses identify distinct customer groups and target high-value customers for marketing campaigns.

---

## 📖 Introduction

Customer segmentation is essential to understand customer behavior and plan effective marketing strategies. Using membership data from a mall (age, gender, annual income, and spending score), we perform unsupervised learning to group customers into meaningful clusters.

---

## 🎯 Objectives

1. Perform **customer segmentation** using K-Means Clustering.
2. Visualize clusters and analyze their characteristics.
3. Identify **target customers** for focused marketing strategies.
4. Save clustered datasets and trained models for future use.

---

## 🛠️ Tools & Libraries

* **Python**
* **Pandas** – Data manipulation
* **NumPy** – Numerical computations
* **Scikit-learn** – Machine learning algorithms
* **Matplotlib & Seaborn** – Visualization
* **Joblib** – Save and load models

---

## 📂 Repository Structure

```
kmeans-customer-clusters/
│
├── datasets/                 # Raw and preprocessed datasets
├── models/                   # Trained K-Means model
├── plots/                    # Visualizations
├── kmn-clustering.ipynb      # Jupyter notebook for analysis
├── data-preprocessing.py     # Data preprocessing script
├── requirements.txt          # Required Python packages
└── README.md                 # Project documentation
```

---

## 📈 Methodology

1. **Data Preprocessing**

   * Remove `CustomerID` for modeling purposes
   * Convert `Gender` to numeric labels (0=Male, 1=Female)
   * Standardize `Age` and `Annual Income`
   * Normalize `Spending Score`
     *(Use `data-preprocessing.py` to process and clean the data)*

2. **Determine Optimal Number of Clusters**

   * **Elbow Method** to analyze inertia
   * **Silhouette Score** to select best K

3. **K-Means Clustering**

   * Fit K-Means model
   * Assign cluster labels to customers
   * Visualize clusters (scatter plots, PCA 2D, 3D plots)

4. **Cluster Analysis**

   * Compute mean, min, max of features per cluster
   * Analyze gender ratio, age, income, and spending behavior

5. **Identify Target Customers**

   * High-value customers based on **Spending Score** and **Annual Income**
   * Export target customers for marketing purposes

6. **Save Outputs**

   * Clustered dataset (`Mall_Customers_with_Clusters.csv`)
   * Target customers (`Target_Customers.csv`)
   * Trained K-Means model (`kmeans_customer_model.pkl`)

---

## 📊 Visualizations

* Customer distribution across clusters
* Pairplots of features by cluster
* Boxplots per cluster (by gender)
* Heatmap of cluster centers
* 3D scatter plot of customer clusters

These plots help in understanding differences between customer segments.

---

## 💾 Installation & Requirements

Install dependencies using the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

1. Open `kmn-clustering.ipynb` to explore the full analysis.
2. Use the preprocessed dataset in `datasets/data-clean.csv` for running the notebook.
3. Generate cluster visualizations and target customer list.
4. Load the saved model with Joblib for predictions on new data:

```python
import joblib

kmeans_model = joblib.load("models/kmeans_customer_model.pkl")
```

---

## 📚 Dataset

* **Source**: Udemy's *[Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)* 
* **Features**:

  * `CustomerID`
  * `Gender`
  * `Age`
  * `Annual Income (k$)`
  * `Spending Score (1-100)`

The dataset is provided in `datasets/` folder for learning purposes only.

---

## 🔖 License

This repository is for **educational purposes** and is freely available for learning and sharing.
