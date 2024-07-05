# Change Permissions in Linux

## Introduction

In this section, we’ll explore how to change file and directory permissions in Linux using the `chmod` command. Changing permissions is essential for managing access to system files and protecting them from unauthorized modifications.

## Reasons for Changing Permissions

- **Department or Workgroup Changes**: Users may change departments or be assigned to different workgroups, necessitating changes in their permissions.
- **Project Requirements**: Users might no longer need access to certain files after a project's completion.
- **Security and Protection**: Adjusting permissions helps protect system files from accidental or deliberate alterations or deletions.

## The `chmod` Command

### Overview

`chmod` stands for "change mode" and is used to change permissions on files and directories. There are two modes for changing permissions: symbolic and numeric. This guide focuses on the symbolic mode.

### Symbolic Mode

Symbolic mode involves using symbols to represent the changes you want to make to file permissions.

### Example Breakdown

Consider the following example: `chmod g+w,o-r access.txt`

- **Target File**: `access.txt` is the file whose permissions we want to change.
- **Owner Types**:
  - `u` represents the user (owner).
  - `g` represents the group.
  - `o` represents others (everyone else).
- **Operators**:
  - `+` (plus) adds a permission.
  - `-` (minus) removes a permission.
- **Permissions**:
  - `r` for read.
  - `w` for write.
  - `x` for execute.

### Example Explanation

- `g+w`: Add write permissions for the group.
- `o-r`: Remove read permissions from others.

### Checking Permissions

Use the `ls -l` command to check the current permissions of a file:

```
css
Copy code
-rw-r--r-- 1 analyst security 0 Jan 1 12:00 access.txt
```

This output indicates:

- ```
  -rw-r--r--
  ```

  : Permission string.

  - `-` (first character): File type (hyphen for regular file, `d` for directory).
  - `rw-` (2nd to 4th characters): Read and write permissions for the user.
  - `r--` (5th to 7th characters): Read permissions for the group.
  - `r--` (8th to 10th characters): Read permissions for others.

## Changing Permissions Example

1. **Initial Permissions Check**:

   ```
   bash
   Copy code
   ls -l access.txt
   ```

   Output:

   ```
   css
   Copy code
   -rw-r--r-- 1 analyst security 0 Jan 1 12:00 access.txt
   ```

2. **Change Permissions**:

   ```
   bash
   Copy code
   chmod g+w,o-r access.txt
   ```

3. **Verify Permissions**:

   ```
   bash
   Copy code
   ls -l access.txt
   ```

   Output:

   ```
   diff
   Copy code
   -rw-rw---- 1 analyst security 0 Jan 1 12:00 access.txt
   ```

   Changes:

   - Group (`g`) now has write permissions (`w` added).
   - Others (`o`) no longer have read permissions (`r` removed).

## 