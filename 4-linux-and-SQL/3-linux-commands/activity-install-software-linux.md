# Activity: Install Software in a Linux Distribution

## Overview
In this lab activity, you’ll use the Advanced Package Tool (APT) and `sudo` to install and uninstall applications in a Linux Bash shell. You'll work with Suricata and tcpdump, which are network security applications used to capture and analyze network traffic. The lab environment uses a Debian-based distribution of Linux, ensuring you can safely experiment without affecting your primary system.

## Scenario
As a security analyst, you need to have Suricata and tcpdump installed on your system. You will install, uninstall, and reinstall these applications on your Linux Bash shell, confirming the installations at each step.

## Tasks
### Task 1: Ensure that APT is Installed
1. **Check if APT is installed**:
   - Open the Bash shell.
   - Type `apt` and press `ENTER`.
   - Confirm that APT displays basic usage information.

   ```sh
   apt 1.8.2.3 (amd64)
   Usage: apt [options] command
   ...

- Click "Check my progress" to verify the task.

### Task 2: Install and Uninstall the Suricata Application

1. **Install Suricata**:

   - Type the following command and press `ENTER`:

   ```bash
   sudo apt install suricata
   ```

   - When prompted, press `ENTER` to continue with the default response.

   **Verify Installation**:

   - Type `suricata` and press `ENTER`.

   ```bash
   suricata
   ```

   **Expected Output**:

   ```bash
   Suricata 4.1.2
   USAGE: suricata [OPTIONS] [BPF FILTER]
   ...
   ```

2. **Uninstall Suricata**:

   - Type the following command and press `ENTER`:

   ```
   sh
   Copy code
   sudo apt remove suricata
   ```

   - When prompted, press `ENTER` to continue with the default response.

   **Verify Uninstallation**:

   - Type `suricata` and press `ENTER`.

   ```
   sh
   Copy code
   suricata
   ```

   **Expected Output**:

   ```
   sh
   Copy code
   -bash: /usr/bin/suricata: No such file or directory
   ```

   - Click "Check my progress" to verify the task.

### Task 3: Install the tcpdump Application

1. **Install tcpdump**:

   - Type the following command and press `ENTER`:

   ```
   sh
   Copy code
   sudo apt install tcpdump
   ```

   - Click "Check my progress" to verify the task.

### Task 4: List the Installed Applications

1. **List Installed Applications**:

   - Type the following command and press `ENTER`:

   ```
   sh
   Copy code
   apt list --installed
   ```

   - Search through the list to find `tcpdump`.

   **Expected Output**:

   ```
   sh
   Copy code
   ...
   tcpdump/oldstable,now 4.9.3-1~deb10u2 amd64 [installed]
   ...
   ```

   - Click "Check my progress" to verify the task.

### Task 5: Reinstall the Suricata Application

1. **Reinstall Suricata**:

   - Type the following command and press `ENTER`:

   ```
   sh
   Copy code
   sudo apt install suricata
   ```

   - When prompted, press `ENTER` to continue with the default response.

2. **Verify Installation**:

   - Type the following command and press `ENTER`:

   ```
   sh
   Copy code
   apt list --installed
   ```

   - Search through the list to confirm that Suricata is installed.

   **Expected Output**:

   ```
   sh
   Copy code
   ...
   suricata/oldstable,now 4.1.2-1~deb10u2 amd64 [installed]
   ...
   ```

## End Your Lab

After completing all tasks, refer to the "End your Lab" section to properly end your lab session.

## Key Takeaways

- **APT**: A package manager for Debian-based systems.

- **Suricata**: A network analysis tool for intrusion detection.

- **tcpdump**: A command-line tool for capturing network traffic.

- Commands

  :

  - `sudo apt install [package]`: Installs a package.
  - `sudo apt remove [package]`: Uninstalls a package.
  - `apt list --installed`: Lists installed packages.

Completing this lab activity will help you understand how to manage applications in a Linux environment, a crucial skill for a security analyst.