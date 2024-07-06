# Filter with AND, OR, and NOT

## Activity Overview
As a security analyst, you’ll often need to analyze data. Finding the specific data you need depends on multiple factors. To retrieve specific pieces of information from a database, you can filter for multiple conditions or filter for what does not match a particular condition.

In this lab activity, you’ll use the AND, OR, and NOT operators to create more complex filters for SQL queries.

### Scenario
You need to obtain specific information about employees, their machines, and the departments they belong to from the database to investigate potential security issues and update computers.

You are responsible for filtering the required information from the database.

Tasks:
1. Retrieve all failed login attempts after business hours.
2. Retrieve all login attempts that occurred on specific dates.
3. Retrieve logins that didn't originate in Mexico.
4. Retrieve information about certain employees in the Marketing department.
5. Retrieve information about employees in the Finance or Sales department.
6. Obtain information about employees who are not in the Information Technology department.

## Task 1: Retrieve After Hours Failed Login Attempts
Retrieve all failed login attempts that occurred after 18:00.

### Query
```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;
```

### Question

How many failed login attempts occurred after 18:00?

**Answer:** 19

## Task 2: Retrieve Login Attempts on Specific Dates

Retrieve all login attempts that occurred on '2022-05-09' and '2022-05-08'.

### Query

```
sql
Copy code
SELECT * 
FROM log_in_attempts 
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```

### Question

How many login attempts were made on these two days?

**Answer:** 75

## Task 3: Retrieve Login Attempts Outside of Mexico

Retrieve login attempts that did not originate in Mexico ('MEX' and 'MEXICO').

### Query

```
sql
Copy code
SELECT * 
FROM log_in_attempts 
WHERE NOT country LIKE 'MEX%';
```

### Question

How many login attempts were made outside of Mexico?

**Answer:** 144

## Task 4: Retrieve Employees in Marketing

Retrieve information about employees in the 'Marketing' department located in the East building.

### Query

```
sql
Copy code
SELECT * 
FROM employees 
WHERE department = 'Marketing' AND office LIKE 'East%';
```

### Question

What is the username of the first employee in the Marketing department in the East building?

**Answer:** elarson

## Task 5: Retrieve Employees in Finance or Sales

Retrieve records for employees in the 'Finance' or the 'Sales' department.

### Query

```
sql
Copy code
SELECT * 
FROM employees 
WHERE department = 'Finance' OR department = 'Sales';
```

### Question

What is the username of the first employee in the Sales department?

**Answer:** lrodriqu

## Task 6: Retrieve All Employees Not in IT

Retrieve records for employees who are not in the 'Information Technology' department.

### Query

```
sql
Copy code
SELECT * 
FROM employees 
WHERE NOT department = 'Information Technology';
```

### Question

How many employees are not in the Information Technology department?

**Answer:** 161

## Conclusion

You now have practical experience in using SQL to:

- Run SQL queries to retrieve information from a database.
- Apply AND, OR, and NOT operators to filter SQL queries. You’re well on your way to running complex SQL queries to get specific data from a database.