## Casual-Lending

**Project Overview:**
- Exploration and modeling of a loan eligibility dataset to understand factors influencing loan approval.
- Utilizes data preprocessing, feature engineering, and causal inference techniques.
- Python libraries used: NumPy, Pandas, LightGBM, and DoWhy.

**Dataset:**
- Contains loan applicant details, financial data, and loan approval outcomes.
- Features include gender, marital status, education level, credit history, property area, loan amount, etc.
- Target variable: Loan approval status (0 for not approved, 1 for approved).

**Data Preprocessing:**
- Handle missing categorical values by replacing with mode, numerical values with mean.
- Drop irrelevant columns, create 'TotalIncome' by summing 'ApplicantIncome' and 'CoapplicantIncome'.
- Scale 'TotalIncome', 'LoanAmount', and 'Loan_Amount_Term' using MinMaxScaler.

**Feature Engineering:**
- Introduce 'Appreciability' to capture loan appreciation potential based on financial attributes.
- Create 'IncomeComb' to merge 'Education' and 'Self_Employed', indicating stable income source.

**Causal Inference:**
- Construct a causal graph to model variable relationships and potential causal pathways.
- Highlight relationships like 'Credit_History' -> 'Loan_Status', 'Property_Area' -> 'LoanAmount', etc.

![causal_graph](https://github.com/LoopGlitch26/Casual-Lending/assets/53336715/55a40437-367a-4c46-b5b2-0a24e0f8f7c1)


**Model Development:**
- Divide dataset into training and test sets.
- Train LightGBM classifier on training data to predict 'Loan_Status'.
- Generate counterfactual samples using the model to observe outcomes under varied attributes.

**Results and Analysis:**
- Gain insights into factors influencing loan approval.
- Causal graph reveals potential causal links between attributes.
- Trained model predicts loan approval probabilities, assess impact of changing features.

**Business Implications:**
- Assist lending institutions in informed loan approval decisions.
- Counterfactual analysis helps understand how outcomes change under different scenarios.

![interpretation_graph](https://github.com/LoopGlitch26/Casual-Lending/assets/53336715/5d448237-fc46-4aa9-befd-a6c8df6d2009)


**Conclusion:**
- Successful exploration, preprocessing, and modeling of loan data.
- Causal analysis uncovers attribute relationships.
- Counterfactual insights aid in equitable lending decisions.
- Valuable information for fair and informed lending practices.
