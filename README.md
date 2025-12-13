# Amazon_music_clustering
🎵 Amazon Music Clustering (Unsupervised Learning)

📌 Project Overview

With millions of songs available on music streaming platforms like Amazon Music, manually categorizing tracks into genres or moods is impractical. This project applies unsupervised machine learning techniques to automatically group songs based on their audio characteristics.

Using clustering algorithms, songs with similar sound profiles are grouped together, enabling better playlist creation, music recommendation, and audio-based analysis — all without using any genre labels.


---

🎯 Problem Statement

Manual genre classification does not scale for large music catalogs. The objective of this project is to automatically cluster songs based on audio features such as energy, danceability, tempo, and acousticness, uncovering hidden patterns that reflect musical similarity.


---

🧠 Business Use Cases

🎶 Personalized Playlist Curation

Group similar-sounding songs to automatically generate playlists like Party, Chill, or Workout.

🔍 Improved Song Discovery

Recommend new tracks to users based on similarity to songs they already enjoy.

🎤 Artist & Market Analysis

Identify competitive tracks and analyze music trends based on audio characteristics.

📊 Market Segmentation

Understand listening behavior and optimize promotions or recommendations.


---

🛠️ Skills & Technologies Used

Python

Pandas & NumPy – Data handling

scikit-learn – Scaling, PCA, Clustering

Matplotlib & Seaborn – Visualization

Unsupervised Machine Learning

K-Means Clustering

PCA (Dimensionality Reduction)

Data Storytelling



---

📂 Dataset Description

File Name: single_genre_artists.csv

Audio Features Used:

danceability

energy

loudness

speechiness

acousticness

instrumentalness

liveness

valence

tempo

duration_ms


Ignored Columns:

Track names, artist names, IDs, genres, popularity, and dates were excluded from clustering to avoid bias.


---

🔄 Project Workflow (Step-by-Step)

1️⃣ Data Loading & Exploration

Loaded dataset using Pandas

Inspected shape, data types, and missing values

Verified all selected features were numeric


2️⃣ Feature Selection

Only audio features that describe rhythm, mood, and energy were selected:

danceability, energy, loudness, speechiness,
acousticness, instrumentalness, liveness,
valence, tempo, duration_ms

These features are sufficient to capture how a song sounds.


---

3️⃣ Data Normalization

Clustering is distance-based, so features were scaled using StandardScaler to ensure equal importance.


---

4️⃣ Clustering Technique (K-Means)

Why K-Means?

Simple and effective

Works well with scaled numeric data

Easy to interpret


Choosing the Best Number of Clusters

Elbow Method used to analyze inertia

Silhouette Score used to evaluate cluster quality


📌 Best k = 2 (Silhouette Score ≈ 0.70)


---

5️⃣ Cluster Evaluation

Metric	Result	Interpretation

Silhouette Score	~0.70	Excellent separation
Davies–Bouldin Index	~0.70	Good clustering quality
Inertia	Reported	Used in elbow method



---

6️⃣ Cluster Interpretation

Mean feature values were computed per cluster to understand musical characteristics.

🎉 Cluster 1 – Energetic / Dance Tracks

High energy

High danceability

Faster tempo

Higher valence (happy mood)


Use case: Party, workout, upbeat playlists

🌙 Cluster 0 – Calm / Acoustic / Speech-Oriented

High acousticness

Higher speechiness

Lower energy

Slower tempo


Use case: Chill, podcast-like, relaxing playlists


---

7️⃣ Visualization

The following visualizations were created:

PCA Scatter Plot – 2D visualization of clusters

Bar Charts – Average feature values per cluster

Heatmap – Feature dominance across clusters

Distribution Plots – Feature spread within clusters


These plots clearly show separation and cluster characteristics.


---

8️⃣ Final Output & Export

Cluster labels added to original dataset

Songs grouped by cluster for analysis

Final dataset exported as:


amazon_music_clustered_songs.csv


---

✅ Project Results

By the end of this project, we successfully:

✔ Generated distinct clusters of songs based on audio similarity
✔ Visualized and interpreted musical characteristics of each cluster
✔ Demonstrated how clustering can support recommendation systems and playlist generation


---

📦 Project Deliverables

Jupyter Notebook (.ipynb) with:

Preprocessing

Clustering

Evaluation

Visualization


Final clustered CSV file

This detailed README documentation



---

🚀 Future Improvements

Add Streamlit app for interactive exploration

Try DBSCAN / Hierarchical clustering for comparison

Integrate user listening history

Deploy as a recommendation microservice



---

👤 Author

Mohammed Ansari
Aspiring Data Scientist | Machine Learning Enthusiast
