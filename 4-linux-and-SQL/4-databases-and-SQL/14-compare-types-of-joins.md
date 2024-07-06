# Compare Types of Joins

## Inner Joins
- **Description**: INNER JOIN returns rows that have matching values in both tables.
- **Syntax**:
    ```sql
    SELECT *
    FROM employees
    INNER JOIN machines ON employees.device_id = machines.device_id;
    ```
    - **Explanation**: This query joins the `employees` and `machines` tables on the `device_id` column, returning rows where there is a match.
- **Example with Specific Columns**:
    ```sql
    SELECT username, operating_system, employees.device_id
    FROM employees
    INNER JOIN machines ON employees.device_id = machines.device_id;
    ```

## Outer Joins
Outer joins return all rows from one or both tables, regardless of whether there is a match.

### Left Joins
- **Description**: LEFT JOIN returns all records from the first (left) table, and the matched records from the second (right) table. If no match, the result is NULL from the right side.
- **Syntax**:
    ```sql
    SELECT *
    FROM employees
    LEFT JOIN machines ON employees.device_id = machines.device_id;
    ```
    - **Explanation**: This query returns all rows from `employees` and the matched rows from `machines`. If there is no match, NULL values are returned for columns from `machines`.

### Right Joins
- **Description**: RIGHT JOIN returns all records from the second (right) table, and the matched records from the first (left) table. If no match, the result is NULL from the left side.
- **Syntax**:
    ```sql
    SELECT *
    FROM employees
    RIGHT JOIN machines ON employees.device_id = machines.device_id;
    ```
    - **Explanation**: This query returns all rows from `machines` and the matched rows from `employees`. If there is no match, NULL values are returned for columns from `employees`.

### Full Outer Joins
- **Description**: FULL OUTER JOIN returns all records when there is a match in either left or right table records.
- **Syntax**:
    ```sql
    SELECT *
    FROM employees
    FULL OUTER JOIN machines ON employees.device_id = machines.device_id;
    ```
    - **Explanation**: This query returns all rows from both `employees` and `machines`. If there is no match, NULL values are returned for columns from the table that lacks the match.

## Key Takeaways
- **INNER JOIN**: Returns only the rows with matching values in both tables.
- **LEFT JOIN**: Returns all rows from the left table and matched rows from the right table.
- **RIGHT JOIN**: Returns all rows from the right table and matched rows from the left table.
- **FULL OUTER JOIN**: Returns all rows from both tables, with NULLs where there is no match.
- **Syntax**: Each type of join uses similar syntax but different keywords (INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN) to instruct SQL on how to combine the tables.

Understanding these types of joins will help you efficiently query and combine data from multiple tables, which is crucial for comprehensive data analysis and security investigations.