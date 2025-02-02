# Machine Learning Algorithm to Predict Startup Success or Failure

In this notebook, I've applied machine learning techniques to predict whether a startup will succeed or fail based on data available at the time of investment. The dataset used in this analysis is sourced from [this repository](https://github.com/daniel7an/Startup-Success-Analysis/blob/main/data.csv).

## Approach

I trained two classification models:
- **Logistic Regression**
- **Random Forest Classifier**

These models were used to predict startup success or failure. For this task, I focused only on the categorical (classification) features, as the continuous features contained too many missing values (NaNs). A potential improvement in future iterations could be to handle these missing values more effectively, perhaps by imputing the NaNs or incorporating additional features like the number of employees.

### Key Focus: High True Positive Rate (TPR) with Controlled False Positive Rate (FPR)

In this project, the primary goal was to maximize the True Positive Rate (TPR) while maintaining a reasonable False Positive Rate (FPR). This is particularly important for a VC fund, which wants to minimize the chances of overlooking successful startups, as missing potential winners leads to significant opportunity costs (referred to as "manque à gagner").

### Future Improvements

- **Money Funded**: If a column detailing the amount of money invested by the VC fund was available, we could build a custom scoring system. This scoring method could calculate the financial impact (losses) of misclassified instances, allowing us to better prioritize which startups to focus on.

## Model Performance

The final models achieved the following performance metrics:

- **Precision**: 0.98
- **Accuracy**: 0.82

These results demonstrate a strong ability to classify successful startups with high precision, while maintaining a reasonable accuracy.

