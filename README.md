#  Mobile Price Prediction

---

##  Problem Statement
Given the various parameters of a mobile device, predict the price category of the device.  
Additionally:
- Identify which features most strongly influence price  
- Analyze which features contribute the least and most variation  
- Study how different features relate to device characteristics  

---

##  Group Members

- Nishant — B24CS1050  
- Amar Sisodiya — B24EE1002  
- Payal Tatawat — B24EE1057  
- Pamarthi Sunanda — B24EE1051  

##  Dataset
Dataset used:  
https://www.kaggle.com/datasets/iabhishekofficial/mobile-price-classification

##  Colab Notebook
https://colab.research.google.com/drive/10cmCM4Bz-jUwVnVtCG21mIMsg2Bt1MiH?usp=sharing

##  How to Run

1. Open the Colab notebook using the link above  
2. Run all cells sequentially  
3. The notebook will:
   - Load dataset  
   - Perform preprocessing  
   - Train models  
   - Display results and visualizations  

Alternatively:
1. Install required libraries  
2. Run the notebook locally using Jupyter/Colab

Install the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn kagglehub
```



##  Approach

We followed a structured machine learning pipeline:

1. **Exploratory Data Analysis (EDA)**
   - Analyzed feature relationships using correlation heatmaps and plots  
   - Observed strong relationship between RAM and price  

2. **Hypothesis Formation**
   - Dataset is largely **linearly separable**, primarily driven by RAM  

3. **Preprocessing**
   - Train-test split (80:20)  
   - Feature scaling using `StandardScaler`  
   - No data leakage (scaler fitted only on training data)  

4. **Modeling**
   - Logistic Regression (baseline model)  
   - Support Vector Machine (SVM)  
   - k-Nearest Neighbors (kNN)  

5. **Model Comparison**
   - Compared performance across models to validate hypothesis  

6. **Explainability**
   - Used Logistic Regression coefficients to determine feature importance  

7. **Ablation Study**
   - Removed RAM and retrained model  
   - Observed significant performance drop  

8. **Error Analysis**
   - Used confusion matrix to analyze misclassification patterns  

9. **Dimensionality Reduction**
   - Applied PCA to visualize data in 2D space  

10. **Model Validation**
   - Performed 5-fold cross-validation to ensure robustness  

---

##  Results

| Model                  | Accuracy |
|-----------------------|----------|
| Logistic Regression   | 97.5%    |
| SVM                   | 89.25%   |
| kNN                   | 60.8%      |

### Cross-Validation
- Mean accuracy: ~95%  
- Low variance across folds → model is stable and generalizes well  

---

##  Key Insights

- **RAM is the most influential feature** by a large margin  
- Logistic Regression performs best → confirms linear separability  
- Removing RAM drops accuracy from ~97.5% to ~33%  
- Errors occur only between adjacent classes (expected behavior)  
- PCA shows overlap in 2D, but separation exists in higher dimensions  

---

##  Requirements

Install the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn kagglehub
