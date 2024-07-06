# Apply More Filters in SQL

## Activity Overview
As a security analyst, you’ll often need to query numbers and dates. For example, you may need to filter patch dates to find machines that need an update. Or you might filter login attempts made during a certain period of time to investigate a security incident.

Common operators for working with numeric or date and time data will help you accurately filter data. These are some of the operators you'll use:

- `=` (equal)
- `>` (greater than)
- `<` (less than)
- `<>` (not equal to)
- `>=` (greater than or equal to)
- `<=` (less than or equal to)

In this lab activity, you’ll apply these operators to accurately filter for specific numbers and dates.

## Scenario
You’re investigating a recent security incident. You need to gather information about login attempts for certain dates and times to help in resolving a security incident.

The information you need is located in the `log_in_attempts` table in the `organization` database.

## Tasks
1. Retrieve login attempts made after a certain date.
2. Narrow the focus of the search to filter logins in a date range.
3. Investigate logins made at certain times.
4. Filter login attempts based on their event IDs.

### Task 1: Retrieve Login Attempts After a Certain Date
To investigate a recent security incident, you need to gather information about login attempts made after '2022-05-09'.

```sql
SELECT * 
FROM log_in_attempts 
WHERE login_date > '2022-05-09';
```

**How many login attempts were made after 2022-05-09?**

- Answer: 125

To include 2022-05-09 in your search:

```
sql
Copy code
SELECT * 
FROM log_in_attempts 
WHERE login_date >= '2022-05-09';
```

**How many login attempts were made on or after 2022-05-09?**

- Answer: 165

### Task 2: Retrieve Logins in a Date Range

Filter login attempts made between '2022-05-09' and '2022-05-11':

```
sql
Copy code
SELECT * 
FROM log_in_attempts 
WHERE login_date BETWEEN '2022-05-09' AND '2022-05-11';
```

**How many login attempts were made between 2022-05-09 and 2022-05-11?**

- Answer: 123

### Task 3: Investigate Logins at Certain Times

Filter data in the `log_in_attempts` table by login time (login_time). Retrieve all login attempts made before '07:00:00':

```
sql
Copy code
SELECT * 
FROM log_in_attempts 
WHERE login_time < '07:00:00';
```

**What is the username of the fifth record returned from this query?**

- Answer: eraab

Modify the query to return logins between '06:00:00' and '07:00:00':

```
sql
Copy code
SELECT * 
FROM log_in_attempts 
WHERE login_time BETWEEN '06:00:00' AND '07:00:00';
```

**What time was the earliest login attempt between 06:00:00 and 07:00:00?**

- Answer: 06:01:31

### Task 4: Investigate Logins by Event ID

Return only the `event_id`, `username`, and `login_date` fields from the `log_in_attempts` table. Retrieve login attempts with `event_id` greater than or equal to 100:

```
sql
Copy code
SELECT event_id, username, login_date 
FROM log_in_attempts 
WHERE event_id >= 100;
```

**What is the login date of the third result returned by your query?**

- Answer: 2022-05-09

Modify the query to return only login attempts with `event_id` between 100 and 150:

```
sql
Copy code
SELECT event_id, username, login_date 
FROM log_in_attempts 
WHERE event_id BETWEEN 100 AND 150;
```

**What is the username of the seventh result returned by your query?**

- Answer: tmitchel