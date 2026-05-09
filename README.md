# 🎵 Spotify Popularity: Neural Engineering & Business Intelligence

[![Tech: NumPy-Scratch](https://img.shields.io/badge/Tech-NumPy--Scratch-blue.svg)]()
[![BI: Power-BI](https://img.shields.io/badge/BI-Power--BI-yellow.svg)]()
[![Academic: Ms. Data Science](https://img.shields.io/badge/Academic-Ms.--Data--Science-red.svg)]()

**Spotify Popularity Analytics** is a dual-phase project that bridges the gap between low-level algorithm engineering and high-level executive storytelling. Developed as part of the **MSc Data Science** program at the **University of Europe for Applied Sciences**, this repository features a binary classification system built from scratch and an interactive Power BI dashboard for strategic trend analysis[cite: 1].

## 🧠 Phase 1: Machine Learning from Scratch
To demonstrate a deep understanding of mathematical optimization, three core models were implemented using **pure NumPy**, avoiding high-level libraries like scikit-learn for the model logic[cite: 1].

*   **Custom Perceptron:** Implemented with a binary threshold activation and a manual learning rule to establish a baseline[cite: 1].
*   **Logistic Regression:** Built using Sigmoid activation and Binary Cross-Entropy loss, optimized via Gradient Descent[cite: 1].
*   **Neural Network:** A 3-layer architecture featuring **ReLU** in the hidden layer and **Sigmoid** for the output, trained through manual **Backpropagation**[cite: 1].

### Performance Summary
The goal was to predict if a song's popularity score is $\ge 50$ based on audio features[cite: 1].

| Algorithm | Accuracy (~1k iter) | RMSE | Technical Logic |
| :--- | :--- | :--- | :--- |
| **Perceptron** | 73.8% | Higher | Linear Threshold[cite: 1] |
| **Logistic Regression** | 74.6% | Lower | Probabilistic Gradient Descent[cite: 1] |
| **Neural Network** | 74.6% | Lower | Non-Linear Backpropagation[cite: 1] |

---

## 📊 Phase 2: Power BI Executive Dashboard
To translate these findings for a non-technical audience, I developed an interactive dashboard focusing on clarity, visual hierarchy, and actionable insights.

### 📌 Interactive Components
*   **Danceability vs. Popularity:** Scatter plots identifying the "rhythm-to-success" relationship.
*   **Genre Benchmarking:** Comparison of average popularity across the top 10 genres.
*   **Explicit Content Distribution:** Analysis of how explicit vs. non-explicit tracks impact listener engagement.
*   **KPI Tracking:** Real-time visibility into Total Tracks (114,000+), Average Popularity, and Danceability.

---

## 🛠️ Technical Methodology
1.  **Data Preparation**: Sourced from Kaggle; tracks were labeled as "popular" (1) or "not popular" (0) based on a threshold of 50[cite: 1].
2.  **Feature Engineering**: Standardized 7 key audio dimensions (Danceability, Energy, Valence, Tempo, Loudness, Acousticness, and Instrumentalness) using Z-score normalization[cite: 1].
3.  **Algorithmic Training**: Validated convergence behavior by varying training iterations ($n\_iter$) up to 1000[cite: 1].
4.  **Tools Used**: Python (NumPy, pandas) for core logic[cite: 1] and Power BI (DAX) for visual analytics.

## 📂 Project Files
*   `predicting_song_popularity.py`: Full Python source code for the NumPy-based models.
*   `Machine_Learning_Assignment1.pdf`: Detailed technical report on formulations, methodology, and results[cite: 1].
*   `Spotify_Insights_Dashboard.pbix`: Interactive Power BI dashboard.
*   `Spotify_dataset.csv`: Raw data containing 114k+ Spotify records[cite: 1].

---
*Developed by Khaled Walid under the guidance of Professor Nor Azizah Hitam.*
