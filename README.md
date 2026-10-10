# Facebook-K-Means_Clustering
# 📊 Facebook Live Posts – K-Means Clustering

## 📌 Project Overview

This project uses **Machine Learning (K-Means Clustering)** to group Facebook Live posts based on their engagement characteristics, such as reactions, comments, shares, likes, loves, and other user reactions.

The project includes data preprocessing, feature transformation, standardization, optimal cluster selection, cluster analysis, and interactive visualization using a **Streamlit web application**.

## 🎯 Objectives

- Analyze Facebook Live post engagement data.
- Identify groups of posts with similar engagement patterns.
- Apply K-Means clustering to discover patterns in the dataset.
- Determine the optimal number of clusters using the Elbow Method and Silhouette Score.
- Visualize clusters using Principal Component Analysis (PCA).
- Provide an interactive dashboard to explore results.

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Scikit-learn** – Machine learning and clustering
- **Streamlit** – Interactive web application
- **Jupyter Notebook** – Model experimentation and analysis

## 📂 Project Structure

```text
Facebook-Live-KMeans-Clustering/
│
├── app.py
├── Live.csv
├── facebook_live_project.ipynb
├── requirements.txt
└── README.md
```

## 📊 Dataset Description

The project uses `Live.csv`, which contains Facebook Live post information and engagement metrics.

Important features include:

- `num_reactions`
- `num_comments`
- `num_shares`
- `num_likes`
- `num_loves`
- `num_wows`
- `num_hahas`
- `num_sads`
- `num_angrys`
- `status_type`

The engagement features are used for clustering, while `status_type` helps analyze the composition of different clusters.

## ⚙️ Methodology

### 1. Data Loading
Load the dataset using Pandas and inspect its rows, columns, and post types.

### 2. Data Preprocessing
- Remove unnecessary columns when present.
- Check missing values.
- Replace missing feature values with their median.

### 3. Feature Transformation
Apply the `log1p()` transformation to reduce the effect of highly skewed engagement values.

### 4. Feature Scaling
Use `StandardScaler` to standardize the transformed features.

### 5. Optimal Cluster Selection
- **Elbow Method:** Analyze inertia for different values of K.
- **Silhouette Score:** Compare clustering quality for different values of K.

The application selects the K value with the highest calculated silhouette score.

### 6. K-Means Clustering
Train the final K-Means model and assign a cluster label to each post.

### 7. Cluster Analysis
Examine cluster counts and mean and median engagement profiles.

### 8. PCA Visualization
Use Principal Component Analysis to reduce the scaled features to two dimensions for visualizing clusters.

### 9. Result Export
Download the final clustered dataset as a CSV file.

## ✨ Features

- Interactive Streamlit dashboard
- Dataset preview and missing-value analysis
- Facebook post-type distribution chart
- Automated selection of the number of clusters
- Elbow Method visualization
- Silhouette Score comparison
- K-Means cluster distribution
- Mean and median cluster profiles
- PCA-based cluster visualization
- Post-type composition analysis
- Downloadable clustered dataset

## 🚀 Installation and Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Facebook-Live-KMeans-Clustering.git
```

### Step 2: Open the Project Folder

```bash
cd Facebook-Live-KMeans-Clustering
```

### Step 3: Install Dependencies

```bash
pip install streamlit pandas numpy matplotlib scikit-learn jupyter
```

### Step 4: Run the Streamlit Application

Make sure `app.py` and `Live.csv` are in the same folder.

```bash
streamlit run app.py
```

The application will open in your browser. If it does not open automatically, visit:

`http://localhost:8501`

### Step 5: Run the Jupyter Notebook (Optional)

```bash
jupyter notebook
```

Open `facebook_live_project.ipynb` to explore the notebook-based analysis.

## 📈 Expected Results

The application provides:

- An overview of the Facebook Live dataset.
- Visualizations of post-type distribution.
- Elbow and silhouette plots for cluster selection.
- Cluster labels for individual posts.
- Engagement summaries for each cluster.
- A two-dimensional PCA visualization.
- A downloadable CSV file containing cluster assignments.

Actual cluster counts and evaluation scores depend on the dataset and preprocessing.

## 💡 Applications

- Understanding social media engagement patterns.
- Grouping posts with similar audience interactions.
- Comparing engagement characteristics across post types.
- Supporting social media content analysis.
- Helping content creators explore audience engagement trends.

## ⚠️ Limitations

- K-Means clustering is an unsupervised learning method and does not predict engagement directly.
- Cluster labels do not have predefined meanings.
- Results depend on feature selection, preprocessing, and the chosen clustering method.
- Clustering results alone cannot establish why a post received a particular level of engagement.

## 🔮 Future Enhancements

- Add interactive filters for post types and engagement metrics.
- Compare K-Means with DBSCAN and hierarchical clustering.
- Add downloadable cluster visualizations and reports.
- Deploy the application online.
- Develop a dashboard for comparing engagement patterns over time.

⭐ If you find this project useful, consider giving the repository a star!
