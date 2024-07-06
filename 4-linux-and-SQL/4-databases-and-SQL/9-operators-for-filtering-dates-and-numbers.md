# Operators for Filtering Dates and Numbers in SQL

## Importance of Numeric and Date/Time Data in Cybersecurity

Security analysts frequently work with more than just string data. They often handle:

- Numeric Data

  : Includes data types like numbers, such as:

  - Number of login attempts
  - Count of a specific type of log entry
  - Volume of data being sent from a source or to a destination

- Date and Time Data

  : Represents date and/or time, crucial for tasks like:

  - Timestamps on log records
  - Login dates and times
  - Dates for patches
  - Duration of a connection

## Comparison Operators in SQL

When filtering numeric and date/time data, SQL provides several comparison operators that can be used in the `WHERE` clause of a query. These operators include:

| Operator | Use                        |
| -------- | -------------------------- |
| `<`      | Less than                  |
| `>`      | Greater than               |
| `=`      | Equal to                   |
| `<=`     | Less than or equal to      |
| `>=`     | Greater than or equal to   |
| `<>`     | Not equal to               |
| `!=`     | Not equal to (alternative) |

### Example: Filtering by Birthdate

```
SELECT firstname, lastname, birthdate
FROM employees
WHERE birthdate > '1970-01-01';
```

This query returns employees born after January 1, 1970. Using `>` excludes January 1, 1970. If you use `>=`, it includes January 1, 1970.

### Inclusive vs. Exclusive Operators

- **Exclusive Operators**: Do not include the value of comparison (`<`, `>`).
- **Inclusive Operators**: Include the value of comparison (`<=`, `>=`).

## The BETWEEN Operator

The `BETWEEN` operator is used to filter for values within a specified range and is inclusive of the endpoints.

### Example: Filtering by Hire Date

```
SELECT firstname, lastname, hiredate
FROM employees
WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';
```

This query returns employees hired between January 1, 2002, and January 1, 2003, inclusive of these dates.

## Key Takeaways

- Operators

   are essential for filtering numeric and date/time data in SQL.

  - **Exclusive Operators** (`<`, `>`) do not include the comparison value.
  - **Inclusive Operators** (`<=`, `>=`, `BETWEEN`) include the comparison value.

- The `BETWEEN` operator is useful for filtering within a range and is inclusive of the start and end values.