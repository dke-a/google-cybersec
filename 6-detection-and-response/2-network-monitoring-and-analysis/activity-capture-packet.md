## Activity: Capture Your First Packet with tcpdump

### Overview

As a security analyst, you need to be adept at capturing and analyzing network traffic in a Linux environment. This lab guides you through the process of using **tcpdump** to capture network traffic and analyze the packet data. You'll use a Linux terminal to perform these tasks.

### Scenario

You're tasked with capturing and analyzing live network traffic on a Linux virtual machine. The lab starts with your user account logged in to a Linux terminal. A sample packet capture file is available in your home directory for further analysis.

### Tasks Breakdown

### Task 1: Identify Network Interfaces

1. Identify available network interfaces:

   - Use `ifconfig` to list network interfaces:

     ```bash
     bashCopy code
     sudo ifconfig
     ```

   - Identify the network interface to capture packets from, typically `eth0`.

2. Use tcpdump to list interfaces:

   - Use `tcpdump -D` to list available interfaces:

     ```bash
     bashCopy code
     sudo tcpdump -D
     ```

### Task 2: Inspect Network Traffic with tcpdump

1. Capture and display 5 packets from `eth0`:

   - Command to capture packets:

     ```bash
     bashCopy code
     sudo tcpdump -i eth0 -v -c 5
     ```

   - The output will include timestamp, protocol, IP addresses, ports, and detailed packet information.

### Task 3: Capture Network Traffic to a File

1. Capture HTTP traffic on port 80:

   - Command to capture 9 packets and save them to `capture.pcap`:

     ```bash
     bashCopy code
     sudo tcpdump -i eth0 -nn -c 9 port 80 -w capture.pcap &
     ```

   - Generate HTTP traffic using `curl`:

     ```bash
     bashCopy code
     curl opensource.google.com
     ```

### Task 4: Filter Captured Packet Data

1. Read and filter the captured packets:

   - Display packet headers:

     ```bash
     bashCopy code
     sudo tcpdump -nn -r capture.pcap -v
     ```

   - Display extended packet data in hexadecimal and ASCII:

     ```bash
     bashCopy code
     sudo tcpdump -nn -r capture.pcap -X
     ```

### Key tcpdump Commands Recap

- **List interfaces:**

  ```bash
  bashCopy code
  sudo tcpdump -D
  ```

- **Capture packets on an interface:**

  ```bash
  bashCopy code
  sudo tcpdump -i eth0 -v -c 5
  ```

- **Capture to a file:**

  ```bash
  bashCopy code
  sudo tcpdump -i eth0 -nn -c 9 port 80 -w capture.pcap
  ```

- **Read and filter packets from a file:**

  - Basic view:

    ```bash
    bashCopy code
    sudo tcpdump -nn -r capture.pcap -v
    ```

  - Extended view (Hex and ASCII):

    ```bash
    bashCopy code
    sudo tcpdump -nn -r capture.pcap -X
    ```

### Key Takeaways

- **tcpdump** is a powerful command-line tool for capturing and analyzing network traffic.
- Capturing network traffic involves identifying the right network interface and applying appropriate filters.
- The captured data can be saved for further analysis using various tcpdump options.
- Filtering and interpreting captured packets is essential for effective network security analysis.