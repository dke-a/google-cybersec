# Filter Dates and Numbers in SQL

## Data Types in Databases

In databases, there are three common data types you'll encounter:

1. **String Data**: An ordered sequence of characters, including numbers, letters, or symbols. For example, usernames like `analyst10`.
2. **Numeric Data**: Consists of numbers, allowing mathematical operations such as multiplication or addition.
3. **Date and Time Data**: Represents a date and/or time.

## Filtering by Numbers and Dates

Previously, we applied filters using string data. Now, we will work with numeric and date/time data, which is common in cybersecurity tasks.

### Common Operators

For numeric or date/time data, the following operators are commonly used:

- `=` : Equals
- `>` : Greater than
- `<` : Less than
- `!=` : Not equal to
- `>=` : Greater than or equal to
- `<=` : Less than or equal to

### Example: Filtering Login Attempts After 6 PM

To find login attempts made after 6 PM, indicating potentially suspicious activity:

```
SELECT * 
FROM log_in_attempts 
WHERE login_time > '18:00';
```

This query selects all columns from the `log_in_attempts` table where the `login_time` is later than `18:00` (6 PM).

### Example: Filtering Patches Within a Date Range

To find all patches installed between March 1, 2021, and September 1, 2021, use the `BETWEEN` operator:

```
sql
Copy code
SELECT * 
FROM machines 
WHERE OS_patch_date BETWEEN '2021-03-01' AND '2021-09-01';
```

This query selects all records from the `machines` table where the `OS_patch_date` falls within the specified range.

### Important Note on Filtering

- **Strings, Dates, and Times**: Use quotation marks to specify the values you're filtering for.
- **Numbers**: Do not use quotation marks.

### Key Takeaways

- Filtering with SQL allows for precise data retrieval using conditions on various data types.
- Use appropriate operators (`=`, `>`, `<`, `!=`, `>=`, `<=`) for numeric and date/time data.
- Use the `BETWEEN` operator to filter results within a range.
- Enclose strings, dates, and times in quotation marks, but not numbers.