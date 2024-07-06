# Introduction to Databases

## Overview
Our modern world is filled with data, guiding us in making important decisions. When dealing with large amounts of data, we need to know how to store it so that it is organized and quick to access and process. The solution to this is through databases.

## What is a Database?
- **Definition**: An organized collection of information or data.
- **Comparison with Spreadsheets**:
  - **Spreadsheets**: Suitable for single users or small teams, less data storage, e.g., Google Sheets.
  - **Databases**: Accessed by multiple people simultaneously, store massive amounts of data, perform complex tasks.

## Importance of Databases for Security Analysts
- Access databases containing information on login attempts, software and updates, machines, and their owners.

## Structure and Organization of Databases
- Databases allow storing large amounts of data while keeping it quick and easy to access.
- **Relational Databases**:
  - Structured databases containing tables that are related to each other.
  
## Relational Database Components
- **Tables**: Individual components of a larger database containing fields of information.
  - **Fields (Columns)**: e.g., `employee_id`, `device_id`, `username`.
  - **Rows (Records)**: Specific data related to the columns, e.g., employee details.

### Example of a Table
| employee_id | device_id | username | department |
| ----------- | --------- | -------- | ---------- |
| 1000        | D100      | jdoe     | marketing  |
| 1001        | D101      | asmith   | sales      |

## Relationships Between Tables
- **Common Columns**: Tables can be connected if they share a common column, known as keys.

### Types of Keys
1. **Primary Key**:
   - A column where every row has a unique entry.
   - Must not have any duplicate values or null values.
   - Uniquely identifies every row in the table.
   - Example: `employee_id` in the employees table.

2. **Foreign Key**:
   - A column in a table that is a primary key in another table.
   - Can have empty values and duplicates.
   - Connects two tables together.
   - Example: `employee_id` in the machines table (primary key in the employees table).

### Example of a Relationship Between Tables
- **Employees Table**:
  | employee_id | username | department |
  | ----------- | -------- | ---------- |
  | 1000        | jdoe     | marketing  |
  | 1001        | asmith   | sales      |

- **Machines Table**:
  | machine_id | employee_id | device_id |
  | ---------- | ----------- | --------- |
  | M001       | 1000        | D100      |
  | M002       | 1001        | D101      |

- **Relationship**:
  - The `employee_id` column in both tables establishes the relationship.
  - `employee_id` is a primary key in the employees table and a foreign key in the machines table.

## Summary
- A table can only have one primary key but can have multiple foreign keys.
- Understanding the structure and organization of relational databases is crucial for effective data management.

## Next Steps
- Move on to the basics of SQL, the language that lets us work with databases.
- Gain hands-on experience working with these concepts.

---

Feel free to explore more detailed examples and exercises to reinforce these concepts!
