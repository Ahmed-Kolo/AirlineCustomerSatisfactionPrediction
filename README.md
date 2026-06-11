# Airline Customer Satisfaction Prediction

## Project Overview
This project focuses on building and optimizing a machine learning model to predict airline customer satisfaction based on various service and flight-related features. Utilizing Python and the Scikit-learn library, a Random Forest classification model was developed, fine-tuned, and evaluated. The goal is to identify key drivers of satisfaction and provide actionable insights for airline management to enhance the customer experience.

## Project Structure
-   **Data Loading and Initial Exploration**: Loading the dataset and performing initial checks on data types and missing values.
-   **Data Preprocessing**: Handling missing data, analyzing categorical features, and encoding them for model compatibility.
-   **Data Splitting**: Implementing a rigorous three-way split into training, validation, and test sets.
-   **Hyperparameter Tuning**: Optimizing the Random Forest model using `GridSearchCV` and `PredefinedSplit`.
-   **Model Evaluation**: Assessing model performance using various metrics on an unseen test set.
-   **Model Comparison**: Comparing the optimized Random Forest model with a baseline Decision Tree model.
-   **Feature Importance Analysis**: Identifying the most influential factors contributing to customer satisfaction.
-   **Executive Summary and Recommendations**: Summarizing findings and providing strategic recommendations for the airline.

## Methodology

### Data Source
The dataset used for this analysis is `Invistico_Airline.csv`, containing various features related to airline passenger experiences and their satisfaction levels.

### Data Preprocessing
1.  **Missing Values**: Missing values in the 'Arrival Delay in Minutes' column were imputed using the median value of the column.
2.  **Categorical Feature Analysis**: Unique values and counts for categorical columns (`satisfaction`, `Customer Type`, `Type of Travel`, `Class`) were inspected.
3.  **Encoding Categorical Features**: 
    *   The target variable 'satisfaction' was converted to a numerical format (`dissatisfied`: 0, `satisfied`: 1).
    *   Remaining categorical features (`Customer Type`, `Type of Travel`, `Class`) were one-hot encoded using `pd.get_dummies`, with `drop_first=True` to avoid multicollinearity.

### Data Splitting Strategy
The preprocessed data was rigorously split into three sets:
-   **Training Set (70%)**: Used for model training.
-   **Validation Set (15%)**: Used during hyperparameter tuning with `GridSearchCV`.
-   **Test Set (15%)**: A completely held-out set for final, unbiased model evaluation.

This three-way split ensures robust evaluation and helps prevent data leakage.

### Hyperparameter Tuning
`GridSearchCV` combined with `PredefinedSplit` was employed to systematically search for the optimal hyperparameters for the Random Forest Classifier. The `PredefinedSplit` ensured that the validation set was used consistently during the grid search. The following hyperparameters were tuned:
-   `n_estimators`: Number of trees in the forest (e.g., 50, 100, 200)
-   `max_depth`: Maximum depth of each tree (e.g., 10, 20, 30, None)
-   `min_samples_leaf`: Minimum number of samples required to be at a leaf node (e.g., 1, 2, 4)

### Model Evaluation
The best Random Forest model was evaluated on the unseen test set using standard classification metrics:

-   **Accuracy**: Overall correctness of predictions.
-   **Precision**: The proportion of positive identifications that were actually correct.
-   **Recall**: The proportion of actual positives that were correctly identified.
-   **F1-Score**: The harmonic mean of Precision and Recall. It is particularly useful for imbalanced datasets as it balances both false positives and false negatives, providing a comprehensive measure of accuracy.

## Results and Analysis

### Model Performance Comparison

| Model           | Accuracy | Precision | Recall | F1-Score |
| :-------------- | :------- | :-------- | :----- | :------- |
| Random Forest   | 0.9538   | 0.9664    | 0.9486 | 0.9574   |
| Decision Tree   | 0.9305   | 0.9355    | 0.9376 | 0.9366   |

The Random Forest model significantly outperformed the baseline Decision Tree model across all metrics, demonstrating superior generalization capabilities and robustness. This indicates that the ensemble approach of Random Forest effectively mitigates overfitting and provides a more reliable prediction of customer satisfaction.

### Key Satisfaction Drivers (Top 5 Feature Importances)
Based on the Random Forest model, the most influential factors impacting passenger satisfaction are:

1.  **Inflight entertainment:** `0.2136`
2.  **Seat comfort:** `0.1379`
3.  **Ease of Online booking:** `0.0832`
4.  **Online support:** `0.0574`
5.  **Leg room service:** `0.0447`

These features contribute most significantly to the model's predictive power, highlighting their importance in shaping the overall customer experience.

## Recommendations for Airline Leadership

To enhance customer satisfaction and loyalty, airline management should focus on strategic improvements in the following areas:

*   **Prioritize Inflight Entertainment**: Given its highest importance score, investing in diverse and high-quality inflight entertainment options could significantly boost passenger satisfaction. This includes updated content libraries, reliable personal screens, and potentially offering a wider range of connectivity options.
*   **Improve Seat Comfort**: As the second most crucial factor, initiatives to enhance seat design, ergonomics, and space, especially on longer flights, are essential. This could involve exploring new seat technologies or offering more flexible seating configurations.
*   **Optimize Online Booking Experience**: Streamlining and simplifying the online booking process is vital. Ensuring a user-friendly interface, clear communication, and efficient functionality will reduce friction and improve the customer journey from the outset.
*   **Strengthen Online Support**: Reliable and responsive online support is critical. Airlines should ensure that their digital support channels (e.g., chat, FAQs, social media response teams) are efficient, informative, and easily accessible to address passenger queries and issues promptly.
*   **Enhance Leg Room Service**: While a lower priority than the top factors, offering competitive legroom options and ensuring consistent service in this area can contribute positively to the overall comfort and satisfaction of passengers.

By focusing resources on these key drivers, the airline can strategically improve its service offerings, directly address passenger pain points, and ultimately foster greater satisfaction and business success.

## Technologies Used
-   Python
-   pandas
-   scikit-learn
-   matplotlib
-   seaborn
```
