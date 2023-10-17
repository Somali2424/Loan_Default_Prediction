# Loan_Default_Prediction
**Title: Loan Default Prediction Using PyCaret AutoML**
Introduction:

In this project, we have worked with a dataset comprising 10,000 pieces of information that can assist us in determining whether an individual is likely to fail to repay a loan. This dataset contains four critical factors: employment status, bank balance at the time of data collection, annual salary, and a binary indicator for loan default (0 for 'defaulted' and 1 for 'not defaulted'). The significance of this project lies in its ability to aid financial organizations in making informed decisions when granting loans to individuals.

Exploratory Data Analysis:

Our journey began with exploratory data analysis (EDA), where we undertook several essential steps. We checked for null values, renamed the column 'Defaulted?' to 'Defaulted,' and created a pie chart to understand the distribution of loan default status among our clients. Subsequently, we segregated clients into two groups based on their employment status: employed and unemployed. This allowed us to examine how the target variable, loan default, is distributed among these distinct groups.

Upon separating the data, we examined the class balance within each group. We discovered that unemployed individuals tend to default more often than their employed counterparts. Furthermore, clients who defaulted on their loans exhibited higher bank balances on average than those who did not.

Modeling and Recall Scores:

As we delved into modeling, we observed a fascinating trend: there is a threshold below which individuals with higher annual incomes are more likely to default, and above that threshold, the higher-income group is more prone to default. Additionally, we found no strong correlations between the target variable and any other attributes.

We decided to employ the recall score as our primary evaluation metric. Recall measures our model's ability to correctly predict defaulters, which is crucial for minimizing financial losses to the institution. We aimed to keep false negatives to a minimum, as they represent defaulters who were incorrectly classified as non-defaulters by the model.

Using PyCaret AutoML:

To build and evaluate our models, we leveraged the PyCaret AutoML library. PyCaret enabled us to train and validate our models on a hold-out sample of the training set. We divided our data into a training set, with 75% allocated for training and 25% for validation.

Considering the high cost associated with false negatives and the institution's goal to minimize such occurrences, we focused on maximizing recall. PyCaret allowed us to run 16 different classification algorithms, and we identified the model with the best recall performance. After fine-tuning and testing, we achieved an impressive recall score of 89.55% on unseen data, correctly predicting 60 out of 67 defaulters.

Conclusion:

This project's success in building a robust loan default prediction model using PyCaret's AutoML capabilities is a significant achievement. By focusing on the recall metric, we've demonstrated the model's ability to accurately identify potential defaulters, thus reducing the institution's financial risk. This model can be a valuable tool for financial organizations to make more informed decisions when granting loans to individuals, ultimately enhancing their overall financial stability.

