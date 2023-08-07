# Project Description

Hello there :wave:
I hope this project finds you well!

In this project, I will analyze the risk of borrower default and prepare report for the credit department of a bank. I will find out the influence of a customer's marital status and number of children on the probability of timely loan repayment. The bank already has some data regarding the creditworthiness of its customers.

The report will be considered when making **credit assessments** for potential customers. **Credit assessments** are used to evaluate the ability of prospective borrowers to repay their loans.

**Hypotheses**
1.   Is there a correlation between having children and repaying loans on time?
2.   Is there a correlation between family status and repaying loans on time?
3. Is there a correlation between income level and repaying loans on time?
4. Is there a correlation between the length of employment and repaying loans on time?
5.   How does the credit purpose affect the automatic rate?


# Steps

1. Exploratory Data Analysis
2. Pre-Processing Data
3. Hypothesis Testing

## 1. Exploratory Data Analysis

**Data Description** 

- `children` - number of children in the family
- `days_employed` - number of days employed
- `dob_years` - client's age in years
- `education` - client's education level
- `education_id` - education identifier
- `family_status` - marital status
- `family_status_id` - marital status identifier
- `gender` - client's gender
- `income_type` - type of employment
- `debt` - whether the client has a loan debt
- `total_income` - monthly income
- `purpose` - purpose of the loan application

## 2. Pre-Processing Data

There are several issues in dataset:
1. Discover trends in the data
2. Missing Values . I replaced the missing value with 'unknown'.
3. Outlier Data. I replaced the outlier data with median data.
4. Duplicate Data. I removed it.
5. Duplicate Implicit in column 'education'. I applied str lower to standardize the duplicate implicit.

## 3. Hypothesis Testing

The result of each hypothesis:
1.  Is there a correlation between having children and paying back on time?
	Findings:
	- Borrowers who have children tend to have a higher risk of not paying back on time.
	- However, the number of children does not show a significant trend in the borrowers' ability to repay debts, as the percentage difference between the number of children is not too large.
	
2. Is there a correlation between family status and paying back on time?
	Findings:
	- Borrowers who are not married (statuses 'Civil Partnership' and 'Unmarried') actually have the highest percentage of defaulting on payments.
	- Borrowers who are married tend to have a higher sense of awareness/responsibility to repay debts.

3. Is there a correlation between income level and paying back on time?

	Findings:
	The higher the income, the greater the likelihood of defaulting on debts.

4. Is there a correlation between the length of employment and paying back on time?
	Findings:
	Borrowers with little work experience have the highest probability of defaulting on debts. This indicates that the more work experience a borrower has, the more capable they are of assessing their ability to repay debts.
5. Is there a correlation between age and paying back on time?
	Findings:
	Young Adults and Teenagers have the highest percentage of defaulting on debts. This indicates that borrowers with relatively young ages tend to underestimate their ability and the risks involved in borrowing.
6. How does the loan purpose affect the automatic rate?
	Findings:
	- The loan purposes 'Car' and 'Education' have the highest percentage of likelihood for defaulting on payments.
	- This is because a car is an asset with continuously decreasing value, so when a borrower fails to repay, they still incur a loss when selling the car to cover the debt.
	- Regarding Education, it usually takes time for borrowers to be able to repay the borrowed money, especially if they do not successfully complete their education.




# General Conclusion

**for Data Processing, I did these steps:**

1. Standardizing values: If there are inconsistent values (varying in magnitude), standardization is necessary.

2. Removing minus signs (-) with the assumption that borrowers made input errors.

3. Handling missing values by performing replacements.

4. Checking statistical data (mean, median) in columns before replacement to avoid outliers.

5. Removing duplicate data.

  
**To decide whether to grant a loan or not, it is important to consider the following factors that affect the likelihood of default:**

- Days Employed: The fewer days employed, the higher the likelihood of defaulting on payments.

- Total Income: Higher income correlates with a higher likelihood of defaulting on payments.

- Age: Late teenagers and early adults have a higher likelihood of defaulting.

- Family Status: Borrowers with the status 'unmarried' and 'civil partnership' have a higher likelihood of defaulting.

- Loan purpose for cars and education shows a higher likelihood of defaulting.

 
**Additional questions to further enhance the accuracy of the loan decision-making process:**

- Loan tenure (tenor)

- Loan amount borrowed.
