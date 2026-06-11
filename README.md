# Airline Customer Satisfaction Prediction

## Project Overview

This project focuses on analyzing passenger survey data to predict airline customer satisfaction using Python and the Scikit-learn library. The goal is to build and optimize a machine learning model, specifically a Random Forest classifier, to accurately identify factors influencing satisfaction and provide actionable insights for airline management.

## Executive Summary and Recommendations

### Model Performance Overview

Our analysis developed and optimized a Random Forest classification model to predict airline customer satisfaction, comparing its performance against a single Decision Tree model. The Random Forest model significantly outperformed the Decision Tree model on the held-out test set:

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

The Random Forest model demonstrated superior generalization capabilities, indicating its effectiveness in mitigating overfitting compared to a single Decision Tree. This robust performance makes the Random Forest model a reliable tool for predicting passenger satisfaction.

### Key Satisfaction Drivers (Top 5 Feature Importances)

Based on the Random Forest model, the most influential factors impacting passenger satisfaction are:

1.  **Inflight entertainment:** `0.2136`
2.  **Seat comfort:** `0.1379`
3.  **Ease of Online booking:** `0.0832`
4.  **Online support:** `0.0574`
5.  **Leg room service:** `0.0447`

These features contribute most significantly to the model's predictive power, highlighting their importance in shaping the overall customer experience.

### Recommendations for Airline Leadership

To enhance customer satisfaction and loyalty, airline management should focus on strategic improvements in the following areas:

*   **Prioritize Inflight Entertainment:** Given its highest importance score, investing in diverse and high-quality inflight entertainment options could significantly boost passenger satisfaction. This includes updated content libraries, reliable personal screens, and potentially offering a wider range of connectivity options.
*   **Improve Seat Comfort:** As the second most crucial factor, initiatives to enhance seat design, ergonomics, and space, especially on longer flights, are essential. This could involve exploring new seat technologies or offering more flexible seating configurations.
*   **Optimize Online Booking Experience:** Streamlining and simplifying the online booking process is vital. Ensuring a user-friendly interface, clear communication, and efficient functionality will reduce friction and improve the customer journey from the outset.
*   **Strengthen Online Support:** Reliable and responsive online support is critical. Airlines should ensure that their digital support channels (e.g., chat, FAQs, social media response teams) are efficient, informative, and easily accessible to address passenger queries and issues promptly.
*   **Enhance Leg Room Service:** While a lower priority than the top factors, offering competitive legroom options and ensuring consistent service in this area can contribute positively to the overall comfort and satisfaction of passengers.

By focusing resources on these key drivers, the airline can strategically improve its service offerings, directly address passenger pain points, and ultimately foster greater satisfaction and business success.

## Conclusion

This project successfully demonstrated the process of building, optimizing, and evaluating a Random Forest classification model for predicting airline customer satisfaction. We performed a rigorous three-way data split, hyperparameter tuned with `GridSearchCV` and `PredefinedSplit`, and identified key drivers of satisfaction. The Random Forest model proved to be a robust and accurate predictor compared to a single Decision Tree, offering valuable insights for airline management.
