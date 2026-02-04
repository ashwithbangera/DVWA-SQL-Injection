DVWA SQL Injection Exploitation using SQLMap

📌 Project Overview

This project demonstrates the practical exploitation of a SQL Injection vulnerability using SQLMap on a deliberately vulnerable web application called Damn Vulnerable Web Application (DVWA).
The objective is to understand how improper input validation can allow attackers to access sensitive database information.

🎯 Aim

To identify and exploit a SQL Injection vulnerability in DVWA and extract sensitive information from the backend database using automated tools.

🖥️ Environment Details

Operating System: Kali Linux

Target Application: DVWA (Damn Vulnerable Web Application)

Web Server: Apache

Database: MariaDB (MySQL compatible)

Security Level: Low

🛠️ Tools Used

DVWA – Vulnerable web application for practice

SQLMap – Automated SQL Injection exploitation tool

Web Browser Developer Tools – Cookie capture (PHPSESSID)

Apache & MariaDB – Backend services

⚠️ Vulnerability Description

SQL Injection occurs when user input is directly included in SQL queries without proper validation or sanitization.
In DVWA, the id parameter in the SQL Injection module is vulnerable, allowing attackers to manipulate database queries.

🧪 Methodology
1. DVWA Setup

DVWA installed and configured on Kali Linux

Database connection established

Logged in using default credentials

Security level set to Low

2. Session Cookie Capture

Captured authenticated session cookies:

PHPSESSID

security=low

3. Database Enumeration

SQLMap used to identify available databases

4. Data Extraction

Extracted usernames and password hashes from the users table of the DVWA database

💥 Results

SQL Injection vulnerability successfully exploited

Databases enumerated using SQLMap

Sensitive user credentials extracted

Demonstrated real-world impact of insecure database queries

📊 Impact Analysis

Confidentiality: Leakage of usernames and password hashes

Integrity: Potential modification or deletion of data

Authentication Risk: Possible admin account compromise

Overall Risk: High, if deployed in a real-world application

🛡️ Remediation & Prevention

Use Prepared Statements (Parameterized Queries)

Validate and sanitize all user inputs

Apply least privilege to database users

Disable detailed error messages

Use a Web Application Firewall (WAF)

⚖️ Legal Disclaimer

This project was performed strictly for educational purposes on a deliberately vulnerable application in a controlled environment.
Unauthorized testing on real-world systems without permission is illegal.

📚 Learning Outcome

Gained hands-on experience with SQL Injection

Learned how automated tools exploit web vulnerabilities

Understood the importance of secure coding practices
