# Basic SQL Queries

## Introduction
In this section, we'll learn to run basic SQL queries, a fundamental skill for security analysts. These queries will help determine specific information from a database, such as which computer has been assigned to a certain employee.

## Key SQL Keywords
### SELECT
- **Purpose**: Specifies the columns to return in the query result.
- **Syntax**: 
  ```sql
  SELECT column1, column2

### FROM

- **Purpose**: Specifies the table to query.

- Syntax:

  ```sql
  FROM table_name
  ```

### Example Query

To retrieve information about employee IDs and their assigned device IDs, you can use the following query:

```sql
SELECT employee_id, device_id 
FROM employees;
```

### Explanation

- **Keywords**: `SELECT` and `FROM` are SQL keywords. They can be written in uppercase or lowercase, but uppercase is often used for readability.
- **Columns**: `employee_id` and `device_id` are the columns to be returned.
- **Table**: `employees` is the table being queried.
- Syntax Rules
  - Columns are separated by commas.
  - Keywords are not case-sensitive.
  - A semicolon (`;`) is placed at the end of the statement to signify the end of the query.

### Running the Query

- **Output**: The query will return a list of employee IDs and their corresponding device IDs.

## Select All Columns

If you want to retrieve all columns from a table, you can use the asterisk (`*`), which is referred to as "select all."

### Example Query

To get all columns from the `employees` table, you can use the following query:

```sql
SELECT * 
FROM employees;
```

### Explanation

- **Asterisk (`\*`)**: Used to select all columns from the table.
- **Output**: The query will return all the columns and rows from the `employees` table.

## Summary

- **SELECT**: Specifies which columns to return.
- **FROM**: Specifies which table to query.
- **SELECT \* FROM table_name**: Returns all columns from the specified table.