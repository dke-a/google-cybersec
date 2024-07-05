# File Permissions and Ownership

## Introduction

Understanding and managing file permissions is crucial for maintaining the security and integrity of a Linux system. This guide will review how to read, display, and change permissions, as well as the principle of least privilege, which ensures that users have only the permissions necessary for their tasks.

## Reading Permissions

### Permission Types

- Read (r)

  :

  - **Files**: Ability to read the file contents.
  - **Directories**: Ability to read all contents in the directory, including files and subdirectories.

- Write (w)

  :

  - **Files**: Ability to modify the file contents.
  - **Directories**: Ability to create new files in the directory.

- Execute (x)

  :

  - **Files**: Ability to execute the file if it’s a program.
  - **Directories**: Ability to enter the directory and access its files.

### Owner Types

- **User (u)**: The owner of the file.
- **Group (g)**: A group that the owner is part of.
- **Other (o)**: All other users on the system.

### Permission Representation

Permissions are represented by a 10-character string. Each character provides specific information:

1. **File Type**: `d` for directory, `-` for a regular file.
2. **User Permissions**: `r`, `w`, `x` for read, write, and execute respectively.
3. **Group Permissions**: `r`, `w`, `x` for read, write, and execute respectively.
4. **Other Permissions**: `r`, `w`, `x` for read, write, and execute respectively.

### Example:

```
lua
Copy code
drwxrwxrwx
|  |  |  |
|  |  |  +-- Execute permission for others
|  |  +-- Write permission for others
|  +-- Read permission for others
+-- Execute permission for group
+-- Write permission for group
+-- Read permission for group
+-- Execute permission for user
+-- Write permission for user
+-- Read permission for user
```

## Exploring Existing Permissions

### Using `ls` Command

- `ls -a`: Displays hidden files.
- `ls -l`: Displays permissions to files and directories along with owner name, group, file size, and the time of last modification.
- `ls -la`: Combines the above two options.

## Changing Permissions

### Principle of Least Privilege

The principle of least privilege is the concept of granting only the minimal access and authorization required to complete a task. This minimizes security risks by ensuring that users do not have unnecessary permissions.

### Using `chmod`

The `chmod` command changes permissions on files and directories. It requires two arguments: the first indicates how to change permissions, and the second specifies the file or directory.

#### Example Commands

- Add all permissions:

  ```
  bash
  Copy code
  chmod u+rwx,g+rwx,o+rwx login_sessions.txt
  ```

- Remove all permissions:

  ```
  bash
  Copy code
  chmod u-rwx,g-rwx,o-rwx login_sessions.txt
  ```

- Set read permissions:

  ```
  bash
  Copy code
  chmod u=r,g=r,o=r login_sessions.txt
  ```

#### Arguments and Symbols

- **u**: User
- **g**: Group
- **o**: Other
- **+**: Adds permissions
- **-**: Removes permissions
- **=**: Assigns permissions exactly as specified

#### Example Breakdown

- `chmod g+w,o-r access.txt`: Adds write permissions for the group and removes read permissions from others.

## Practical Example: Principle of Least Privilege in Action

Consider a file called `bonuses.txt` in the `compensation` directory, owned by `hrrep1` in the Human Resources department. To ensure compliance with the principle of least privilege, only `hrrep1` needs access to this file.

1. **Check Permissions**:

   ```
   bash
   Copy code
   ls -l bonuses.txt
   ```

   Output:

   ```
   diff
   Copy code
   -rw-rw---- 1 hrrep1 hr 0 Jan 1 12:00 bonuses.txt
   ```

2. **Adjust Permissions**:

   ```
   bash
   Copy code
   chmod g-rw bonuses.txt
   ```

   Updated Permissions:

   ```
   diff
   Copy code
   -rw------- 1 hrrep1 hr 0 Jan 1 12:00 bonuses.txt
   ```

## Key Takeaways

- **Managing Permissions**: Essential for protecting sensitive files and maintaining system security.
- **Using `ls`**: With `-l` and `-la` options, you can investigate directory and file permissions.
- **Using `chmod`**: Allows you to change user permissions to align with the principle of least privilege.