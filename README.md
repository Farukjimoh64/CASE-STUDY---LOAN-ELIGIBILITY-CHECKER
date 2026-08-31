# CASE-STUDY---LOAN-ELIGIBILITY-CHECKER
This is an introduction of a simple automated loan pre-screening system that manually checks loan eligibility check. It collects customer information, calculate the customer's debt-to-income ratio, calculate a sample monthly repayment, check the customer's eligibility against predefined rules (that are fictitious)
What Problem Are We Solving?

Imagine a bank receiving hundreds of loan applications.

Before a loan officer sends an application for further review, the
institution needs to answer a few basic questions:

Is the applicant old enough?

Does the applicant earn enough?

Is the requested amount within the permitted limit?

Is the applicant's existing debt manageable?

Is the credit score acceptable?

Does the applicant already have an active loan?

Is the applicant employed?

Is the requested repayment period valid?

Doing these checks manually for every applicant can be repetitive.

Our solution is a simple automated pre-screening system.

The Loan Eligibility Checker takes customer information, applies the
project's predefined rules, performs the necessary calculations, and
produces a clear eligibility decision.

In simple terms:

Customer information → Check the rules → Calculate financial
indicators → Make a decision → Generate a report

The project brief explicitly describes the system as an educational
prototype rather than a real lending or financial decision system.

Industry Scenario

In the fictional scenario, we have joined the Digital Banking Team
of a fictional financial institution as Junior Python Developers.

The institution currently performs basic loan screening manually. The
team has therefore been asked to create a Python program capable of
performing the initial checks automatically.

The system is expected to:

Collect customer information.

Validate the information provided.

Calculate the customer's Debt-to-Income Ratio (DTI).

Check eligibility against predefined rules.

Determine the customer's loan/credit category where applicable.

Calculate a sample monthly repayment.

Generate a clear loan eligibility report.

The rules are fictional and exist specifically for programming practice.

How the System Thinks

The program does not "understand" a customer in the human sense.

Instead, it follows clearly defined rules.

For example:

Is age between 18 and 65?
        ↓
Is monthly income at least ₦150,000?
        ↓
Is requested loan greater than ₦0 and ≤ ₦5,000,000?
        ↓
Is credit score at least 650?
        ↓
Is DTI ≤ 40%?
        ↓
Does the customer have NO existing loan?
        ↓
Is the employment status acceptable?
        ↓
Is the loan term 6, 12 or 24 months?
        ↓
       YES
        ↓
     ELIGIBLE

If a required condition fails, the final eligibility result becomes
Not Eligible.

This is a practical example of converting a real-world business policy
into programmable logic.

Eligibility Rules

The project uses the following fictional rules.

1. Age Requirement

The customer must be:

18 years or older
AND
65 years or younger

So the valid range is:

18 ≤ Age ≤ 65

2. Minimum Monthly Income

The applicant's monthly income must be at least:

₦150,000

Therefore:

Income ≥ ₦150,000

3. Employment Status

The project recognises three possible employment categories:

Employed

Self-Employed

Unemployed

However, the eligibility rule requires the applicant not to be
Unemployed to proceed.

Therefore:

Employed       → Can proceed
Self-Employed  → Can proceed
Unemployed     → Not eligible

4. Credit Score

Credit scores are classified as:

        Score Category

     **750+** Excellent
 **650--749** Good
 **550--649** Fair
**Below 550** Poor

For overall eligibility, the minimum required credit score is:

650

This means an applicant may have a score categorised as Good or
Excellent and satisfy the credit-score requirement.

5. Existing Loan

The project assumes that a customer with an existing loan is not
eligible for a new loan.

Existing Loan = False → Pass
Existing Loan = True  → Fail

For reporting:

False → Existing Loan: None
True  → Existing Loan: Active

6. Requested Loan Amount

The requested loan must satisfy both conditions:

Loan Amount > ₦0
AND
Loan Amount ≤ ₦5,000,000

Therefore, zero, negative values and amounts above ₦5 million are
invalid.

7. Debt-to-Income Ratio (DTI)

The project calculates DTI using:

DTI = (Existing Monthly Debt / Monthly Income) × 100

The maximum permitted DTI is:

40%

Example

For the sample customer:

Existing Monthly Debt = ₦70,000
Monthly Income        = ₦350,000

DTI = (70,000 / 350,000) × 100
    = 20%

Since:

20% ≤ 40%

the customer passes the DTI requirement.

8. Loan Term

Only these repayment periods are accepted:

6 months

12 months

24 months

Any other value should be flagged as:

Invalid Loan Term

Initial Test Customer

The project provides a fictional customer record for the initial test.

Customer Information    Value

