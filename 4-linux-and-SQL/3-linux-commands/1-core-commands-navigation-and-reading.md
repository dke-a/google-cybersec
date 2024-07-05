# Core Commands for Navigation and Reading Files

## Introduction

Navigating and reading files in the Linux file system is a crucial skill for cybersecurity professionals. This section will cover the foundational commands needed to navigate the Linux file system using the Bash shell.

## The Linux File System

- **Filesystem Hierarchy Standard (FHS)**: Organizes data in the Linux OS. Everything in Linux is considered a file, and the FHS is a hierarchical system where everything branches out from the root directory.
- **Root Directory**: The highest-level directory in Linux, designated by a single slash (`/`). Subdirectories branch off from the root directory.

### Directory Structure Example

- ```
  /
  ```

   (Root Directory)

  - ```
    /home
    ```

     (Subdirectory)

    - `/home/analyst` (Subdirectory within home)

## Core Navigation Commands

- **pwd**: Prints the working directory. Displays the current directory you are in.
- **ls**: Lists the names of files and directories in the current working directory.
- **cd**: Changes directories. Use this command to navigate between directories.

### Example Commands

1. **pwd**:
   - Command: `pwd`
   - Output: Displays the path to the current working directory, e.g., `/home/analyst`.
2. **ls**:
   - Command: `ls`
   - Output: Lists files and directories in the current working directory, e.g., `logs`, `oldreports`, `projects`, `reports`, and `updates.txt`.
3. **cd**:
   - Command: `cd logs`
   - Output: No direct output, but changes the current directory to `logs`. Use `pwd` to confirm.

## Reading File Content

Security analysts often need to read files to check for configuration settings, user access reports, and potential vulnerabilities.

### Commands to Read Files

- **cat**: Displays the full content of a file.
- **head**: Displays the beginning of a file. By default, it shows the first ten lines.

### Example Commands

1. **cat**:
   - Command: `cat access.txt`
   - Output: Displays the entire content of the file `access.txt`.
2. **head**:
   - Command: `head access.txt`
   - Output: Displays the first ten lines of the file `access.txt`.

## Key Takeaways

- **pwd**: Use to print the current working directory.
- **ls**: Use to list files and directories in the current directory.
- **cd**: Use to change directories.
- **cat**: Use to display the full content of a file.
- **head**: Use to display the first ten lines of a file.

Understanding and using these core commands will enable you to navigate and manage files in the Linux operating system efficiently, which is essential for any security analyst.