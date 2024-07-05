# Manage Files with Linux Commands

## Activity Overview

In this lab activity, you’ll use Linux commands to modify a directory structure and the files it contains. You’ll also use the nano text editor to add text to a file.

As a security analyst, creating, removing, and editing directories and files are core tasks you’ll need to perform to help you manage data. When data is well organized, you can more easily detect issues and keep data safe.

## Scenario

You need to ensure that the `/home/analyst` directory is properly organized.

### Initial Directory Structure

home
└── analyst
    ├── notes
    │   ├── Q3patches.txt
    │   └── tempnotes.txt
    ├── reports
    │   ├── Q1patches.txt
    │   └── Q2patches.txt
    └── temp

### Target Directory Structure

home
└── analyst
    ├── logs
    ├── notes
    │   └── tasks.txt    
    └── reports
        ├── Q1patches.txt
        ├── Q2patches.txt
        └── Q3patches.txt

## Tasks

### Task 1: Create a New Directory

1. **Create a new subdirectory called `logs` in the `/home/analyst` directory.**

   ```
   bash
   Copy code
   mkdir /home/analyst/logs
   ```

2. **List the contents of the `/home/analyst` directory to confirm the creation of the new logs subdirectory.**

   ```
   bash
   Copy code
   ls /home/analyst
   ```

   Output should list: `logs notes reports temp`

### Task 2: Remove a Directory

1. **Remove the `/home/analyst/temp` directory.**

   ```
   bash
   Copy code
   rmdir /home/analyst/temp
   ```

2. **List the contents of the `/home/analyst` directory to confirm the removal.**

   ```
   bash
   Copy code
   ls /home/analyst
   ```

   Output should list: `logs notes reports`

### Task 3: Move a File

1. **Navigate to the `/home/analyst/notes` directory.**

   ```
   bash
   Copy code
   cd /home/analyst/notes
   ```

2. **Move the `Q3patches.txt` file to the `/home/analyst/reports` directory.**

   ```
   bash
   Copy code
   mv Q3patches.txt /home/analyst/reports/
   ```

3. **List the contents of the `/home/analyst/reports` directory to confirm the file move.**

   ```
   bash
   Copy code
   ls /home/analyst/reports
   ```

   Output should list: `Q1patches.txt Q2patches.txt Q3patches.txt`

### Task 4: Remove a File

1. **Remove the `tempnotes.txt` file from the `/home/analyst/notes` directory.**

   ```
   bash
   Copy code
   rm /home/analyst/notes/tempnotes.txt
   ```

2. **List the contents of the `/home/analyst/notes` directory to confirm the removal.**

   ```
   bash
   Copy code
   ls /home/analyst/notes
   ```

   No files should be listed.

### Task 5: Create a New File

1. **Create an empty file called `tasks.txt` in the `/home/analyst/notes` directory.**

   ```
   bash
   Copy code
   touch /home/analyst/notes/tasks.txt
   ```

2. **List the contents of the `/home/analyst/notes` directory to confirm the file creation.**

   ```
   bash
   Copy code
   ls /home/analyst/notes
   ```

   Output should list: `tasks.txt`

### Task 6: Edit a File

1. **Open the `tasks.txt` file in the nano text editor.**

   ```
   bash
   Copy code
   nano /home/analyst/notes/tasks.txt
   ```

2. **Copy and paste the following text into the text input area of nano:**

   ```
   arduino
   Copy code
   Completed tasks
   1. Managed file structure in /home/analyst
   ```

3. **Save the file and exit nano.**

   - Press `Ctrl+O`, then `Enter` to save.
   - Press `Ctrl+X` to exit.

4. **Clear the Bash shell window.**

   ```
   bash
   Copy code
   clear
   ```

5. **Display the contents of the `tasks.txt` file to confirm the update.**

   ```
   bash
   Copy code
   cat /home/analyst/notes/tasks.txt
   ```

   Output should display:

   ```
   arduino
   Copy code
   Completed tasks
   1. Managed file structure in /home/analyst
   ```

## Conclusion

You now have practical experience in using basic Linux Bash shell commands to:

- Create and remove directories.
- Copy, move, and remove files.
- Edit files with the nano text editor.

These skills are fundamental for managing directories and files in a Linux environment.