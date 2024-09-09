##The College-Managment app has a login bypass vulnerability through SQL injection 

## Affected version: 
College-Management System - 1.0

## Software:

https://code-projects.org/college-management-system-in-php-with-source-code/

## Vulnerability File:
College-Management-System/login/login.php

## Description:

Improper error handling in the College Management application allows for a login bypass through SQL injection. This vulnerability arises because the application does not adequately manage or sanitize error messages, which can be exploited to manipulate SQL queries and gain unauthorized access.

POC

### Attempting the payload ' ADMIN OR 1=1-- reveals that the application is using MariaDB.

![image](https://github.com/user-attachments/assets/1f1018da-26a2-4b2e-9ea5-a1a1ecf350d4)

------------------------------------------------------------------------------------------------
### The following payload leads to a login bypass ' or ''='

![image](https://github.com/user-attachments/assets/f5bab159-b291-49c7-b98f-c044cbb5632f)

----------------------------------------------------------------------------------------------
### Logged in as admin

![image](https://github.com/user-attachments/assets/b0e4b018-9045-4130-a5de-00d04f807ac5)


