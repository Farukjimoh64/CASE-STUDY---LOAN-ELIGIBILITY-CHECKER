# CASE-STUDY: LOAN-ELIGIBILITY CHECKER
 
## Project Overview
The SmartBank Loan Eligibility Checker is a Python-based educational project designed to simulate a simple automated loan pre-screening system.
The program evaluates fictional loan applications using predefined eligibility criteria such as:
•	Customer age
•	Monthly income
•	Employment status
•	Credit score
•	Existing loan status
•	Requested loan amount
•	Loan term
•	Debt-to-Income (DTI) ratio
The system processes customer information, validates loan requirements, calculates estimated monthly repayments, and generates a structured loan eligibility report.
 This project is an educational prototype. It does not represent a real financial lending or credit decision system.
 
## Project Objectives
This project demonstrates practical application of fundamental Python programming concepts, including:
•	Variables and data types
•	Arithmetic operators
•	Comparison operators
•	Logical operators
•	if, elif, and else statements
•	for loops
•	while loops
•	Infinite loops
•	Functions
•	Parameters and arguments
•	Return values
•	Global and local variable scope
 
## Loan Eligibility Requirements
A customer is considered eligible only when all the following conditions are satisfied:
* Requirement	Condition
* Age	Between 18 and 65 years
* Monthly Income	At least ₦150,000
* Credit Score	At least 650
* Debt-to-Income Ratio	40% or below
* Existing Loan	Must not have an active loan
* Employment Status	Employed or Self-Employed
* Loan Amount	Greater than ₦0 and not more than ₦5,000,000
* Loan Term	6, 12, or 24 months
 
## Debt-to-Income Calculation
The Debt-to-Income ratio is calculated using the following formula:
``` Debt-to-Income Ratio =
Existing Monthly Debt / Monthly Income × 100
```
Example
``` ₦70,000 / ₦350,000 × 100 = 20%
```
The customer must have a DTI ratio of 40% or below to satisfy the requirement.
 
## Credit Score Categories
#### Credit Score	Category
```
750 and above	Excellent
650 – 749	Good
550 – 649	Fair
Below 550	Poor
```
The minimum required credit score for eligibility is 650.
 
## Features
* The Loan Eligibility Checker can:
* Validate customer information
* Validate age requirements
* Check monthly income eligibility
* Validate loan amounts
* Categorize credit scores
* Calculate Debt-to-Income ratios
* Check employment status
* Detect existing loans
* Validate loan terms
* Calculate estimated monthly repayments
* Determine overall loan eligibility
* Process multiple loan applications
* Generate structured eligibility reports
* Demonstrate user input validation using a while loop
* Demonstrate a controlled infinite loop using while True
 
 ## Functions Used
```
calculate_dti()
Calculates and returns the customer's Debt-to-Income ratio.
```
```
get_credit_category()
Determines the customer's credit score category.
```
```
check_loan_eligibility()
Evaluates all loan requirements and returns the customer's overall eligibility result.
```
```
calculate_monthly_payment()
Calculates the estimated monthly repayment using:
Monthly Payment = Loan Amount / Loan Term
```
```
generate_report()
Generates a detailed and structured loan eligibility report.
``` 
 ## Sample Applications
The program processes four fictional loan applications:
1.	Daniel Okafor
2.	Grace Bello
3.	Samuel Ade
4.	Anita James
Each applicant is evaluated against the same eligibility requirements.
 
 ## Bonus Analysis
After processing all applications, the program identifies:
•	Number of eligible applicants
•	Number of non-eligible applicants
•	Applicant with the highest credit score
•	Applicant with the highest monthly income
•	Applicant with the highest DTI ratio
•	Applicant with the lowest DTI ratio
•	Applicants who failed the income requirement
•	Applicants with existing loans
•	Applicant with the highest requested loan amount
 
 ## Example Output
========================================
Eligibility Report
SmartBank
========================================
Customer Name: Daniel Okafor
Customer ID: CUST001
Age: 35
Monthly Income: ₦350,000.00
Existing Monthly Debt: ₦70,000.00
Credit Score: 720
Credit Category: Good
Loan Amount: ₦1,000,000.00
Loan Term: 12 Months

----------------------------------------
Eligibility Checks
----------------------------------------

Age Requirement: Passed
Income Requirement: Passed
Loan Amount: Passed
Credit Score Requirement: Passed
Debt-to-Income Requirement: Passed
Existing Loan Requirement: Passed
Employment Requirement: Passed
Loan Term Requirement: Passed

Debt-to-Income Ratio: 20.00%

-----------------------------------------
Loan Calculation
-----------------------------------------

Estimated Monthly Payment: ₦83,333.33

-----------------------------------------
Final Result
-----------------------------------------

Loan Eligibility: Eligible
=========================================
 
 ## How to Run the Project
1. Clone the Repository
git clone https://github.com/YOUR-GITHUB-USERNAME/loan-eligibility-checker.git
2. Navigate into the Project Folder
cd loan-eligibility-checker
3. Run the Program
python loan_eligibility_checker.py
 
 ## Technologies Used
•	Python
No external libraries were used in this project.
 
 ## Key Learning Outcomes
Through this project, I strengthened my understanding of how to transform a real-world scenario into a structured programming solution.
Some key lessons include:
•	Breaking large problems into smaller functions
•	Using logical operators to combine multiple conditions
•	Writing reusable functions
•	Processing multiple records with loops
•	Validating user input
•	Understanding global and local variable scope
•	Creating structured and readable program output
This project helped me move beyond learning individual Python concepts and begin combining them to solve practical problems.
 
 ## Future Improvements
Possible future improvements include:
•	Adding more customer records
•	Creating a graphical user interface
•	Saving loan applications to a database
•	Adding interest rate calculations
•	Creating a web-based version
•	Adding advanced input validation
•	Building an administrative dashboard
 
 ## Acknowledgements
Special appreciation to Coach Timothy for the guidance and practical Python learning experience that inspired this project.
Recognition is also given to SmartBizCrux for supporting practical learning and skill development.
 
 ## Author
### JIMOH FARUK
**Aspiring Python Developer | Business Professional | Agribusiness Entrepreneur**
I am passionate about continuous learning and applying technology to solve practical business and real-world problems.
⭐ If you found this project interesting, feel free to star the repository!
