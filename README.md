# 💉 HbA1C Value Prediction with Regression Models

This repository contains a machine learning project focused on predicting **Glycated Hemoglobin (HbA1c)** values, a key indicator for diagnosing and managing diabetes, using various linear regression techniques.

The project explores and compares the performance of baseline and regularized linear models to provide an accurate predictive tool based on patient data.

## 🌟 Models Implemented

The analysis is performed within Jupyter Notebooks, comparing the efficacy of three different regression algorithms from the `scikit-learn` library:

| Model | Purpose | Notebook File |
| :--- | :--- | :--- |
| **Standard Linear Regression** | Establishes a baseline for prediction using the Ordinary Least Squares method. | `Diabetes_linearregression.ipynb` |
| **Ridge Regression (L2)** | Applies L2 regularization to handle multicollinearity and prevent overfitting by penalizing large coefficients. | `Diabetes_lasso_ridge.ipynb` |
| **Lasso Regression (L1)** | Applies L1 regularization for feature selection by shrinking the coefficients of less important features to zero. | `Diabetes_lasso_ridge.ipynb` |

## 🚀 Getting Started

Follow these instructions to set up and run the project notebooks locally.

### Prerequisites

The project requires **Python 3.x** and the following libraries. You will need to install these if they are not already present:

* `pandas`
* `numpy`
* `scikit-learn`
* `matplotlib` (for visualizations)
* `seaborn` (for visualizations)
* `jupyter` (to run the notebooks)

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Soumyals/HbA1C-Value-Prediction.git](https://github.com/Soumyals/HbA1C-Value-Prediction.git)
    cd HbA1C-Value-Prediction
    ```

2.  **Install the necessary packages:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn jupyter
    ```
    *(**Note**: A `requirements.txt` file is recommended for a production environment, but the manual install above should suffice.)*

### Execution

1.  **Start the Jupyter Notebook server:**
    ```bash
    jupyter notebook
    ```

2.  Open the following notebooks in your browser to run the analysis:
    * **`Diabetes_linearregression.ipynb`**: For the standard model and baseline performance.
    * **`Diabetes_lasso_ridge.ipynb`**: For the analysis using regularized (Lasso and Ridge) models.

***

## 📂 Repository Structure
