# Navigate Linux and Read File Content

## Filesystem Hierarchy Standard (FHS)

- **FHS**: Organizes data in Linux, defining how directories, directory contents, and other storage are structured.

### Root Directory

- **Root Directory (`/`)**: The highest-level directory in Linux. All other directories branch from here.

- Standard FHS Directories

  :

  - **/home**: Contains user-specific directories.
  - **/bin**: Stores binary files and executables.
  - **/etc**: Holds system configuration files.
  - **/tmp**: Temporary files; often targeted by attackers.
  - **/mnt**: Mount directory for media like USB drives and hard drives.

### User-Specific Subdirectories

- **Home Directory (`/home`)**: Contains user-specific subdirectories, such as `/home/analyst`.
- **Tilde (`~`)**: Represents the user’s home directory, e.g., `~/logs` is equivalent to `/home/analyst/logs`.

## Navigating the File System

- File Paths

  : Location of files or directories.

  - **Absolute File Path**: Full path from the root, e.g., `/home/analyst/projects`.
  - **Relative File Path**: Path relative to the current directory, e.g., `../projects`.
  - **Dot (`.`)**: Current directory.
  - **Double Dot (`..`)**: Parent directory.

### Key Commands for Navigation

- **pwd (Print Working Directory)**: Displays the current directory.
  - Example: `pwd` returns `/home/analyst`.
- **ls (List)**: Displays names of files and directories in the current directory.
  - Example: `ls` returns `logs`, `oldreports`, `projects`, `reports`, and `updates.txt`.
  - With an argument: `ls /home/analyst/projects` or `ls projects`.
- **cd (Change Directory)**: Navigates between directories.
  - To a subdirectory: `cd logs`.
  - Using an absolute path: `cd /home/analyst/logs`.
  - Using a relative path: `cd ..` moves up one level.

## Common Commands for Reading File Content

- **cat (Concatenate)**: Displays the entire content of a file.

  - Example: `cat updates.txt` shows all contents of `updates.txt`.

- **head**: Displays the beginning of a file, default 10 lines.

  - Example: `head updates.txt`.
  - To specify lines: `head -n 5 updates.txt` for the first 5 lines.

- **tail**: Displays the end of a file, default 10 lines.

  - Example: `tail updates.txt`.

- **less**: Displays the content one page at a time.

  - Example: `less updates.txt`.

  - Navigation in 

    ```
    less
    ```

    :

    - Space bar: Move forward one page.
    - `b`: Move back one page.
    - Down arrow: Move forward one line.
    - Up arrow: Move back one line.
    - `q`: Quit and return to the terminal.

## Key Takeaways

- **Navigation Commands**: Essential for locating and analyzing files. Commands include `pwd`, `ls`, and `cd`.
- **Reading File Content**: Important for analyzing configuration settings, user access reports, and other critical data. Commands include `cat`, `head`, `tail`, and `less`.