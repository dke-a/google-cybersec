# Exemplar: Manage Authorization

## Activity Overview

In this lab activity, you’ll use Linux commands to configure authorization. Authorization is crucial for maintaining system security by ensuring that only authorized users have access to specific resources.

### Importance of Authorization

Authorization prevents unauthorized users from accessing and modifying files, thus protecting sensitive information and maintaining system integrity.

### Scenario

In this scenario, you must manage permissions on the files in the `/home/researcher2/projects` directory for the `researcher2` user, who is part of the `research_team` group. Your tasks include checking and modifying permissions to align with appropriate access levels.

### Tasks Overview

1. **Check file and directory details**
2. **Change file permissions**
3. **Change file permissions on a hidden file**
4. **Change directory permissions**

## Task 1: Check File and Directory Details

### Navigate to the Projects Directory

Command:

```
bash
Copy code
cd projects
```

### List Contents and Permissions

Command:

```
bash
Copy code
ls -l
```

Example Output:

```
diff
Copy code
total 20
drwx--x--- 2 researcher2 research_team 4096 Oct 14 18:40 drafts
-rw-rw-rw- 1 researcher2 research_team   46 Oct 14 18:40 project_k.txt
-rw-r----- 1 researcher2 research_team   46 Oct 14 18:40 project_m.txt
-rw-rw-r-- 1 researcher2 research_team   46 Oct 14 18:40 project_r.txt
-rw-rw-r-- 1 researcher2 research_team   46 Oct 14 18:40 project_t.txt
```

### Understanding Permissions

- **File Type**: `d` for directory, `-` for regular file.
- **User Permissions**: Characters 2-4 (e.g., `rwx`).
- **Group Permissions**: Characters 5-7 (e.g., `rwx`).
- **Other Permissions**: Characters 8-10 (e.g., `rwx`).

### Check for Hidden Files

Command:

```
bash
Copy code
ls -la
```

### Identifying Hidden Files

Example Output:

```
diff
Copy code
-rw-rw-r-- 1 researcher2 research_team  46 Oct 14 18:40 .project_x.txt
```

## Task 2: Change File Permissions

### Identify Files with Incorrect Permissions

Command:

```
bash
Copy code
ls -l
```

### Example Output Analysis

File `project_k.txt` grants write permissions to others (`-rw-rw-rw-`).

### Remove Write Permissions from Others

Command:

```
bash
Copy code
chmod o-w project_k.txt
```

### Restrict Group Permissions on `project_m.txt`

Command:

```
bash
Copy code
chmod g-r project_m.txt
```

## Task 3: Change File Permissions on a Hidden File

### Check Hidden File Permissions

Command:

```
bash
Copy code
ls -la
```

### Identify Incorrect Write Permissions

Example Output Analysis: File `.project_x.txt` grants write permissions to user and group.

### Adjust Permissions

Command:

```
bash
Copy code
chmod u-w,g-w,g+r .project_x.txt
```

## Task 4: Change Directory Permissions

### Check Permissions of `drafts` Directory

Command:

```
bash
Copy code
ls -l
```

### Example Output Analysis

Directory `drafts` grants execute permissions to the group (`drwx--x---`).

### Remove Execute Permission from Group

Command:

```
bash
Copy code
chmod g-x drafts
```

## Conclusion

In this lab, you have gained practical experience with Linux commands to:

- Examine file and directory permissions.
- Change permissions on files and directories to align with the principle of least privilege.
- Ensure that only authorized users have access to sensitive information.