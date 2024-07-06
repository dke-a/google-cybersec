# More on Filters with AND, OR, and NOT

## Logical Operators
Logical operators like AND, OR, and NOT help you refine your SQL queries to return specific information. These operators are crucial for filtering data based on multiple conditions.

### AND Operator
The AND operator is used to filter records based on two conditions that must be met simultaneously.

#### Example
To find customer accounts handled by a support representative with an ID of 5 and located in the USA:
```sql
SELECT firstname, lastname, email, country, supportrepid
FROM customers
WHERE supportrepid = 5 AND country = 'USA';
```

- **Explanation**: This query returns customers who meet both conditions: having a support representative ID of 5 and being located in the USA.

### OR Operator

The OR operator connects two conditions and specifies that either condition can be met.

#### Example

To find customers located in either the USA or Canada:

```
sql
Copy code
SELECT firstname, lastname, email, country
FROM customers
WHERE country = 'Canada' OR country = 'USA';
```

- **Explanation**: This query returns all customers located in either the USA or Canada.

### NOT Operator

The NOT operator negates a condition, returning all records that do not match the specified condition.

#### Example

To find customers who are not located in the USA:

```
sql
Copy code
SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'USA';
```

- **Explanation**: This query returns all customers who are not located in the USA.

#### Pro Tip

You can also use the <> or != operators to find values that are not equal to a certain value:

```
sql
Copy code
WHERE country <> 'USA'
WHERE country != 'USA'
```

## Combining Logical Operators

Logical operators can be combined to create more complex filters.

#### Example

To find customers who are not located in either the USA or Canada:

```
sql
Copy code
SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'Canada' AND NOT country = 'USA';
```

- **Explanation**: This query returns customers who are not located in either the USA or Canada.

## Key Takeaways

- **AND**: Requires both conditions to be true simultaneously.
- **OR**: Requires either one or both conditions to be true.
- **NOT**: Negates a condition, returning records that do not match the condition.
- Logical operators can be combined to create specific filters that target the security-related information you need.

By using these logical operators, you can create more precise SQL queries to find the exact data you need for your security analysis tasks.