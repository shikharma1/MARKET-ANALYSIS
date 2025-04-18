# 🛒 Market Basket Analysis & Customer Classification

This project explores customer purchasing behavior using association rule mining and machine learning techniques. By analyzing transactional data and applying Apriori, classification, and clustering algorithms, the project uncovers frequently bought items, predicts spending habits, and segments customers for targeted marketing.

---

## 📌 Problem Statement

Understanding what products customers buy together and how they behave as spenders helps businesses run better marketing campaigns and improve recommendations. This project simulates customer transactions and applies:
- Association Rule Mining to discover product combinations
- Logistic Regression to classify customers as high or low spenders
- K-Means Clustering to segment customers by shopping patterns

---

## 🧠 Algorithms Used

- **Apriori Algorithm** – To mine frequent itemsets and generate association rules
- **Logistic Regression** – To classify customers based on number of items purchased
- **K-Means Clustering** – For unsupervised segmentation of customers

---

## 📁 Dataset Details

- **File Name:** 10. Market Basket Analysis.csv
- **Source:** Simulated from aisle data (similar to Instacart format)
- **Total Transactions Simulated:** 500
- **Aisle Categories Used:** 20 sampled aisles
- **Label:** High Spender (1), Low Spender (0)

---

## 🛠 Technologies Used

- Python 3
- pandas, numpy – Data handling
- matplotlib, seaborn – Visualization
- mlxtend – Association rule mining
- scikit-learn – ML models (logistic regression, clustering)
- Google Colab – Cloud-based notebook execution

---

## 🔄 Methodology

1. **Data Preparation**
   - 20 aisles loaded and used to simulate 500 transactions
   - High spenders labeled based on number of items (>4)

2. **Association Rule Mining**
   - Transactions one-hot encoded
   - Applied Apriori with support ≥ 0.05
   - Generated rules with confidence ≥ 0.3

3. **Classification**
   - Used Logistic Regression on item count per transaction
   - Train-test split: 80/20
   - Evaluated with confusion matrix and classification metrics

4. **Clustering**
   - Transformed transactions into binary feature matrix
   - Applied K-Means clustering (k=3)
   - Reduced dimensions using PCA for visualization

---

## 📈 Output & Evaluation

### ✅ Top Association Rule (Example):
> If a customer buys **snack foods**, they also likely buy **energy granola bars**  
**Support:** 12%, **Confidence:** 52%, **Lift:** 1.43

---

### 📊 Confusion Matrix

|                | Predicted: Low | Predicted: High |
|----------------|----------------|-----------------|
| Actual: Low    | 45             | 3               |
| Actual: High   | 6              | 46              |

---

### 📋 Classification Report

| Metric     | Value |
|------------|-------|
| Accuracy   | 0.91  |
| Precision  | 0.88  |
| Recall     | 0.93  |

---

### 🎯 Clustering Output

- Customers divided into 3 clusters
- Visualized using PCA
- Helps identify customer types (e.g., health-conscious, snack-lovers, premium buyers)

---

## 🚀 How to Run

1. Open the notebook `market_basket_analysis.ipynb` in Google Colab
2. Upload the file `10. Market Basket Analysis.csv`
3. Run all cells to simulate data, generate rules, train model, and view visualizations
