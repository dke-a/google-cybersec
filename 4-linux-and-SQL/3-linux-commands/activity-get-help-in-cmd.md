# Get Help in the Command Line

## Activity Overview

As a security analyst, you won't always have all the answers, but you can learn where to find them. Linux provides help directly through the command line, enabling you to get information on commands and how they work. This lab activity focuses on using `man`, `whatis`, and `apropos` commands to explore and understand various Linux commands.

## Scenario

In this scenario, you need to find more information about commands you need to use. You'll explore commands to learn about their functionality, find options to add to commands, get brief descriptions of commands, and identify the right command for specific tasks.

## Task 1: Learn More About Commands

### Step 1: Use `whatis` Command

Imagine you can't remember what the `cat` command does and want a quick reminder.

- **Command**: `whatis cat`

- Question

  : What are the first two words of the short description of 

  ```
  cat
  ```

   returned by 

  ```
  whatis
  ```

  ?

  - **Answer**: "concatenate files"

### Step 2: Use `man` Command

Imagine you want more details about `cat` and its options.

- **Command**: `man cat`

- Question

  : What option can you use to number the output lines of the 

  ```
  cat
  ```

   command?

  - **Answer**: `-n, --number`

- **Note**: Press `Q` to exit the manual page.

### Step 3: Use `apropos` Command

Imagine you've heard of a command that prints the first part of a file but can't remember the exact command.

- **Command**: `apropos -a first part file`

- Question

  : Which command returns the first part of a file?

  - **Answer**: `head`

## Task 2: Explore the `useradd` Command

### Step 1: Use `man` Command

Imagine you need to set the expiration date for a temporary user account using the `useradd` command.

- **Command**: `man useradd`

- Question

  : Which option can be used with the 

  ```
  useradd
  ```

   command to set an expiration date for a temporary user account?

  - **Answer**: `-e`

- **Note**: Press `Q` to exit the manual page.

## Task 3: Explore the `rm` and `rmdir` Commands

### Step 1: Use `whatis` Command

You need to determine the difference between the `rm` and `rmdir` commands.

- Commands

  :

  - `whatis rm`
  - `whatis rmdir`

- Question

  : Which of these commands removes only empty directories?

  - **Answer**: `rmdir`

## Task 4: Determine Which Command to Use

### Step 1: Use `apropos` Command

Imagine you need to create a new group but can't remember the command.

- **Command**: `apropos -a create new group`

- Question

  : What command can you use to create a new group?

  - **Answer**: `groupadd`

## Conclusion

Great work! You now have practical experience using basic Linux Bash shell commands to:

- Get a short description of a command using `whatis`.
- Display the man pages for a command using `man`.
- Find commands based on keywords about their function using `apropos`.