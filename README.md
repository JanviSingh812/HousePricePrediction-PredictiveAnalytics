# House Price Prediction

## 📌 Project Overview
This repository contains a data-driven regression pipeline engineered to eliminate pricing guesswork in real estate transactions. Using a real-world housing dataset comprising structural, amenity-based, and geographical variables, we benchmarked predictive models to project property valuations and isolate key market drivers.

---

## 📁 Repository Structure
* **`analysis.ipynb`** — The complete, documented Jupyter Notebook covering data loading, cleaning, preprocessing, model training, and data visualization.
* **`Housing.csv`** — The underlying raw housing dataset used for training and validation.
* **`summary.pdf`** — An executive-ready 1-page written evaluation report detailing strategic business insights.
* **`charts/`** — High-resolution production plots exported during model analysis:
  * `chart1_price_distribution.png` (Market Valuation Profile)
  * `chart2_correlation_heatmap.png` (Feature Weights Matrix)
  * `chart3_actual_vs_predicted.png` (Optimal Model Alignment)

---

## 📊 Core Model Evaluation Summary
Contrary to initial non-linear expectations, the baseline **Linear Regression** model outperformed the ensemble Random Forest Regressor across all primary evaluation metrics:

| Machine Learning Model | Mean Absolute Error (MAE) | Root Mean Squared Error (RMSE) | R² Score |
| :--- | :---: | :---: | :---: |
| **Linear Regression (Best Model)** | 970,043.40 | 1,324,506.96 | **0.6529** |
| **Random Forest Regressor** | 1,021,546.04 | 1,400,565.97 | 0.6119 |

### Key Takeaway:
The superior performance of the linear baseline indicates that the structural and amenity assets within this specific dataset scale in a highly linear fashion with property values. Complex ensemble models over-compensated for non-existent non-linear complexities, leading to a slight drop in generalization accuracy on the test set.

---

## 💡 Key Market Insights & Business Recommendations
* **Primary Drivers:** Physical asset size (**`area`** correlation at **0.54**) and the number of **`bathrooms`** (**0.52**) hold the strongest positive relationships with market price.
* **Renovation Priority:** Adding climate control features (`airconditioning`) and vertical space (`stories`) yields a significantly higher statistical correlation to price than simply scaling basic bedroom counts.
* **Staging Strategy:** An unfurnished status acts as a strong downward anchor on property value (**-0.28**). Deploying strategic staging furniture can neutralize this negative premium and maximize resale margins.
