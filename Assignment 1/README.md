# Airbnb Price Prediction: Bangkok & Singapore
## Data Analysis 3 - Assignment 1

### 📌 Project Overview
This project builds and evaluates machine learning models to predict Airbnb listing prices in **Bangkok, Thailand**. The goal is to develop a pricing model for a hypothetical Airbnb management company.

The project follows a rigorous workflow:
1.  **Data Cleaning & Feature Engineering**: Handling missing values, amenity extraction, and log-transformation of targets.
2.  **Model Building**: Training 5 models (OLS, LASSO, Ridge, Random Forest, GBM).
3.  **Performance Evaluation**: Comparing models using RMSE (Root Mean Squared Error) via 5-fold Cross-Validation.
4.  **External Validity Testing**:
    *   **Time Validity**: Testing the model on a later date in Bangkok (Q3).
    *   **Spatial Validity**: Testing the model on a different city, **Singapore** (Q3).

### 📂 Repository Structure
The repository is organized to ensure fully reproducible results:

```text
Data Analysis 3/
├── Assignment 1/
│   ├── code/                      # Code scripts for data processing and modeling
│   │   ├── src.ipynb
│   ├── data/
│   │   ├── raw/                   # Raw data files (compressed csv)
│   │   │   ├── listings_Bangkok_Q2.csv.gz
│   │   │   ├── listings_Bangkok_Q3.csv.gz
│   │   │   └── listings_Singapore_Q3.csv.gz
│   │   └── cleaned/               # Cleaned data files (post-processing)
│   ├── output/                    # Generated outputs
│   ├── README.md                  # This file
│   └── requirements.txt           # Python dependencies
```
### 📊 Data Source
Data is sourced from Inside Airbnb.
• Training Data: Bangkok (June 2025 / Q2)
• Time Validation: Bangkok (September 2025 / Q3)
• Spatial Validation: Singapore (September 2025 / Q3)
Note: Data files are stored in data/raw/ to ensure the code runs offline.
### 🚀 How to Run
1. Clone the repository:
2. Install dependencies: Ensure you have Python installed, then run:
3. Run the Notebook: Open src.ipynb in Jupyter Lab or VS Code and run all cells.
    ◦ The code uses relative paths, so no path configuration is needed.
### 🔑 Key Findings
• Best Model: Gradient Boosting Machine (GBM) outperformed OLS and Random Forest with the lowest RMSE (~0.19 log points).
• Feature Importance: accommodates (capacity) and room_type were the strongest predictors.
• External Validity:
    ◦ Time: The model performed excellently on future Bangkok data (RMSE stable).
    ◦ Space: The model failed to generalize to Singapore (RMSE ~1.50). Diagnostic plots reveal a systematic overestimation, suggesting structural differences in amenity valuation between the two markets.