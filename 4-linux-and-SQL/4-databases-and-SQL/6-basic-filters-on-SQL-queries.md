# Basic Filters on SQL Queries

## Introduction
One of the most powerful features of SQL is its ability to filter data. Filtering allows you to select specific pieces of data from a database that match certain conditions, making your queries more precise and relevant.

## Understanding Filtering
Filtering is the process of selecting data that meets a specific condition. For example, as a security analyst, you might filter a `log_in_attempts` table to find all attempts from a specific country. This could be done by applying a filter on the `country` column to return only records containing "Canada."

## SQL Operators
An operator is a symbol or keyword that represents an operation. An example of an operator is the equal to (`=`) operator. For example, if you want to find all records that have "USA" in the `country` column, you would use:
```sql
country = 'USA'
```

To filter a query in SQL, you add an extra line to the `SELECT` and `FROM` statement using a `WHERE` clause. The `WHERE` clause indicates the condition for the filter. For example, to find all login attempts made in the United States, you would create this filter:

```

SELECT *
FROM log_in_attempts
WHERE country = 'USA';
```

This query returns all records where the `country` column is equal to "USA."

## Using Patterns with Filters

You can make conditions more complex by searching for patterns instead of exact values. For example, in the `employees` table, you could search for records in the `office` column that match a certain pattern. To search for a pattern, use the percentage sign (`%`) as a wildcard for unspecified characters. For example:

```sql
office LIKE 'East%'
```

This would return all records that start with "East" such as "East-120," "East-290," and "East-435."

When searching for patterns, use the `LIKE` operator instead of the equal (`=`) operator. For example:

```sql
SELECT *
FROM log_in_attempts
WHERE country LIKE 'US%';
```

This query returns all entries where the `country` column starts with "US," including both "US" and "USA."

## Practical Examples

### Example 1: Basic Filter

```sql
SELECT *
FROM log_in_attempts
WHERE country = 'USA';
```

This query selects all columns from the `log_in_attempts` table where the `country` is "USA."

### Example 2: Pattern Matching

Imagine your database has inconsistencies with how the United States is represented, with some entries using "US" and others using "USA." You can use the `LIKE` operator to filter for both patterns:

```sql
SELECT *
FROM log_in_attempts
WHERE country LIKE 'US%';
```

This query returns all entries where the `country` column begins with "US," covering both "US" and "USA."

## Key Takeaways

- **Filtering**: Selecting data that matches a certain condition using the `WHERE` clause.
- **Operators**: Symbols or keywords that represent an operation (e.g., `=`, `LIKE`).
- **Pattern Matching**: Using the `LIKE` operator with wildcards (`%`) to search for patterns in data.