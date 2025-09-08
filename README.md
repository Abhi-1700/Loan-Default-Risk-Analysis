# Loan-Default-Risk-Analysis
analyzes a loan dataset (2007–2011) to identify variables that indicate whether a person is likely to default on a loan

This project analyzes a loan dataset (2007–2011) to identify variables that indicate whether a person is likely to default on a loan. Such insights are useful for financial institutions to detect risky loan applicants and reduce financial losses.

The project involves data cleaning, feature engineering, exploratory data analysis (EDA), and visualization using Python.

**Dataset Description**

The dataset contains loan records with various borrower attributes and loan details.

annual_inc → Self-reported annual income of the borrower.

dti → Debt-to-income ratio.

emp_length → Employment length (0–10 years).

funded_amnt / funded_amnt_inv → Loan amount funded by company/investors.

grade → Loan grade assigned by Lending Club.

int_rate → Loan interest rate.

installment → Monthly payment owed by the borrower.

loan_amnt → Amount applied for by the borrower.

loan_status → Current status of the loan (Fully Paid, Charged Off, etc.).

term → Loan term in months (36 or 60).

purpose → Purpose of the loan (credit card, debt consolidation, etc.).


**Project Objectives**

The following tasks were performed step by step:

Import and explore the dataset.

Find number of rows and columns.

Convert int_rate column from string to float using a lambda function.

Check data types of all columns.

Clean dataset by removing columns with all NaN values.

Analyze loan_status column and filter only “Fully Paid” and “Charged Off” loans.

Extract numerical values from emp_length column (e.g., < 1 year → 1).

Clean term column (e.g., 36 months → 36).

Create a new feature risky_loan_applicant:

      0 → If loan_amnt <= funded_amnt

      1 → If loan_amnt > funded_amnt

Visualize loan_status against categorical variables: grade, term, verification_status.

Convert emp_length into categories:

    fresher → emp_len ≤ 1

    junior → 1 < emp_len < 3

    senior → 3 ≤ emp_len < 7

    expert → emp_len ≥ 7

Find the sum of loan_amnt for each grade and visualize using a pie chart.

**📊 Visualizations**

Bar Plots: Loan Status vs Grade, Term, Verification Status.

Pie Plot: Loan amount distribution by Grade.

These help in identifying patterns in loan repayment and risk profiles across borrower categories.

total_acc → Total credit lines of the borrower.

total_pymnt / total_pymnt_inv / total_rec_int → Payments and interest received.
