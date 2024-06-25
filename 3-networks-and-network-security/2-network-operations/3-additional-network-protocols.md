# Additional Network Protocols

In previous readings and videos, you learned how network protocols organize the sending and receiving of data across a network. You also learned that protocols can be divided into three categories: communication protocols, management protocols, and security protocols.

This reading will introduce you to a few additional concepts and protocols that will come up regularly in your work as a security analyst. Some protocols are assigned port numbers by the Internet Assigned Numbers Authority (IANA). These port numbers are included in the description of each protocol, if assigned. 

## Network Address Translation (NAT)

- **Definition**: NAT allows devices on a local network (LAN) with private IP addresses to communicate with the public internet using a single public IP address.
- **Function**: Routers or firewalls configured for NAT replace private IP addresses with the public IP address for outgoing messages and reverse the process for incoming responses.
- **Layer**: Part of layer 2 (internet layer) and layer 3 (transport layer) of the TCP/IP model.

### IP Address Types

| Private IP Addresses                                         | Public IP Addresses                                          |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Assigned by the router                                       | Assigned by ISP and IANA                                     |
| Unique only within private network                           | Unique address in global internet                            |
| No cost to use                                               | Costs to lease a public IP address                           |
| Address ranges: 10.0.0.0-10.255.255.255, 172.16.0.0-172.31.255.255, 192.168.0.0-192.168.255.255 | Assignable address ranges: 1.0.0.0-9.255.255.255, 11.0.0.0-126.255.255.255, 128.0.0.0-172.15.255.255, 172.32.0.0-192.167.255.255, 192.169.0.0-233.255.255.255 |

## Dynamic Host Configuration Protocol (DHCP)

- **Definition**: An application layer protocol used to automatically assign IP addresses and configure devices on a network.
- **Ports**: DHCP servers operate on UDP port 67, and DHCP clients operate on UDP port 68.
- **Function**: Works with the router to assign unique IP addresses, DNS server addresses, and default gateway addresses to devices.

## Address Resolution Protocol (ARP)

- **Definition**: A network access layer protocol used to translate IP addresses into MAC addresses.
- **Function**: Each device on the network performs ARP and maintains an ARP cache to track matching IP and MAC addresses.
- **Port**: ARP does not use a specific port number.

## Telnet

- **Definition**: An application layer protocol used to connect to remote systems.
- **Security**: Sends all information in clear text, making it less secure than SSH.
- **Port**: TCP port 23.

## Secure Shell (SSH)

- **Definition**: A protocol for creating a secure connection with a remote system.
- **Security**: Provides secure authentication and encrypted communication.
- **Port**: TCP port 22.

## Post Office Protocol (POP)

- **Definition**: An application layer protocol used to manage and retrieve email from a mail server.
- **Versions**: POP3 is the most commonly used version.
- **Ports**: Uses TCP/UDP port 110 for unencrypted emails and TCP/UDP port 995 for encrypted emails (SSL/TLS).

## Internet Message Access Protocol (IMAP)

- **Definition**: An application layer protocol used for managing incoming email.
- **Function**: Downloads headers of emails and message content, allowing access from multiple devices.
- **Ports**: Uses TCP port 143 for unencrypted email and TCP port 993 for encrypted email (TLS).

## Simple Mail Transfer Protocol (SMTP)

- **Definition**: An application layer protocol used to transmit and route email from sender to recipient.
- **Ports**: Uses TCP/UDP port 25 for unencrypted emails and TCP/UDP port 587 for encrypted emails (TLS).

## Protocols and Port Numbers

Network protocols and port numbers are crucial for identifying and managing data packets. Firewalls can filter out unwanted traffic based on port numbers.

| Protocol | Port                                                         |
| -------- | ------------------------------------------------------------ |
| DHCP     | UDP port 67 (servers), UDP port 68 (clients)                 |
| ARP      | None                                                         |
| Telnet   | TCP port 23                                                  |
| SSH      | TCP port 22                                                  |
| POP3     | TCP/UDP port 110 (unencrypted), TCP/UDP port 995 (encrypted, SSL/TLS) |
| IMAP     | TCP port 143 (unencrypted), TCP port 993 (encrypted, SSL/TLS) |
| SMTP     | TCP/UDP Port 25 (unencrypted), TCP/UDP port 587 (encrypted, TLS) |

## Key Takeaways

- **Understanding Protocols**: Essential for cybersecurity analysts to manage network security effectively.
- **Protocol Knowledge**: Knowing where each protocol is structured in the TCP/IP model and which ports they occupy is critical for network security and management.