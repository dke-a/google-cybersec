# Add and Manage Users with Linux Commands

## Activity Overview

In this lab activity, you’ll manage user access in the Linux Bash shell using commands such as `useradd`, `usermod`, `userdel`, and `chown`. Authentication ensures users are who they claim to be, while authorization grants access to specific system resources. As a security analyst, it's essential to manage user access effectively.

## Scenario

A new employee, researcher9, joins the Research department. You will:

1. Add them to the system.
2. Assign them to their primary group.
3. Make them the owner of a specific file.
4. Add them to a supplementary group.
5. Delete the user from the system when they leave the organization.

## Tasks

### Task 1: Add a New User

A new employee, researcher9, has joined the Research department. You need to add them to the system.

1. Add a user called researcher9:

   ```
   bash
   Copy code
   sudo useradd researcher9
   ```

2. Add the new user to the 

   ```
   research_team
   ```

    group as their primary group:

   ```
   bash
   Copy code
   sudo usermod -g research_team researcher9
   ```

Alternatively, you can perform both steps at once: `bash sudo useradd researcher9 -g research_team`

### Task 2: Assign File Ownership

The new employee, researcher9, will take responsibility for project_r. Make them the owner of the `project_r.txt` file located in the `/home/researcher2/projects` directory.

1. Use the 

   ```
   chown
   ```

    command to make researcher9 the owner of the 

   ```
   project_r.txt
   ```

    file:

   ```
   bash
   Copy code
   sudo chown researcher9 /home/researcher2/projects/project_r.txt
   ```

### Task 3: Add the User to a Secondary Group

A couple of months later, researcher9's role changes, and they need to be added to the `sales_team` group while retaining their primary group as `research_team`.

1. Use the 

   ```
   usermod
   ```

    command with the 

   ```
   -a
   ```

    and 

   ```
   -G
   ```

    options to add researcher9 to the 

   ```
   sales_team
   ```

    group as a secondary group:

   ```
   bash
   Copy code
   sudo usermod -a -G sales_team researcher9
   ```

### Task 4: Delete a User

A year later, researcher9 leaves the company. You must remove them from the system.

1. Delete researcher9 from the system:

   ```
   bash
   Copy code
   sudo userdel researcher9
   ```

   **Note:** This command outputs:

   ```
   sql
   Copy code
   Userdel: Group researcher9 not removed because it is not the primary group of user researcher9.
   ```

2. Delete the researcher9 group that is no longer required:

   ```
   bash
   Copy code
   sudo groupdel researcher9
   ```

## Conclusion

You now have practical experience in using basic Linux Bash shell commands to:

- Add new users and assign them to groups.
- Modify user account details and group memberships.
- Assign file ownership to users.
- Delete users and clean up associated groups.

These tasks are essential for managing user access and maintaining system security.