# house-prices-eda-preprocessing
##  Data Cleaning, Preprocessing, and EDA

This project performs a comprehensive data cleaning, preprocessing, and exploratory data analysis (EDA) on the Ames Housing dataset. The dataset provides rich information about residential homes in Ames, Iowa, and is commonly used for predictive modeling and regression tasks.

## 📌 Objective

To explore, clean, preprocess, and derive insights from the dataset using Python and standard data science libraries. This forms a critical foundation for future machine learning modeling.

---

## 🗂️ Dataset

- **Files Used:**
  - `train.csv` — Main dataset for analysis and EDA
  - `data_description.txt` — Metadata and codebook for feature interpretation

---

## 🔍 Analysis Workflow

### 1. **Data Exploration**
- Loaded the dataset and inspected structure and types
- Identified missing values, duplicates, and inconsistent data

### 2. **Missing Value Treatment**
- Numerical features: Imputed using **mean** values
- Categorical features: Imputed using **mode** or `"None"`

### 3. **Data Visualization**
- **Histograms and boxplots** of `SalePrice` and `LotArea` to identify distribution and outliers
- **Correlation heatmap** to study relationships among numerical features

### 4. **Encoding and Feature Engineering**
- One-hot encoding applied to categorical columns: `Neighborhood`, `MSZoning`
- Boolean columns converted to binary (`True/False` → `1/0`)

### 5. **Feature Scaling**
- `LotArea` normalized using **Min-Max Scaling**
- `GrLivArea` standardized using **Z-score Scaling (StandardScaler)**

---

## 📈 Key Insights

- `OverallQual`, `GrLivArea`, `GarageCars`, and `TotalBsmtSF` show the **strongest positive correlation** with `SalePrice`.
- `SalePrice` and `LotArea` distributions are **right-skewed** and contain **extreme outliers**, indicating a need for transformation or robust modeling.
- Features like `Id`, `MiscVal`, and `MoSold` have **little to no correlation** with the target and may be dropped for modeling.

---

## 📦 Technologies Used

- Python 3.x
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn (for scaling)

---

## 📁 Outputs

- `cleaned_file.csv`: Final processed dataset ready for modeling
- EDA plots (histograms, boxplots, heatmaps)