Customer Name           Daniel Okafor
Customer ID             CUST001
Age                     35
Monthly Income          ₦350,000
Existing Monthly Debt   ₦70,000
Requested Loan Amount   ₦1,000,000
Loan Term               12 months
Credit Score            720
Existing Loan           False
Employment Status       Employed

Expected financial interpretation

Credit Score

720 → Good

DTI

₦70,000 / ₦350,000 × 100 = 20%

Estimated monthly payment

₦1,000,000 / 12 = ₦83,333.33

The sample customer satisfies all the fictional eligibility conditions
and is therefore expected to be:

Loan Eligibility: Eligible

Project Tasks

The project combines the concepts taught throughout the relevant Python
lessons.

Task 1 --- Customer Variables

Create meaningful variables for:

Customer name

Customer ID

Age

Monthly income

Existing monthly debt

Requested loan amount

Loan term

Credit score

Existing loan status

Employment status

Task 2 --- Customer Information Validation

Validate whether:

Customer name is provided.

Customer ID is provided.

Age is valid.

Monthly income is valid.

Loan amount is valid.

The results should be stored as Boolean values and displayed.

Task 3 --- Age Validation

Use comparison operators to determine whether:

Age >= 18
AND
Age <= 65

Task 4 --- Income Validation

Check whether:

Monthly Income >= ₦150,000

Display either:

Income Requirement: Passed

or:

Income Requirement: Failed

Task 5 --- Loan Amount Validation

Check:

Loan Amount > ₦0
AND
Loan Amount <= ₦5,000,000

Task 6 --- Credit Score Categorisation

Use:

if
elif
else

to classify the customer's credit score as:

Excellent
Good
Fair
Poor

Task 7 --- DTI Calculation

Use the project's DTI formula:

Existing Monthly Debt / Monthly Income × 100

Then determine whether the result is within the maximum 40%
requirement.

Task 8 --- Employment Validation

Classify the applicant as:

Employed
Self-Employed
Unemployed

The project considers an unemployed applicant ineligible.

Task 9 --- Existing Loan Check

Determine whether the customer has an existing loan.

False → None
True  → Active

An active existing loan makes the applicant ineligible under the
project's fictional rules.

Task 10 --- Loan Term Validation

Accept only:

6, 12, 24

Any other value is invalid.

Reusable Functions

One of the key goals of the project is to move beyond writing everything
as one continuous sequence of code.

check_loan_eligibility()

This function is designed to receive relevant customer information
through parameters, including:

Age

Monthly income

DTI

Credit score

Existing loan status

Employment status

Loan amount

Loan term

It should evaluate the rules and return the appropriate eligibility
result.

Conceptually:

Customer data
     ↓
check_loan_eligibility()
     ↓
All required conditions?
     ↓
True / False

calculate_dti()

This function receives:

Monthly Income
Existing Monthly Debt

and returns the calculated DTI.

Conceptually:

def calculate_dti(monthly_income, existing_monthly_debt):
    # calculate DTI
    # return result

The benefit is reuse: the same calculation can be applied to every
applicant.

calculate_monthly_payment()

This function receives:

Loan amount

Loan term

and returns the estimated monthly payment.

The project's simplified formula is:

Monthly Payment = Loan Amount / Loan Term

For example:

₦1,000,000 / 12
= ₦83,333.33

Important limitation

This is deliberately a simplified educational calculation.

It does not include:

Interest

Fees

Taxes

Insurance

Penalties

Real lending conditions

Amortisation

Therefore, it must not be interpreted as a real bank repayment
quotation.

Processing Multiple Applicants

The project introduces four fictional loan applications and asks the
program to process them using a for loop.

Applicant 1 --- Daniel Okafor

Age:                  35
Monthly Income:       ₦350,000
Existing Debt:        ₦70,000
Loan Amount:          ₦1,000,000
Loan Term:            12 months
Credit Score:         720
Existing Loan:        False
Employment:           Employed

Applicant 2 --- Grace Bello

Age:                  42
Monthly Income:       ₦500,000
Existing Debt:        ₦100,000
Loan Amount:          ₦2,000,000
Loan Term:            24 months
Credit Score:         780
Existing Loan:        False
Employment:           Employed

Applicant 3 --- Samuel Ade

Age:                  27
Monthly Income:       ₦120,000
Existing Debt:        ₦20,000
Loan Amount:          ₦500,000
Loan Term:            12 months
Credit Score:         700
Existing Loan:        False
Employment:           Employed

Applicant 4 --- Anita James

Age:                  50
Monthly Income:       ₦400,000
Existing Debt:        ₦200,000
Loan Amount:          ₦1,500,000
Loan Term:            12 months
Credit Score:         680
Existing Loan:        True
Employment:           Employed

For every applicant, the system should determine:

Age validity

Income eligibility

