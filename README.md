# Mall Customer Segmentation using K-Means

This project performs customer segmentation using the K-Means clustering algorithm on a mall dataset. The segmentation is based on **Annual Income** and **Spending Score**, helping identify different types of customers for targeted marketing.

---

## 📊 Dataset

- **Source:** Mall Customer Dataset (Mall_Customers.csv)
- **Features used:**
  - `Annual Income (k$)`
  - `Spending Score (1–100)`

---

## ⚙️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Pickle

---

## 🚀 Project Workflow

1. **Load and explore the dataset**
2. **Select relevant features**
3. **Use the Elbow Method** to determine the optimal number of clusters
4. **Train KMeans model**
5. **Visualize the clusters**
6. **Save the trained model using Pickle**

---

## 🧪 Sample Output

![Customer Segments](https://i.ibb.co/Wp49Vp7X/image.png)


Each color represents a unique cluster of customers:

- **Red:** High income, high spending  - Premium customers likely to respond well to exclusive offers.  
- **Yellow:** Low income, high spending  - Brand-loyal or impulsive buyers despite low income.  
- **Blue:** High income, low spending  - Conservative spenders or need targeted marketing.  
- **Green:** Average income and spending  - Balanced income and spending customers.  
- **Brown:** Low income, low spending  - Balanced income and spending customers.  
- **Cyan points:** Centroids of the clusters  

---

## 🧠 KMeans Training & Saving

```python
from sklearn.cluster import KMeans
import pickle

# Train model
kmeans = KMeans(n_clusters=5, random_state=42)
kmeans.fit(X)

# Save model
with open("kmeans_model.pkl", "wb") as f:
    pickle.dump(kmeans, f)

# Load model
with open("kmeans_model.pkl", "rb") as f:
    loaded_model = pickle.load(f)
```

## 📦 Requirements

You can install all required libraries using:

```bash
pip install -r requirements.txt
```
