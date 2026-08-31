# CASE-STUDY---LOAN-ELIGIBILITY-CHECKER
This is an introduction of a simple automated loan pre-screening system that manually checks loan eligibility check. It collects customer information, calculate the customer's debt-to-income ratio, calculate a sample monthly repayment, check the customer's eligibility against predefined rules (that are fictitious)
A Python-based loan pre-screening prototype that evaluates a customer's financial and personal information against predefined eligibility rules. The project combines conditional statements, loops, functions, calculations, Boolean logic, parameters, return values, and variable scope to solve a practical Digital Banking scenario.

Note: This is an educational prototype using fictional rules and data. It is not a real lending or financial decision system.

## Project Overview

The system simulates the initial screening a financial institution might perform before sending a loan application for further review.

It can:

Collect and validate customer information

Categorise credit scores

Calculate Debt-to-Income Ratio (DTI)

Validate loan amount and repayment term

Check employment and existing-loan status

Determine overall loan eligibility

Estimate monthly repayment

Process multiple applicants using a for loop

Repeatedly request valid input using a while loop

Generate a structured eligibility report

## Process

Customer Information
        ↓
Input Validation
        ↓
Financial Calculations
        ↓
Eligibility Checks
        ↓
Final Decision
        ↓
Loan Eligibility Report

## Eligibility Rules

An applicant is eligible only when all required conditions are satisfied:

Requirement

Rule

### Age

18–65 years

### Monthly Income

At least ₦150,000

### Credit Score

At least 650

### DTI

40% or less

### Existing Loan

Must have no existing loan

### Employment

Must not be unemployed

### Loan Amount

Greater than ₦0 and up to ₦5,000,000

### Loan Term

6, 12, or 24 months

Credit Score Categories

Score

Category

750+

Excellent

650–749

Good

550–649

Fair

Below 550

Poor

DTI Formula

DTI = (Existing Monthly Debt / Monthly Income) × 100

Monthly Repayment Formula

For this exercise:

Monthly Payment = Loan Amount / Loan Term

Example:

₦1,000,000 / 12 = ₦83,333.33

The repayment formula is intentionally simplified and does not include interest, fees, taxes, or other real-world lending conditions.

## Core Functions

The project uses reusable functions for the main calculations and decision-making:

check_loan_eligibility()
calculate_dti()
calculate_monthly_payment()

These functions demonstrate how Python can separate calculations and business rules into reusable components.

## Multiple Applicant Processing

The project processes four fictional applications using a for loop:

Applicant

Income

DTI

Credit Score

Existing Loan

Daniel Okafor

₦350,000

20%

720

No

Grace Bello

₦500,000

20%

780

No

Samuel Ade

₦120,000

16.67%

700

No

Anita James

₦400,000

50%

680

Yes

## Based on the project rules:

Daniel Okafor: Eligible

Grace Bello: Eligible

Samuel Ade: Not Eligible — income below ₦150,000

Anita James: Not Eligible — DTI above 40% and existing loan

## Python Concepts Demonstrated

Variables and data types

Arithmetic and comparison operators

Boolean logic

if, elif, and else

for loops

while loops

while True and break

Functions

Parameters and arguments

Return values

Local and global variable scope

Structured program output

The project intentionally stays within the concepts required by the study brief and does not use classes, file handling, exception handling, external libraries, or untaught advanced Python concepts.

## Project Purpose

The goal is to demonstrate how fundamental Python concepts can be combined to translate a real-world business problem into a working logical solution.

### The development approach is:

Understand → Plan → Code → Test → Debug → Improve

## Team

Team D
Python Study Group — Gift II
Case Study Project #5: Loan Eligibility Checker

## Recognition: 
SmartBizCrux

## Junior Python Developer 
JIMOH FARUK