Credit category

DTI

Employment status

Existing loan status

Loan amount validity

Loan term validity

Overall eligibility

Estimated monthly payment

Bonus Challenge --- Portfolio-Level Insights

After processing all four applicants, the project asks the system to
answer:

How many applicants are eligible?

How many are not eligible?

Who has the highest credit score?

Who has the highest monthly income?

Who has the highest DTI?

Who has the lowest DTI?

Who failed the income requirement?

Who failed because of an existing loan?

Who requested the highest loan amount?

What is the estimated monthly payment for each eligible applicant?

This transforms the program from merely checking one person into a small
loan application analysis tool.

While Loop: Validating Income

The project also requires a while loop that repeatedly asks for
monthly income until the user enters a valid value.

For example:

Enter monthly income: 0

Monthly income must be greater than ₦0.

Enter monthly income: 350000

Income accepted.

The important programming idea is:

Do not allow the process to continue until the required input is
valid.

Controlled Infinite Loop

The project introduces:

while True:

to demonstrate an infinite loop with a controlled exit.

The program should ask:

Do you want to check another loan application?

If the user enters:

yes

the program continues.

If the user enters:

no

the program uses:

break

to stop the loop.

This demonstrates that an infinite loop does not necessarily mean a
program is permanently trapped. A deliberate exit condition can control
it.

Understanding Variable Scope

The project introduces the difference between global and local
variables.

A global variable is defined as:

institution_name = "SmartBank"

This variable exists outside a function and can be accessible according
to Python's global-scope rules.

Inside a function, the project asks for a local variable such as:

def generate_report():
    report_title = "Loan Eligibility Report"

report_title belongs to the function's local scope.

This exercise demonstrates an important programming principle:

Where a variable is created affects where it can be accessed.

Final Loan Eligibility Report

The final output is expected to be neat and structured.

A report should communicate:

========================================
LOAN ELIGIBILITY REPORT
========================================

Customer Name: Daniel Okafor
Customer ID: CUST001
Age: 35
Monthly Income: ₦350,000
Existing Monthly Debt: ₦70,000
Credit Score: 720
Credit Category: Good
Loan Amount: ₦1,000,000
Loan Term: 12 Months
Existing Loan: False
Employment Status: Employed

----------------------------------------
ELIGIBILITY CHECKS
----------------------------------------

Age Requirement: Passed
Income Requirement: Passed
Loan Amount: Passed
Credit Score Requirement: Passed
Debt-to-Income Requirement: Passed
Existing Loan Requirement: Passed
Employment Requirement: Passed
Loan Term Requirement: Passed

Debt-to-Income Ratio: 20%

----------------------------------------
LOAN CALCULATION
----------------------------------------

Requested Loan: ₦1,000,000
Loan Term: 12 Months
Estimated Monthly Payment: ₦83,333.33

----------------------------------------
FINAL RESULT
----------------------------------------

Loan Eligibility: Eligible

========================================

The objective is not merely to make the output work, but to make it
readable, organised and understandable.

System Architecture

The complete project can be understood as a sequence of six stages:

┌─────────────────────────────┐
│  1. COLLECT CUSTOMER DATA   │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│  2. VALIDATE INPUTS         │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│  3. CALCULATE DTI & PAYMENT │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│  4. APPLY ELIGIBILITY RULES │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│  5. PROCESS APPLICATIONS    │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│  6. GENERATE FINAL REPORT   │
└─────────────────────────────┘

This structure demonstrates how individual Python concepts can work
together to solve one coherent problem.

Python Concepts Demonstrated

This project deliberately brings together the concepts covered in the
study programme.

Operators

Used for calculations and comparisons.

Examples:

+
-
/
*
>=
<=
==

Conditional Statements

Used to make decisions:

if
elif
else

Logical Operators

Used to combine requirements:

and
or

for Loops

Used to process multiple fictional loan applications.

while Loops

Used to repeatedly request valid information.

Infinite while Loops

Used with:

while True:

and controlled using:

break

Functions

Used to package reusable logic.

Parameters and Arguments

Used to pass customer information into functions.

Return Values

Used by functions such as DTI and monthly payment calculations to send
results back to the calling code.

Variable Scope

Used to demonstrate the difference between global and local variables.

Boolean Values

Used to represent pass/fail conditions and eligibility states.

Project Boundaries

The project rules specifically restrict the implementation to concepts
covered in the relevant semester.

Required concepts

Operators

if

elif

else

for loops

while loops

Infinite while loops

Functions

Parameters

Arguments

Return values

Variable scope

Also permitted

Variables

Data types

Boolean values

Arithmetic calculations

Not permitted for this exercise

Classes

File handling

Exception handling

External Python libraries

Advanced Python concepts not taught in the Study Group

