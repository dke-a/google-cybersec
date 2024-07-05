# Create and Modify Directories and Files

## Directory and File Management Commands

### Creating and Removing Directories

- `mkdir` (Make Directory):

   Creates a new directory.

  - Example: `mkdir drafts` creates a directory named "drafts".

- `rmdir` (Remove Directory):

   Removes an empty directory. If the directory is not empty, it will not be deleted, providing a built-in warning.

  - Example: `rmdir oldreports` removes the directory named "oldreports".

### Creating and Removing Files

- `touch`:

   Creates a new empty file.

  - Example: `touch email_patches.txt` creates a file named "email_patches.txt".

- `rm` (Remove):

   Deletes a file.

  - Example: `rm email_patches.txt` removes the file named "email_patches.txt".

### Moving and Copying Files and Directories

- `mv` (Move):

   Moves a file or directory to a new location. It can also be used to rename files or directories.

  - Example: `mv email_policy.txt drafts/` moves the file "email_policy.txt" to the "drafts" directory.

- `cp` (Copy):

   Copies a file or directory to a new location.

  - Example: `cp vulnerabilities.txt projects/` copies the file "vulnerabilities.txt" to the "projects" directory.

## Practical Examples

### Initial Setup

1. **Print Working Directory:**
   - Command: `pwd`
   - This command prints the current working directory.
2. **List Directory Contents:**
   - Command: `ls`
   - This command lists the files and directories in the current working directory.

### Directory Management

1. **Remove an Old Directory:**
   - Command: `rmdir oldreports`
   - Removes the directory named "oldreports".
2. **Create a New Directory:**
   - Command: `mkdir drafts`
   - Creates a new directory named "drafts".
3. **Change to New Directory:**
   - Command: `cd drafts`
   - Changes the current directory to "drafts".

### File Management

1. **Create New Files:**
   - Command: `touch email_patches.txt OS_patches.txt`
   - Creates two files named "email_patches.txt" and "OS_patches.txt".
2. **Remove a File:**
   - Command: `rm email_patches.txt`
   - Removes the file named "email_patches.txt".

### Moving and Copying Files

1. **Move a File:**
   - Command: `mv reports/email_policy.txt drafts/`
   - Moves "email_policy.txt" from "reports" to "drafts".
2. **Copy a File:**
   - Command: `cp vulnerabilities.txt projects/`
   - Copies "vulnerabilities.txt" to the "projects" directory.

## Editing Files with Nano

- Nano:

   A beginner-friendly text editor accessed through the 

  ```
  nano
  ```

   command.

  - Example: 

    ```
    nano OS_patches.txt
    ```

    - Opens the file "OS_patches.txt" in the nano editor.
    - To save changes, press `Ctrl + O`, then press `Enter`.
    - To exit nano, press `Ctrl + X`.

## Summary

By mastering these commands, you can efficiently manage directories and files in Linux. This skill is crucial for organizing data, detecting issues, and ensuring information security. Keep practicing these commands to become proficient in Linux file and directory management.