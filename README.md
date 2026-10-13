# 🎵 Spotify Popularity: Neural Engineering & Business Intelligence

[![Tech: NumPy-Scratch](https://img.shields.io/badge/Tech-NumPy--Scratch-blue.svg)]()
[![BI: Power-BI](https://img.shields.io/badge/BI-Power--BI-yellow.svg)]()
[![Academic: Ms. Data Science](https://img.shields.io/badge/Academic-Ms.--Data--Science-red.svg)]()

**Spotify Popularity Analytics** is a dual-phase project that bridges the gap between low-level algorithm engineering and high-level executive storytelling. Developed as part of the **MSc Data Science** program at the **University of Europe for Applied Sciences**, this repository features a binary classification system built from scratch and an interactive Power BI dashboard for strategic trend analysis.

## 🧠 Phase 1: Machine Learning from Scratch
To demonstrate a deep understanding of mathematical optimization, three core models were implemented using **pure NumPy**, avoiding high-level libraries like scikit-learn for the model logic.

*   **Custom Perceptron:** Implemented with a binary threshold activation and a manual learning rule to establish a baseline.
*   **Logistic Regression:** Built using Sigmoid activation and Binary Cross-Entropy loss, optimized via Gradient Descent.
*   **Neural Network:** Input → 8-unit hidden layer (**ReLU**) → **Sigmoid** output, trained with manual **Backpropagation** (3 layers counting the input).

### Performance Summary
The goal was to predict if a song's popularity score is $\ge 50$ based on audio features.

| Algorithm | Accuracy | RMSE | Training setup | Technical Logic |
| :--- | :--- | :--- | :--- | :--- |
| **Perceptron** | 73.8% | 0.512 | 10 epochs, lr 0.01 | Linear Threshold |
| **Logistic Regression** | 74.6% | 0.475 | 1,000 iterations, lr 0.001 | Probabilistic Gradient Descent |
| **Neural Network** | 74.6% | 0.435 | 2,000 iterations, lr 0.01, 8 hidden units | Non-Linear Backpropagation |

*Results reproduced by running `predicting_song_popularity.py` on `Spotify_dataset.csv` (80/20 split, `random_state=42`; the neural network's small random initialisation can shift its numbers slightly between runs).*

> **Honest note:** only ~25.8% of the 114,000 tracks have popularity ≥ 50, so always predicting "not popular" already scores ~74.2%. These audio features carry limited signal for popularity, and all three models land just above that baseline. RMSE (on predicted probabilities) is the more informative comparison here.

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
1.  **Data Preparation**: Sourced from Kaggle; tracks were labeled as "popular" (1) or "not popular" (0) based on a threshold of 50.
2.  **Feature Engineering**: Standardized 7 key audio dimensions (Danceability, Energy, Valence, Tempo, Loudness, Acousticness, and Instrumentalness) using Z-score normalization.
3.  **Algorithmic Training**: Trained with 10 (perceptron), 1,000 (logistic regression) and 2,000 (neural network) iterations, with an 80/20 train/test split.
4.  **Tools Used**: Python (NumPy for the models; pandas and scikit-learn only for loading, scaling, splitting and the RMSE metric) and Power BI (DAX) for visual analytics.

## 📂 Project Files
*   `predicting_song_popularity.py`: Full Python source code for the NumPy-based models. Exported from Colab: change the dataset path in `pd.read_csv(...)` to `Spotify_dataset.csv` and remove the `google.colab` import to run it locally.
*   `Machine_Learning_Assignment1.pdf`: Detailed technical report on formulations, methodology, and results.
*   `Spotify_Insights_Dashboard.pbix`: Interactive Power BI dashboard.
*   `Spotify_dataset.csv`: Raw data containing 114k+ Spotify records.

---
*Developed by Khaled Walid under the guidance of Professor Nor Azizah Hitam.*
