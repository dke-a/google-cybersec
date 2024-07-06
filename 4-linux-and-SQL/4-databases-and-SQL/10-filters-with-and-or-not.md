# Filters with AND, OR, and NOT

## Introduction

In SQL, filtering queries for multiple conditions is common in real security tasks. This reading explains how to use the AND, OR, and NOT operators to combine conditions in SQL queries. These operators help specify which rows to return based on multiple criteria.

## AND Operator

The AND operator specifies that both conditions must be met simultaneously. This is useful when looking for data that meets multiple criteria.

### Example

To find machines running Operating System 1 and using Email Client 1:

```
SELECT * 
FROM machines 
WHERE operating_system = 'OS 1' 
AND email_client = 'Email Client 1';
```

- **Explanation**: This query returns all machines that have both 'OS 1' as the operating system and 'Email Client 1' as the email client.

## OR Operator

The OR operator specifies that either condition can be met. This operator is useful when you need to find data that meets at least one of several conditions.

### Example

To find machines running either Operating System 1 or Operating System 3:

```
SELECT * 
FROM machines 
WHERE operating_system = 'OS 1' 
OR operating_system = 'OS 3';
```

- **Explanation**: This query returns all machines that have either 'OS 1' or 'OS 3' as the operating system.

## NOT Operator

The NOT operator negates a condition, returning all rows that do not meet the specified condition.

### Example

To find machines that are not using Operating System 3:

```
SELECT * 
FROM machines 
WHERE NOT operating_system = 'OS 3';
```

- **Explanation**: This query returns all machines that do not have 'OS 3' as the operating system.

## Combining Operators

You can combine these operators to create more complex queries that filter data based on multiple conditions.

### Example

To find machines that are either using Operating System 1 or 3 but not Email Client 2:

```
SELECT * 
FROM machines 
WHERE (operating_system = 'OS 1' OR operating_system = 'OS 3') 
AND NOT email_client = 'Email Client 2';
```

- **Explanation**: This query returns all machines that are running either 'OS 1' or 'OS 3' and are not using 'Email Client 2'.

## Key Takeaways

- **AND**: Both conditions must be met.
- **OR**: Either condition can be met.
- **NOT**: The condition must not be met.

Using these operators allows you to filter your data more precisely, making your SQL queries more powerful and efficient.