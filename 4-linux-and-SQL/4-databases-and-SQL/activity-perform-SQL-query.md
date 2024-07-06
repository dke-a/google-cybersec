# Activity: Perform a SQL Query

## Activity Overview
Previously, you learned how to use basic SQL queries to retrieve information from a database. You have also learned about using the `ORDER BY` keyword to sort data returned in an ascending or a descending order.

In this lab activity, you’ll use `SELECT` and `FROM` in SQL to return the information you need from a database. You’ll also use the `ORDER BY` keyword to sequence the information returned by a query based on a specified column.

It's important to know how to query information from a database because this is a common task you might encounter as a security analyst. You should know how to get the information you need to improve security and keep data safe.

## Scenario
In this scenario, you have to determine which employee devices must be updated. You also need to investigate user login activity to explore if any unusual activity has occurred.

The information you need is located in the `machines` and `login_attempts` tables in the `organization` database.

Here’s how you’ll do this task: First, you’ll obtain information on the employee devices that must be updated. Next, you’ll examine the login attempts for unusual activity. Finally, you’ll use the `ORDER BY` keyword to sort the data returned by your SQL queries.

OK, let’s get ready to practice running your very first SQL queries!

Note: In this lab you’ll be working with the `organization` database and the tables it contains. The lab starts with the `organization` database in the MariaDB shell that is already open. This means you can start with the tasks as soon as you click the Start Lab button.

If you unintentionally exit the `organization` database in the MariaDB shell, you can reconnect by running the `sudo mysql organization` command.

## Task 1: Retrieve Employee Device Data
In this task, you need to obtain information on employee devices because your team needs to update them. The information you need is in the `machines` table in the `organization` database.

First, you need to retrieve all the information about the employee devices.

Run the following query to select all device information from the `machines` table:
```sql
SELECT *
FROM machines;
```

The output returns all the contents of the `machines` table:

```
yaml
Copy code
+--------------+------------------+----------------+---------------+-------------+
| device_id    | operating_system | email_client   | OS_patch_date | employee_id |
+--------------+------------------+----------------+---------------+-------------+
| a184b775c707 | OS 1             | Email Client 1 | 2021-09-01    |        1156 |
| a192b174c940 | OS 2             | Email Client 1 | 2021-06-01    |        1052 |
| a305b818c708 | OS 3             | Email Client 2 | 2021-06-01    |        1182 |
| a317b635c465 | OS 1             | Email Client 2 | 2021-03-01    |        1130 |
| a320b137c219 | OS 2             | Email Client 2 | 2021-03-01    |        1000 |
| ...          | ...              | ...            | ...           | ...         |
+--------------+------------------+----------------+---------------+-------------+
200 rows in set (0.356 sec)
```

Next, you want to focus on the email client running on various devices.

Run the following query to select only the `device_id` and `email_client` columns from the `machines` table:

```
SELECT device_id, email_client
FROM machines;
```

### Question:

**What email client is returned in the third row?**

-  Email Client 3
-  Email Client 4
-  Email Client 1
-  Email Client 2

Now, you need information on the operating systems used on various devices and their last patch date.

Complete the query to return only the `device_id`, `operating_system`, and `OS_patch_date` columns from the `machines` table:

```
sql
Copy code
SELECT device_id, operating_system, OS_patch_date
FROM machines;
```

### Question:

**What is the patch date of the first entry?**

-  2021-06-01
-  2021-09-01
-  2021-03-01
-  2021-12-01

Click `Check my progress` to verify that you have completed this task correctly.

You have completed this task and retrieved the needed information from the `machines` table.

## Task 2: Investigate Login Activity

In this task, you need to analyze the information from the `login_attempts` table to determine if any unusual activity has occurred.

First, you need to investigate the locations where login attempts were made to ensure that they’re in expected areas (the United States, Canada, or Mexico).

Write a SQL query to select the `event_id` and `country` columns from the `login_attempts` table:

```
sql
Copy code
SELECT event_id, country
FROM login_attempts;
```

### Question:

**Were any login attempts made from Australia?**

-  No
-  Yes

Next, you need to check if login attempts were made outside of the organization's working hours.

Write a SQL query that selects the `username`, `login_date`, and `login_time` columns from the `login_attempts` table:

```
sql
Copy code
SELECT username, login_date, login_time
FROM login_attempts;
```

### Question:

**What username is returned in the fifth row?**

-  mrah
-  dkot
-  apatel
-  jrafael

Now, you need to get a complete picture of all login attempts.

Write a SQL query that selects all columns from the `login_attempts` table, using a single symbol after the `SELECT` keyword:

```
sql
Copy code
SELECT *
FROM login_attempts;
```

Click `Check my progress` to verify that you have completed this task correctly.

You have completed this task and retrieved the needed information from the `login_attempts` table.

## Task 3: Order Login Attempts Data

In this task, you need to use the `ORDER BY` keyword. You'll sequence the data that your query returns according to the login date and time.

First, you need to sort the information by date.

Run the following query, which orders `login_attempts` data by `login_date`:

```
sql
Copy code
SELECT *
FROM login_attempts
ORDER BY login_date;
```

### Question:

**What are the username and login date of the first record returned?**

-  mabadi on 2022-05-10
-  sbaelish on 2022-05-10
-  daquino on 2022-05-08
-  ivelasco on 2022-05-08

Now, you need to further organize the previous results by ordering them by `login_time`.

Modify the query from the previous step by adding the login time to the `ORDER BY` clause:

```
sql
Copy code
SELECT * 
FROM login_attempts
ORDER BY login_date, login_time;
```

### Question:

**What are the username and login time of the first record returned by the above query?**

-  gesparza at 00:40:00
-  bsand at 00:19:11
-  pwashing at 00:36:12
-  wjaffrey at 00:15:55

Click `Check my progress` to verify that you have completed this task correctly.

You have completed this task and used the `ORDER BY` keyword to sort the data returned from the `login_attempts` table.

## Conclusion

Great work!

You have completed this activity, and you now have practical experience in running basic SQL queries to:

- select specific columns from a table,
- select all columns from a table by using an asterisk (*), and
- sort query results using the `ORDER BY` keyword.

These basic queries form the foundation for running more advanced queries and applying filters later.