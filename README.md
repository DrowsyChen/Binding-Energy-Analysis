# Binding-Energy-Analysis of $C_3N$
This repository provides a complete pipeline for analyzing the binding energy of a series of $C_3N$ structure using Support Vector Regression (SVR) combined with Principal Component Analysis (PCA), grid search optimization, cross-validation, and feature importance analysis (SHAP and permutation importance).

The project includes:
1. Data preprocessing
2. Dimensionality reduction (PCA)
3. Hyperparameter tuning of SVR
4. Model evaluation with $R^2$ and MSE
5. Feature importance evaluation (SHAP)

## Library Requirements
```pandas numpy matplotlib scikit-learn shap openpyxl```

## Usage
1. Download or Prepare the dataset as an Excel file (.xlsx) with the following columns:
    + Missing-N
    + Misplaced-N
    + Distance
    + Groups
    + Binding_Energy
2. Edit file paths on your own computer as follow:
```
file_read = 'your_file_path_1'   # Input dataset (.xlsx)
output_dir = 'your_file_path_2'  # Output directory for results
```
3. Run the program:
```
python svr_binding_energy.py
```
4. Outputs:
+ SVR.xlsx: PCA data and contour matrices.
+ SVR_Contour_Figure.png: Contour visualization of binding energy prediction.
+ Feature_Importance.xlsx: SHAP values, permutation importance, and combined importance.


## File Structure
```
.
├── svr_binding_energy.py      # Main program
└── README.md                  # Documentation
```
