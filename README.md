# KC House Price Prediction Model Analysis

This report presents a comparative analysis of different machine learning models for price prediction. The models were evaluated using three key metrics: **R² Score, Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE)**. The goal was to determine the best-performing model by analyzing both raw and winsorized data.

## Model Performance Summary

| Model                               | R² Score | MAE ($)     | RMSE ($)     |
|--------------------------------------|-----------|-------------|--------------|
| **Original Price Model**             | 0.8833    | 71,019.08   | 132,799.29   |
| **Winsorized Price Model**           | 0.8671    | 57,759.84   | 92,937.23    |
| **XGBoost Model**                    | 0.9906    | 10,470.06   | 37,786.89    |
| **XGBoost Model (Winsorized)**       | 0.9976    | 7,760.38    | 12,442.22    |
| **Gradient Boosting Model**          | 0.9949    | 12,570.02   | 27,678.87    |
| **Winsorized Gradient Boosting Model** | 0.9963    | 10,447.26   | 15,607.72    |

### Key Observations:
1. Traditional regression models (**Original & Winsorized**) showed lower performance, with R² scores around **0.87-0.88** and high error metrics.
2. **Winsorization** improved all models by reducing the impact of outliers, leading to lower MAE and RMSE.
3. **XGBoost** outperformed other models, achieving an R² score of **0.9906** in its standard form and **0.9976** with Winsorization.
4. **Gradient Boosting** performed well but was slightly less accurate than **XGBoost** in both standard and winsorized versions.

## Train vs. Test Performance Comparison

### **XGBoost Model**
#### Train Performance:
- **R²**: 0.9988
- **MAE**: 7,854.37
- **RMSE**: 12,438.88

#### Test Performance:
- **R²**: 0.9906
- **MAE**: 10,470.06
- **RMSE**: 37,786.89

📌 *Observation:* The model performed well on training data but showed a slightly higher RMSE on test data, indicating minor overfitting.

### **XGBoost (Winsorized) – Best Model**
#### Train Performance:
- **R²**: 0.9985
- **MAE**: 6,560.53
- **RMSE**: 9,547.85

#### Test Performance:
- **R²**: 0.9976
- **MAE**: 7,760.38
- **RMSE**: 12,442.22

📌 *Observation:* This model achieved the best generalization, with high R² and the lowest MAE & RMSE on test data, making it the most reliable choice.

## Conclusion
✅ **XGBoost (Winsorized) is the best model for price prediction**, achieving:
- **Highest R² Score (0.9976)** → Best variance explanation
- **Lowest MAE (7,760.38) & RMSE (12,442.22)** → Most accurate predictions
- **Minimal overfitting**, indicating strong generalization performance.

💡 **Winsorization** plays a crucial role in enhancing model performance by handling outliers, reducing errors, and improving stability.

## Key Takeaways
✔ **XGBoost (Winsorized) emerged as the top performer** among all models, achieving the highest predictive accuracy and strong generalization ability.
✔ **Winsorization** was key in improving the robustness of the models by mitigating the influence of extreme outliers.
✔ The analysis suggests that **XGBoost with Winsorization is the optimal choice** for predicting house prices in this dataset.

---
📌 **Project Repository:** [GitHub Link](#) *(Replace with your actual repo link)*

