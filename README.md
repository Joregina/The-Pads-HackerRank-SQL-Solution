# 📘 SQL Challenge – Formatting Names with Occupation Initials
This repository contains my solution to a classic SQL problem that requires formatting names from a database and appending the first letter of their occupation in parentheses.

## 🧩 Problem Statement
Query an alphabetically ordered list of all names in the OCCUPATIONS table, immediately followed by the first letter of each profession enclosed in parentheses.

## 🗂 Table Structure
The OCCUPATIONS table has the following columns:
| Column         | Type    |
|----------------|---------|
| Name   | String  |
| Occupation       | String  |

## 🛠️ Solution Breakdown
I solved this problem by breaking it down into manageable steps:

**1. Sort names alphabetically**

<pre>SELECT Name 
FROM OCCUPATIONS 
ORDER BY Name ASC;</pre>

**2. Extract the first letter of the occupation**

<pre>SELECT SUBSTRING(Occupation, 1, 1) 
FROM OCCUPATIONS;</pre>

**3. Wrap the first letter in parentheses**

<pre>SELECT CONCAT('(', SUBSTRING(Occupation, 1, 1), ')') 
FROM OCCUPATIONS;</pre>

**4. Combine name and formatted occupation**

<pre>SELECT CONCAT(Name, CONCAT('(', SUBSTRING(Occupation, 1, 1), ')')) 
FROM OCCUPATIONS 
ORDER BY Name ASC;</pre>







🧠 Key SQL Functions Used
CONCAT() – To merge strings
SUBSTRING() – To extract a portion of the occupation string
ORDER BY – To alphabetize the results

✅ Final Output
