# Casual-Lending

## Project Overview
The Casual Lending project involves the exploration and modeling of a loan eligibility dataset to better understand the factors that influence loan approval. By utilizing data preprocessing, feature engineering, and causal inference techniques, this project aims to uncover the relationships between various applicant attributes and their impact on loan approval outcomes. The project involves the use of Python libraries such as NumPy, Pandas, LightGBM, and DoWhy for data analysis and modeling.

## Dataset
The project uses a dataset containing information about loan applicants, their financial details, and loan approval outcomes. The dataset includes features like gender, marital status, education level, credit history, property area, loan amount, loan amount term, total income, and more. The target variable is the loan approval status (0 for not approved and 1 for approved).

## Data Preprocessing
The dataset is initially loaded, and missing values in categorical variables are handled by replacing them with the mode value, while numerical variables are filled with the mean. Certain columns deemed irrelevant are dropped, and a new feature 'TotalIncome' is created by summing up 'ApplicantIncome' and 'CoapplicantIncome'. The 'TotalIncome', 'LoanAmount', and 'Loan_Amount_Term' columns are scaled using MinMaxScaler for uniformity.

## Feature Engineering
An additional feature 'Appreciability' is introduced to capture the appreciation potential of the loan for each applicant based on their financial attributes. Another feature 'IncomeComb' is created to combine 'Education' and 'Self_Employed' features, indicating whether the applicant has a stable income source.

## Causal Inference
A causal graph is constructed to model the relationships between variables. The graph indicates the potential causal pathways among the variables. Notable causal relationships include 'Credit_History' affecting 'Loan_Status', 'Property_Area' influencing 'LoanAmount', and 'TotalIncome' impacting 'Loan_Status'. 

## Model Development
The dataset is divided into training and test sets for model evaluation. A LightGBM classifier is trained on the training data to predict 'Loan_Status'. To ensure fairness and avoid discrimination, the trained model is used to generate counterfactual samples for various applicant profiles. This allows us to observe the predicted outcomes if certain variables were different while keeping others constant.

## Results and Analysis
The project yields insights into the factors affecting loan approval decisions. The causal graph helps identify the potential causal relationships between different attributes. The trained model provides predictions on loan approval probabilities, allowing us to evaluate the impact of changing specific features on the outcome.
![causal_graph](https://github.com/LoopGlitch26/Casual-Lending/assets/53336715/55a40437-367a-4c46-b5b2-0a24e0f8f7c1)


## Business Implications
This project has several business implications for the lending institution. The causal analysis can assist in making informed decisions about which factors to focus on when making loan approval decisions. The counterfactual samples provide a way to understand how loan approval outcomes might change under different circumstances, helping the institution make fair and equitable decisions.

## Conclusion
The project successfully explores loan eligibility data, preprocesses and engineers features, and builds a predictive model. The causal analysis sheds light on the underlying relationships between variables, and the counterfactual analysis offers insights into how different attributes impact loan approval decisions. This project contributes valuable information for a lending institution to make informed and fair lending decisions while adhering to industry regulations and practices.
![interpretation_graph](https://github.com/LoopGlitch26/Casual-Lending/assets/53336715/5d448237-fc46-4aa9-befd-a6c8df6d2009)

