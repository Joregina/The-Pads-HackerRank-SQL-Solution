# 📘 SQL Challenge – Formatting Names with Occupation Initials
This repository contains my solution to a classic SQL problem that requires formatting names from a database and appending the first letter of their occupation in parentheses.

## 🧩 Problem Statement
Query an alphabetically ordered list of all names in the OCCUPATIONS table, immediately followed by the first letter of each profession enclosed in parentheses.

## 🗂 Table Structure
The OCCUPATIONS table has the following columns:
Name – The name of the person
Occupation – The person's job title (Doctor, Professor, Singer, Actor)

## 🛠️ Solution Breakdown
I solved this problem by breaking it down into manageable steps:

**1. Sort names alphabetically**

SELECT Name 
FROM OCCUPATIONS 
ORDER BY Name ASC;

**2. Extract the first letter of the occupation**

SELECT SUBSTRING(Occupation, 1, 1) 
FROM OCCUPATIONS;

**3. Wrap the first letter in parentheses**

SELECT CONCAT('(', SUBSTRING(Occupation, 1, 1), ')') 
FROM OCCUPATIONS;

**4. Combine name and formatted occupation**

SELECT CONCAT(Name, CONCAT('(', SUBSTRING(Occupation, 1, 1), ')')) 
FROM OCCUPATIONS 
ORDER BY Name ASC;







🧠 Key SQL Functions Used
CONCAT() – To merge strings
SUBSTRING() – To extract a portion of the occupation string
ORDER BY – To alphabetize the results

✅ Final Output
