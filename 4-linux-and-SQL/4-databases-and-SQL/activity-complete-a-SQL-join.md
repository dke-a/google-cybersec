# Complete a SQL Join

## Activity Overview
As a security analyst, you often need data from more than one table. SQL joins enable you to combine tables with shared columns, which is helpful when connecting information from different tables. In this lab activity, you will use SQL joins to connect separate tables and retrieve the needed information.

### Scenario
You are investigating a recent security incident that compromised some machines. You are responsible for retrieving the required information from the database for the investigation.

Tasks:
1. Use an inner join to identify which employees are using which machines.
2. Use left and right joins to find machines that do not belong to any specific user and users who do not have any specific machine assigned to them.
3. Use an inner join to list all login attempts made by all employees.

### Note
In this lab, you will work with the organization database and the tables it contains. The lab starts with the organization database in the MariaDB shell that is already open. 

## Task 1: Match Employees to Their Machines
Identify which employees are using which machines by performing an inner join between the `machines` and `employees` tables on the `device_id` column.

### SQL Query
```sql
SELECT * 
FROM machines 
INNER JOIN employees ON machines.device_id = employees.device_id;
```

### Answer

The inner join query returned **185** rows.

## Task 2: Return More Data

### Part 1: Left Join

Connect the `machines` and `employees` tables through a left join.

### SQL Query

```
SELECT * 
FROM machines 
LEFT JOIN employees ON machines.device_id = employees.device_id;
```

### Answer

The value in the `username` column for the last record returned is **NULL**.

### Part 2: Right Join

Connect the `machines` and `employees` tables through a right join.

### SQL Query

```
SELECT * 
FROM machines 
RIGHT JOIN employees ON machines.device_id = employees.device_id;
```

### Answer

The value in the `username` column for the last record returned is **areyes**.

## Task 3: Retrieve Login Attempt Data

Retrieve information on all employees who have made login attempts by performing an inner join on the `employees` and `log_in_attempts` tables, linking them on the common `username` column.

### SQL Query

```
SELECT * 
FROM employees 
INNER JOIN log_in_attempts ON employees.username = log_in_attempts.username;
```

### Answer

There are **200** records returned by the inner join.