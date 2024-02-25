Note: To run this file, you will need a Kaggle.json file that has an API token from Kaggle. You will have to upload that token in the 2nd cell. Then the program will be able run. [click here to download]([(https://drive.google.com/file/d/1DxR-pfG8j7n0INhKo0dmvo64u6915CCn/view?usp=share_link)https://drive.google.com/file/d/1DxR-pfG8j7n0INhKo0dmvo64u6915CCn/view?usp=share_link])

***Highlight of the project***
**Data Imputation Strategy for ICU Admission Prediction Project**

In the course of developing a machine learning model to predict ICU admission based on medical information, a significant challenge surfaced — handling missing data entries. The conventional methods such as mean, median, or average imputation proved ineffective due to the unique nature of the dataset. Each patient had five entries, and missing values were prevalent, with almost every patient having at least one entry.

Given the specific instructions in the dataset, entries were recorded regularly. However, when a patient's condition remained stable, no additional entries were made. Leveraging this insight, a novel imputation strategy was devised to fill missing values based on the last available data.

Here's a breakdown of the imputation process:

1. **Single Entry Scenario:**
   - If there is a value at the 0 index and no values at 1-4 indices, the value at the 0 index is used to fill the missing entries.

2. **Sparse Entries Scenario:**
   - If there are values at the 0 and 3 indices, the value at the 0 index is used to fill indices 1 and 2, while the value at the 3 index is used to fill indices 4 and 5.

3. **Single Value Scenario:**
   - If there is only one value at the 3 or 5 index, that value is filled across all remaining indices.

This customized imputation approach not only respects the irregularities in the data but also aligns with the underlying pattern of data recording. By strategically utilizing the last available data points, the imputation process ensures a more contextually relevant and accurate representation of missing values.

This method not only proved effective in addressing missing data challenges but also contributed to the robustness of the predictive model, making it a valuable component of the ICU admission prediction project.
**That not only improved the accuracy of the results but the specificity of the results as well.