These restrictions are intentional: the objective is to demonstrate
understanding of the taught Python fundamentals rather than to build an
unnecessarily complex application.

Why This Project Is More Than an if Statement

At first glance, a loan checker may look like a simple collection of
conditions.

It is actually a useful demonstration of problem decomposition.

A real-world requirement such as:

"Determine whether this customer qualifies for a loan."

is too broad to code effectively as one thought.

We break it into smaller questions:

What information do we need?
        ↓
How do we validate it?
        ↓
What calculations are required?
        ↓
What rules determine eligibility?
        ↓
How do we process more than one applicant?
        ↓
How do we repeat input when it is invalid?
        ↓
How do functions make the code reusable?
        ↓
How do we communicate the final result?

That is the real programming lesson behind the project.

Expected Analysis of the Four Applicants

Using the rules supplied in the project brief:

Applicant          Income           DTI        Credit Existing   Expected
Loan       Eligibility

Daniel           ₦350,000           20%  720 --- Good No         Eligible
Okafor

Grace Bello      ₦500,000           20%       780 --- No         Eligible
Excellent

Samuel Ade       ₦120,000        16.67%  700 --- Good No         Not
Eligible ---
income below
minimum

What this demonstrates

Daniel satisfies the requirements.

Grace satisfies the requirements and has the highest credit score
and monthly income among the four.

Samuel has an acceptable DTI and credit score, but fails because his
monthly income is below ₦150,000.

Anita fails two major eligibility conditions: her DTI is 50%, which
exceeds the 40% maximum, and she already has an existing loan.

Estimated Monthly Payments

Using the project's simplified formula:

Monthly Payment = Loan Amount / Loan Term

Applicant               Loan        Term   Estimated Monthly Payment

Daniel Okafor     ₦1,000,000   12 months                  ₦83,333.33
Grace Bello       ₦2,000,000   24 months                  ₦83,333.33
Samuel Ade          ₦500,000   12 months                  ₦41,666.67
Anita James       ₦1,500,000   12 months                 ₦125,000.00

These are mathematical estimates under the project's simplified formula,
not real lending quotations.

Key Project Insights

From the four supplied applications:

2 applicants are eligible.

2 applicants are not eligible.

Grace Bello has the highest credit score: 780.

Grace Bello has the highest monthly income: ₦500,000.

Anita James has the highest DTI: 50%.

Samuel Ade has the lowest DTI: 16.67%.

Samuel Ade fails the income requirement.

Anita James fails because of an existing loan.

Grace Bello requests the highest loan amount: ₦2,000,000.

The eligible applicants are Daniel Okafor and Grace Bello.

Testing Strategy

A strong implementation should not only test the happy path.

The logic should be tested against different situations.

Scenario 1 --- Fully eligible applicant

All conditions pass.

Expected:

Eligible

Scenario 2 --- Income below ₦150,000

Income fails.

Expected:

Not Eligible

Scenario 3 --- Credit score below 650

Credit requirement fails.

Expected:

Not Eligible

Scenario 4 --- DTI above 40%

Debt burden is too high.

Expected:

Not Eligible

Scenario 5 --- Existing loan is active

Existing-loan requirement fails.

Expected:

Not Eligible

Scenario 6 --- Invalid loan term

For example:

18 months

Expected:

Invalid Loan Term

Scenario 7 --- Invalid income entry

For example:

₦0

The program should continue requesting income until a value greater than
₦0 is supplied.

Learning Outcomes

Completing this project demonstrates that the developer can:

Translate a written business problem into programming rules.

Store information using meaningful variables.

Perform financial calculations with arithmetic operators.

Compare values using comparison operators.

Combine multiple conditions with logical operators.

Use conditional statements for decision-making.

Use loops to repeat operations.

Use functions to organise reusable logic.

Pass information through parameters and arguments.

Return calculated results.

Understand variable scope.

Present a computational result in a human-readable format.

The project therefore represents a transition from learning individual
Python statements to using those statements together to solve a
structured problem.

Possible Future Improvements

Although the current exercise intentionally stays within the taught
Python concepts, a future version could evolve into a more sophisticated
application.

Possible improvements include:

1. Better input validation

Prevent invalid data from reaching calculations.

2. Detailed rejection reasons

Instead of returning only:

Not Eligible

the system could explain:

Not Eligible

Reasons:
- Monthly income is below ₦150,000.
- Debt-to-income ratio exceeds 40%.

3. More flexible applicant processing

Instead of manually defining applicants, the program could collect and
process new applicants dynamically.

4. More realistic repayment calculations

A future financial model could incorporate interest and amortisation.

5. Data storage

A production-oriented system could store applications for later review.

6. User interface

The logic could eventually be connected to a graphical or web interface.
