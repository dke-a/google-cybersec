# Activity: Find Files with Linux Commands

## Activity Overview

In this lab activity, you’ll navigate a Linux file structure, locate files, and read the contents of files using various Linux commands in the Bash shell. This is a practical scenario where you play the role of a security analyst investigating files in the `/home/analyst` directory.

## Scenario

As a security analyst, your tasks include:

1. Getting the information of the current working directory.
2. Navigating to the `reports` directory and listing its subdirectories.
3. Locating and reading the contents of a specific file in the `users` subdirectory.
4. Navigating to the `logs` directory and displaying the first 10 lines of a file.

## Task 1: Get the Current Directory Information

1. Display the current working directory

   :

   - Command: `pwd`
   - Output Example: `/home/analyst`

2. List the contents of the current working directory

   :

   - Command: `ls`
   - Output Example: `logs oldreports projects reports updates.txt`

### Questions:

- Current working directory

  :

  - Options:
    - `/home/analyst/logs`
    - `/home/analyst`
    - `/home`
    - `/var/logs`

- Number of directories in the current working directory

  :

  - Options:
    - Five
    - One
    - Four
    - Two

## Task 2: Change Directory and List the Subdirectories

1. Navigate to the `/home/analyst/reports` directory

   :

   - Command: `cd /home/analyst/reports`

2. List the files and subdirectories in the `reports` directory

   :

   - Command: `ls`
   - Output Example: `users`

### Questions:

- Name of the subdirectory in the `reports` directory

  :

  - Options:
    - logs
    - projects
    - users
    - analyst

## Task 3: Locate and Read the Contents of a File

1. Navigate to the `/home/analyst/reports/users` directory

   :

   - Command: `cd /home/analyst/reports/users`

2. List the files in the current directory

   :

   - Command: `ls`
   - Output Example: `Q1_added_users.txt`

3. Display the contents of the `Q1_added_users.txt` file

   :

   - Command: `cat Q1_added_users.txt`

   - Example Content:

     ```bash
     username  department          employee_id
     aezra     Human Resources     1104
     mreed     Information Technology 1177
     ```

### Questions:

- Department of the employee with the username `aezra`

  :

  - Options:
    - Human Resources
    - Finance
    - Information Technology
    - Sales

- Employee_id of the user `mreed` in the Information Technology department

  :

  - Options:
    - 1177
    - 1104
    - 1188
    - 1001

## Task 4: Navigate to a Directory and Locate a File

1. Navigate to the `/home/analyst/logs` directory

   :

   - Command: `cd /home/analyst/logs`

2. Display the name of the file it contains

   :

   - Command: `ls`
   - Output Example: `server_logs.txt`

3. Display the first 10 lines of the `server_logs.txt` file

   :

   - Command: `head server_logs.txt`

   - Example Content:

     ```bash
     [WARNING] 2023-06-01 Connection lost
     [INFO] 2023-06-01 Connection established
     [WARNING] 2023-06-01 High memory usage
     ```

### Questions:

- Number of warning messages in the first 10 lines of the `server_logs.txt` file

  :

  - Options:
    - Three
    - One
    - Six
    - Two

## Conclusion

In this activity, you have practiced:

- Navigating directory structures with the `cd` command.
- Displaying the current working directory with the `pwd` command.
- Listing the contents of a directory with the `ls` command.
- Displaying the contents of files with the `cat` and `head` commands.

These are fundamental skills for security analysts working with Linux systems.