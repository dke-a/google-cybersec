# Types of Joins

## Introduction
In SQL, joins are used to combine rows from two or more tables based on a related column. While INNER JOIN returns only the rows with matching values in both tables, outer joins are used when you need to return all entries from one or both of the tables, regardless of whether there is a match.

## Types of Joins
There are three types of outer joins:
- **LEFT JOIN**
- **RIGHT JOIN**
- **FULL OUTER JOIN**

### LEFT JOIN
- **Description**: Returns all the records from the first (left) table and the matched records from the second (right) table. The result is NULL from the right side if there is no match.
- **Example**:
    ```sql
    SELECT employees.employee_id, employees.username, machines.device_id
    FROM employees
    LEFT JOIN machines
    ON employees.employee_id = machines.employee_id;
    ```
- **Explanation**: This query returns all rows from the `employees` table and only the matched rows from the `machines` table. If there's no match, the result for `machines.device_id` will be NULL.

### RIGHT JOIN
- **Description**: Returns all the records from the second (right) table and the matched records from the first (left) table. The result is NULL from the left side if there is no match.
- **Example**:
    ```sql
    SELECT employees.employee_id, employees.username, machines.device_id
    FROM employees
    RIGHT JOIN machines
    ON employees.employee_id = machines.employee_id;
    ```
- **Explanation**: This query returns all rows from the `machines` table and only the matched rows from the `employees` table. If there's no match, the result for `employees.employee_id` and `employees.username` will be NULL.

### FULL OUTER JOIN
- **Description**: Returns all records when there is a match in either left or right table records. If there is no match, the result is NULL on the side where there is no match.
- **Example**:
    ```sql
    SELECT employees.employee_id, employees.username, machines.device_id
    FROM employees
    FULL OUTER JOIN machines
    ON employees.employee_id = machines.employee_id;
    ```
- **Explanation**: This query returns all rows from both tables. If there is no match, the result will be NULL in the columns from the table that doesn't have the matching row.

## Practical Use Cases
As a security analyst, you might need to use these joins in various scenarios:
- **LEFT JOIN**: To find all employees and their assigned machines, including employees without machines.
- **RIGHT JOIN**: To find all machines and their assigned users, including machines without users.
- **FULL OUTER JOIN**: To get a comprehensive list of all employees and machines, including those without matches.

## Key Takeaways
- **LEFT JOIN**: Returns all rows from the left table and matched rows from the right table.
- **RIGHT JOIN**: Returns all rows from the right table and matched rows from the left table.
- **FULL OUTER JOIN**: Returns all rows when there is a match in either table; NULL where there is no match.
- **Syntax**: Similar to INNER JOIN, but with the keywords LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN.

Understanding these types of joins will help you efficiently query and combine data from multiple tables, which is crucial for comprehensive data analysis and security investigations.