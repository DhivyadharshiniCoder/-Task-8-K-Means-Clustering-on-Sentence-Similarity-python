# 📘 Task 8 – K-Means Clustering on Plagiarism Detection Data

In this task, we applied **K-Means Clustering** on the sentence similarity scores generated from our plagiarism detection model to explore whether sentence pairs could be grouped into meaningful clusters without supervision.

---

## 📂 Dataset Used
- File: `similarity_output_task3.csv`
- Columns:
  - `Similarity_Score`: Cosine similarity between sentence pairs
  - `Plagiarised`: 1 (Yes) or 0 (No) — used only for evaluating clustering accuracy

---

## 🛠️ Task Objective
To group sentence pairs into clusters (likely plagiarised vs. not) using unsupervised learning.

---

## ✅ Steps Performed

1. Imported `Similarity_Score` feature from the dataset.
2. Scaled the data using `StandardScaler` for better clustering performance.
3. Applied `KMeans` with 2 clusters.
4. Visualized the clusters using a scatter plot.
5. Evaluated the clustering using:
   - **Silhouette Score**
   - **Confusion Matrix** (compared against `Plagiarised` column for reference)

---

## 📈 Visualization

A scatter plot was generated to show the two clusters. Since it's 1D data, the y-axis was fixed to 0, and clustering was done along the similarity scores.

---

## 🧠 Insights

- The KMeans model was able to separate high-similarity and low-similarity sentence pairs effectively.
- The Silhouette Score provided a measure of how well-defined the clusters were.
- Comparing the predicted clusters with actual `Plagiarised` labels gave us insight into how useful unsupervised methods can be in detecting plagiarism.

---

## 📌 Libraries Used

- `pandas`
- `matplotlib`
- `seaborn`
- `sklearn.cluster.KMeans`
- `sklearn.preprocessing.StandardScaler`
- `sklearn.metrics.silhouette_score`, `confusion_matrix`

---

## 🧾 Output Example

```bash
🧠 Silhouette Score: 0.697

✅ Confusion Matrix (Cluster vs. Actual Label):
[[20  5]
 [ 0 25]]

