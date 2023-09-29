# Module 12 Report Template


### Overview of the Analysis

#### **Purpose of the Analysis**

The primary objective of this analysis was to develop a machine learning model capable of predicting the credit risk associated with various loans. By accurately assessing the risk levels of potential borrowers, financial institutions can make informed decisions, thereby minimizing the risk of loan defaults and maintaining a healthy financial portfolio.

#### **Financial Information Analyzed**

 * The analysis leveraged a comprehensive dataset comprising various financial and non-financial attributes of different loans.  * The primary focus was to predict the loan status, which was categorized into two groups: "healthy loans" (0) representing a low risk of default and "high-risk loans" (1) representing a high probability of default. 
 * The dataset included features such as credit score, loan size, and other pertinent details that are traditionally used to assess credit risk.

#### **Variables Predicted**

The target variable was the loan status, which was binary:

- **Healthy loans (0):** These represent loans that have a low risk of default. The dataset contained a substantial number of healthy loans.
- **High-risk loans (1):** These represent loans with a high risk of default. The dataset contained a smaller but significant number of high-risk loans.

The `value_counts` function was used to quantify the distribution of healthy and high-risk loans in the dataset, helping to identify the class imbalance inherent in the data.

#### **Stages of the Machine Learning Process**

The machine learning process was carried out in several stages:

1. **Data Preprocessing:** The initial stage involved cleaning and preparing the data for analysis, which included handling missing values and encoding categorical variables.
   
2. **Feature Selection and Engineering:** This stage involved selecting the most relevant features to use in the model and potentially creating new features to improve the model's predictive power.
   
3. **Data Splitting:** The data was split into training and testing sets to facilitate the training and evaluation of the model.
   
4. **Model Training:** The logistic regression model was trained using the training data set.

5. **Resampling:** Due to the class imbalance identified in the initial analysis, resampling techniques were employed using the `RandomOverSampler` module to create a balanced training dataset.

6. **Model Evaluation:** The model's performance was evaluated using a variety of metrics, including accuracy score, precision, and recall, derived from the confusion matrix and classification report.

#### **Methods Used**

To achieve the analysis objectives, various methods and techniques were employed:

- **Logistic Regression:** A logistic regression model was used for its ability to predict binary outcomes effectively, making it suitable for predicting the binary loan status variable.

- **Random Over Sampling:** To address the class imbalance issue, random over sampling technique was employed to balance the dataset by increasing the minority class size, thus enhancing the model's predictive accuracy for the minority class.

By navigating through these stages and employing these methods, the analysis aimed to build a machine learning model capable of accurately predicting loan risks, thereby aiding financial institutions in making informed lending decisions.



### Results

In this section, we delineate the results attained from the two machine learning models utilized in this analysis: the baseline logistic regression model and the logistic regression model augmented with oversampling to address class imbalance.

#### **Machine Learning Model 2: Logistic Regression with Oversampled Data**

- **Balanced Accuracy Score:**
  * **Score:** 99.37%
  * **Interpretation:** The model showcases an excellent ability to predict both healthy and high-risk loans accurately, as reflected by the high balanced accuracy score.

- **Precision:**

  * **Healthy Loans (0):**
    * **Score:** 100%
    * **Interpretation:** The model demonstrates perfect precision for healthy loans, indicating no false positives in the predictions; every loan predicted as healthy was indeed healthy.

  * **High-Risk Loans (1):**
    * **Score:** 84%
    * **Interpretation:** While the precision for high-risk loans is slightly lower, it is still quite high, showcasing the model's robustness in predicting high-risk loans with a reasonable degree of confidence.

- **Recall:**

  * **Healthy Loans (0):**
    * **Score:** 99%
    * **Interpretation:** The model correctly identified 99% of all actual healthy loans, showcasing its high sensitivity in detecting healthy loans.

  * **High-Risk Loans (1):**
    * **Score:** 99%
    * **Interpretation:** Similarly, for high-risk loans, the model exhibited a high recall rate, accurately identifying 99% of all the high-risk loans in the dataset.

In this section, we have highlighted the performance metrics of the two machine learning models in terms of balanced accuracy, precision, and recall scores. The scores indicate the robustness of each model in predicting loan statuses accurately, with particular emphasis on the model trained with oversampled data showcasing superior performance.



### Summary

In the course of this analysis, we developed and assessed two logistic regression models to predict the credit risk associated with various loans. The first model was trained using the original dataset, while the second model benefited from oversampling to create a balanced dataset, enhancing its ability to predict the minority class (high-risk loans). Here we summarize the performance of these models and provide a recommendation based on their results.

#### **Performance Summary**

- **Machine Learning Model 2 (Oversampled Data)**
  - **Performance:** The second model, trained with oversampled data, demonstrated remarkable predictive power, as evidenced by the high balanced accuracy score of 99.37%. Moreover, it achieved high precision and recall scores, particularly impressive in identifying high-risk loans.
  - **Best Use Cases:** Given its high recall score for high-risk loans, this model would be extremely beneficial in scenarios where identifying potential defaults is a priority to mitigate financial risk.

#### **Recommendation**

Based on the evaluated metrics, it is apparent that Machine Learning Model 2, which utilized oversampled data, stands out as the superior choice. This conclusion is drawn from its high balanced accuracy score and exceptional recall rates for both healthy and high-risk loans, indicating a high degree of reliability in predicting both categories accurately. 

The decision on the best model also substantially depends on the specific problem we are aiming to address. In the context of credit risk assessment:
- **Predicting 1’s (High-Risk Loans):** Given that high-risk loans carry a greater financial risk, a model with a high recall rate for predicting 1’s would be more desirable to minimize potential defaults.
- **Predicting 0’s (Healthy Loans):** Meanwhile, accurately predicting healthy loans is also crucial to ensure business growth by granting loans to reliable borrowers. 

Given that Machine Learning Model 2 exhibits high recall rates for both categories, it emerges as a well-balanced solution capable of addressing both aspects effectively.

Therefore, we recommend adopting Machine Learning Model 2 trained with oversampled data for credit risk analysis. This recommendation is grounded in the model's proven ability to accurately identify both healthy and high-risk loans, thus providing a robust tool for making informed and risk-mitigated lending decisions.

We advise, however, that as with any machine learning model, it should be continually monitored and adjusted based on its real-world performance to ensure sustained accuracy and reliability.
