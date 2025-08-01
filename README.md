# CODECRAFT_ML_01
# 🏠 House Price Prediction using Linear Regression

## 📌 Project Overview
This project implements a **linear regression model** to predict house prices based on:
- Square footage (`GrLivArea`)
- Number of bedrooms (`BedroomAbvGr`)
- Number of bathrooms (`FullBath + 0.5 * HalfBath`)

The dataset is from the [Kaggle House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) competition.

---

## ⚙️ Steps
1. Loaded and inspected training/test datasets
2. Engineered `Bathrooms` feature
3. Selected predictors: `GrLivArea`, `BedroomAbvGr`, `Bathrooms`
4. Trained a **Linear Regression model**
5. Evaluated performance using RMSE and R²
6. Created diagnostic plots (residuals, Q–Q plot, Cook’s distance, etc.)
7. Generated predictions on the test set (`submission.csv`)

---

## 📊 Results
- **RMSE (holdout set)**: **53,863**  
- **R² (holdout set)**: ~0.63  
- **Model insights:**
  - Larger `GrLivArea` increases price (~\$100 per additional sq. ft.)
  - More `Bathrooms` significantly increase price (~\$27,000 per bathroom)
  - `BedroomAbvGr` coefficient was negative, suggesting **multicollinearity** with other features

---

## 🚀 How to Run
```bash
# Clone the repo
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# Install requirements
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook HousePricePrediction.ipynb
