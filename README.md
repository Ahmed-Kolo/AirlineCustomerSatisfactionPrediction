
# Airline Customer Satisfaction Prediction

## Project Overview

This project focuses on building and optimizing a Random Forest classification model to predict airline customer satisfaction based on passenger survey data. The analysis involves data preprocessing, a three-way data split (training, validation, testing), hyperparameter tuning using `GridSearchCV` with `PredefinedSplit`, model evaluation, and a comparison with a simpler Decision Tree model. The goal is to identify key drivers of customer satisfaction and provide actionable recommendations for airline management.

## Key Results

### Model Performance Comparison

After comprehensive hyperparameter tuning, the **Random Forest model** demonstrated superior performance compared to a baseline **Decision Tree model** on the held-out test set:

*   **Random Forest Model:**
    *   Accuracy: `0.9538`
    *   Precision: `0.9664`
    *   Recall: `0.9486`
    *   F1-Score: `0.9574`

*   **Decision Tree Model:**
    *   Accuracy: `0.9305`
    *   Precision: `0.9355`
    *   Recall: `0.9376`
    *   F1-Score: `0.9366`

The Random Forest model's higher metrics across the board confirm its robustness and better generalization capabilities for predicting airline customer satisfaction.

### Top 5 Feature Importances

Analysis of feature importance from the optimized Random Forest model revealed the most influential factors driving customer satisfaction:

1.  **Inflight entertainment:** (Importance: `0.2136`)
2.  **Seat comfort:** (Importance: `0.1379`)
3.  **Ease of Online booking:** (Importance: `0.0832`)
4.  **Online support:** (Importance: `0.0574`)
5.  **Leg room service:** (Importance: `0.0447`)

These features are critical in shaping the overall customer experience and have the most significant impact on satisfaction levels.

## Recommendations

Based on these findings, airline leadership is recommended to:

*   **Prioritize enhancements in inflight entertainment** to significantly boost passenger satisfaction.
*   **Invest in improving seat comfort** through better design and ergonomics.
*   **Optimize the online booking experience** for greater ease and efficiency.
*   **Strengthen online support channels** to ensure responsive and effective assistance.
*   **Consider improvements to legroom services** to further enhance passenger comfort.

By strategically focusing on these key areas, the airline can effectively improve service offerings, address passenger pain points, and foster higher customer satisfaction and loyalty.
```
