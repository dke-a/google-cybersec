# Join Tables in SQL

## Activity Overview
You've already learned a lot about SQL queries and filters. Now, let's introduce the concept of joining tables when querying a database. This is helpful when you need information from two different tables in a database. For example, combining tables that tell us about security vulnerabilities of different operating systems and machines in our company can give us a list of vulnerable machines.

## Syntax of Joins
When working with two tables, you need a way to tell SQL what table you're picking columns from. For example, if you have an `employee_id` column in both the `employees` table and the `machines` table, SQL needs to know which column you're referring to. To resolve this, write the name of the table first, followed by a period, and then the name of the column, like so: `employees.employee_id` and `machines.employee_id`.

## INNER JOIN
An INNER JOIN returns rows matching on a specified column that exists in more than one table. 

### Example
Imagine we want to understand the employees accessing the machines in our company by joining the `employees` and `machines` tables. We use the `employee_id` column to connect the two tables. The `employee_id` column is a primary key in the `employees` table and a foreign key in the `machines` table.

### SQL Query for INNER JOIN
To get a list of users and their office locations along with the operating systems they use on their machines:

```sql
SELECT username, office, operating_system
FROM employees
INNER JOIN machines
ON employees.employee_id = machines.employee_id;
```

### Breakdown of the Query

- **SELECT**: Specifies the columns to return: `username`, `office`, and `operating_system`.
- **FROM**: Indicates the `employees` table as the first (left) table.
- **INNER JOIN**: Tells SQL to perform an INNER JOIN with the `machines` table.
- **ON**: Specifies the column to base the join on: `employees.employee_id` and `machines.employee_id`.

### Example Output

This query returns:

- `username`, `office` from the `employees` table
- `operating_system` from the `machines` table
- Only those rows where there is a match on `employee_id` in both tables.

## Handling NULL Values

In SQL, NULL represents a missing value. For example, machines that are not assigned to any employee may have NULL values in the `employee_id` column. INNER JOIN will not include rows where there are NULL values in the join column.

## Key Takeaways

- **INNER JOIN**: Used to return rows with matching values in both tables.
- **Syntax**: Specify the columns to return, the tables to join, and the column to join on.
- **NULL Values**: Not included in INNER JOIN results if present in the join column.

## Practical Example

### Scenario

To investigate potential security issues and update computers, we need specific information about employees, their machines, and the departments they belong to. We can use INNER JOIN to combine relevant tables and retrieve the necessary data.

### SQL Query

Retrieve a list of users, their office locations, and the operating systems they use on their machines:

```sql
SELECT username, office, operating_system
FROM employees
INNER JOIN machines
ON employees.employee_id = machines.employee_id;
```

This query helps in identifying the employees and their machine details for further analysis or updates.