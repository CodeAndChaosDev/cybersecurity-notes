# SQL Injection Attacks 

## Introduction: 
This content explains how websites and applications work with databases using SQL queries. It focuses on how attackers exploit weaknesses in these queries through SQL injection. 

## Key Points: 
1. Interaction with Databases: 

• Applications use SQL queries to store, modify, and retrieve data from databases. 

• An example of a login page asks for a username and password, creating an SQL query to check the credentials. 

2. Example SQL Query: 

• When a user enters credentials (e. g. , Username: John, Password: Un@detectable444), the application constructs a SQL query: 
``` 
SELECT FROM users WHERE username = 'John' AND password = 'Un@detectable444'; 
``` 
• The database checks if both conditions are met to return user details. 

3. SQL Injection Vulnerability: 

• If input is not properly validated, attackers can input malicious SQL code. 

• SQL injection can compromise critical data stored in databases. 

4. Injection Example: 

• An attacker can exploit a vulnerability by entering: 

• Username: John 

• Password: abc' OR 1=1;-- - 

• The resulting SQL query becomes: 

``` 
SELECT FROM users WHERE username = 'John' AND password = 'abc' OR 1=1;-- -'; 
``` 
• The condition OR 1=1 always evaluates to true, allowing unauthorized access. 

5. Importance of Input Validation: 

• Proper input validation and sanitization can prevent SQL injection attacks. 

• The attacker uses a single quote after "abc" to manipulate the query structure successfully. 

## Conclusion: 
SQL injection is a serious security risk that can allow unauthorized access to sensitive information. Understanding how SQL queries function and the impact of improper input validation is crucial for securing applications against these types of attacks. Always ensure to obtain permission before testing for SQL vulnerabilities.

# Try Hack Me

- Q: Which flag in the SQLMap tool is used to extract all the databases available?

- A: --dbs

- Q: What would be the full command of SQLMap for extracting all tables from the "members" database? (Vulnerable URL: http://sqlmaptesting.thm/search/cat=1)
- A: sqlmap -u http://sqlmaptesting.thm/search/cat=1 -D members --tables

- Q: What is the name of the table available in the "ai" database?

- A: user

- C: sqlmap -u 'http://10.10.181.98/ai/includes/user_login?email=test&password=test'  --tables --level=5


- Q: What is the password of the email test@chatai.com?

- A: 12345678

- C: sqlmap -u 'http://10.10.181.98/ai/includes/user_login?email=test&password=test'  --tables --level=5 -D ai -T user --dump
