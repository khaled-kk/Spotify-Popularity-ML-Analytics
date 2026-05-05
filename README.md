# 🎵 Spotify Popularity: Machine Learning from Scratch

[![Tech: Python/NumPy](https://img.shields.io/badge/Tech-NumPy--Only-blue.svg)]()
[![Field: Data Science](https://img.shields.io/badge/Academic-Ms.--Data--Science-red.svg)]()
[![Status: Research-Complete](https://img.shields.io/badge/Status-Complete-success.svg)]()

**Spotify Popularity ML** is an in-depth exploration of binary classification algorithms implemented entirely from scratch using Python and NumPy. This project bypasses high-level ML libraries to demonstrate the mathematical mechanics behind how models learn, optimize, and generalize.

## 📊 Project Objective
The goal is to predict song popularity (defined as a score $\ge 50$) based on acoustic features. By manually coding the backpropagation and gradient descent logic, this project serves as a technical benchmark for foundational ML principles.

## 🛠️ Implemented Models
Unlike standard projects, these models were built using pure matrix mathematics:
*   **Perceptron:** A classic linear binary classifier using the perceptron learning rule.
*   **Logistic Regression:** Optimized via Gradient Descent using Sigmoid activation and Binary Cross-Entropy loss[cite: 1].
*   **Neural Network:** A multi-layer architecture featuring **ReLU** activation in the hidden layer and **Backpropagation** for weight updates[cite: 1].

## 🧪 Methodology & Preprocessing
*   **Feature Engineering:** Focused on 7 key audio dimensions: Danceability, Energy, Valence, Tempo, Loudness, Acousticness, and Instrumentalness[cite: 1].
*   **Normalization:** Applied Z-score standardization to ensure numerical stability and consistent feature scaling[cite: 1].
*   **Training Strategy:** Implemented an 80/20 train-test split with iterative convergence monitoring ($n\_iter$ up to 1000)[cite: 1].
  
## 📊 Business Intelligence Dashboard (Power BI)
To complement the machine learning models, I developed an interactive Power BI dashboard to explore the underlying trends of the Spotify dataset.

*   **Feature Correlation:** Heatmaps showing the relationship between "Energy" and "Loudness."
*   **Popularity Distribution:** Analysis of the $P \ge 50$ threshold across different genres and tempos.
*   **Acoustic Profiles:** Visualizing the "sweet spot" of danceability and valence for hit records.
*   **Model Performance:** A visual comparison of Accuracy and RMSE across the Perceptron, Logistic Regression, and Neural Network models.
  
## 📈 Results & Benchmarks
The performance was evaluated using Accuracy and **RMSE** to assess probability calibration[cite: 1].

| Model | Accuracy (~1k iter) | RMSE |
| :--- | :--- | :--- |
| **Perceptron** | 73.8% | Higher |
| **Logistic Regression** | 74.6% | Lower |
| **Neural Network** | 74.6% | Lower |

> **Key Insight:** While the Neural Network and Logistic Regression plateaued at similar accuracy, the lower RMSE in these models indicates superior confidence and probability calibration compared to the basic Perceptron[cite: 1].

## 🚀 Getting Started
1. **Clone the repo:**
   ```bash
   git clone [https://github.com/khaled-kk/Spotify-Popularity-ML-Scratch.git](https://github.com/khaled-kk/Spotify-Popularity-ML-Scratch.git)

2. **Review the Report:** See Assignment_Report.pdf for the full mathematical breakdown and professor guidance[cite: 1].

3. **Run the Code:** Open the Jupyter notebook to see the NumPy-based implementations.

---
*Developed by Khaled Walid under the guidance of Professor Nor Azizah Hitam.*
