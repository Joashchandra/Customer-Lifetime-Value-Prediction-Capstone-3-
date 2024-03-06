**Background**

Recognizing the importance of understanding the long-term value of its customers, a car insurance company aims to optimize marketing strategies, prioritize resource allocation, and enhance profitability. Accurately predicting Customer Lifetime Value (CLV) allows the car insurance company to forecast future revenue streams and better understand the overall value that each customer contributes to the business over their lifetime. This insight enables the car insurance company to make informed decisions regarding customer acquisition, retention, and engagement strategies. By leveraging CLV predictions, the car insurance company can allocate resources more efficiently, target marketing efforts more effectively, and ultimately improve its bottom line.

**Problem Statement**

The car insurance company lacks a dependable method to anticipate the future value of individual customers over their tenure with the company. In the absence of accurate CLV predictions, the company encounters challenges in allocating marketing budgets optimally, distinguishing between high and low-value customers, and implementing tailored retention tactics.

**Goals**

Given the stated problem, the primary objective is to develop an accurate prediction model for the company's Customer Lifetime Value (CLV).

**Analytic Approach**

Firstly, we will clean and preprocess the dataset by addressing missing values, duplicated data, and outliers. Subsequently, we will perform exploratory data analysis to uncover underlying patterns and relationships within the dataset. Once we have gained insights from the data, we will split it into features and target variables. Following this, we will compare the datasets with and without outliers, as well as with and without scaling. Next, we will select the top three models and perform hyperparameter tuning to determine the best model among them.

**Metric Evaluation**

1. **Root Mean Squared Error (RMSE)**: Measures the average magnitude of errors between predicted and actual CLV values. Lower RMSE values indicate better accuracy, indicating that predictions are closer to the actual values.
2. **Mean Absolute Error (MAE)**: Calculates the average absolute difference between predicted and actual CLV values. Lower MAE values represent smaller prediction errors and better model performance.
3. **R-Squared (R^2)**: Evaluates the goodness of fit of the CLV prediction model by quantifying the proportion of variance in CLV values explained by the model. Higher R-squared values signify better model performance and capture more variability in CLV.
4. **Mean Absolute Percentage Error (MAPE)**: Computes the average percentage difference between predicted and actual CLV values. MAPE offers insights into relative prediction accuracy, considering the scale of values. It's expressed as a percentage.

MAPE is chosen because it provides insights into how accurate the CLV predictions are relative to the actual values, regardless of their scale. It calculates the average percentage difference between predicted and actual CLV values, making it easy to interpret and compare across different datasets or models.

**Data Understanding**

- The dataset is about the Customer lifetime value of a vehicle insurance company.

**Attributes Information**

| **Feature** | **Data Type** | **Description** |
| --- | --- | --- |
| Vehicle Class | Object | This column categorizes vehicles into different classes |
| Coverage | Object | This column reflects the level of insurance coverage chosen by the customer |
| Renew Offer Type | Object | This column indicates the type of renewal offer extended to the customer |
| EmploymentStatus | Object | This column describes the employment status of the customer |
| Marital Status | Object | This column indicates the marital status of the customer  |
| Education | Object | This column describes the highest level of education of the customer |
| Number of Policies | Float | This column indicates the total number of policies held by the customer with the insurance company |
| Monthly Premium Auto | Float | This column indicates the monthly premium amount of money paid monthly for auto insurance |
| Total Claim Amount | Float | This column represents the total amount claimed by each customer |
| Income | Float | This column represents the income of each customer |
| Customer Lifetime Value | Float | This column represent the lifetime value of the customer to the insurance company |

**Conclusion**

Based on the conducted tests, the following conclusions can be drawn:
1. Among the 10 models listed, Random Forest, Decision Tree, and Gradient Boosting emerge as the top 3 best-performing models.
2. The dataset without outliers consistently outperforms the dataset with outliers.
3. There is no significant difference in the test scores with or without scaling.
4. Although Random Forest initially showed the best performance, after hyperparameter tuning, Gradient Boosting emerged as the superior model.
5. The accuracy above 9000 CLV of the final best model become less accurate.

**Recommendation**

Here are some recommendations we can consider:
1. To potentially enhance the MAPE score further, we could explore adding additional parameters for testing during hyperparameter tuning.
2. We may also experiment with grid search instead of randomized search to systematically explore a broader range of hyperparameter combinations.
3. Given that all tree-based models yielded superior results based on our observations, we might want to incorporate more tree-based models into our model benchmarking process to ensure comprehensive evaluation.
4. It's essential to prioritize features such as `Number of Policies`, `Monthly Premium Auto`, and `Income`, as they appear to be significant predictors based on our analysis. These features should be given special attention during feature selection and model training.
