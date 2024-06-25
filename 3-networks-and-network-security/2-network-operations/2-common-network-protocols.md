# Common Network Protocols

In this section, you learned about network protocols and how they organize communication over a network. This reading will delve deeper into network protocols, reviewing some basics and introducing new ones. You will also learn about their involvement in network security.

## Overview of Network Protocols

A network protocol is a set of rules used by two or more devices on a network to describe the order of delivery and the structure of data. Network protocols serve as instructions that accompany the information in the data packet, telling the receiving device what to do with the data. Protocols act as a common language, allowing devices worldwide to communicate and understand each other.

While network protocols are essential for network communication, security analysts must understand their associated security implications. Some protocols have vulnerabilities that malicious actors exploit. For example, the Domain Name System (DNS) protocol can be manipulated to divert traffic to malicious websites.

## Categories of Network Protocols

Network protocols can be divided into three main categories: communication protocols, management protocols, and security protocols. Below are the key protocols you should know as an entry-level security analyst.

### Communication Protocols

1. **Transmission Control Protocol (TCP)**
   - **Definition**: An internet communication protocol that allows two devices to form a connection and stream data.
   - **Process**: Uses a three-way handshake process (SYN, SYN/ACK, ACK).
   - **Layer**: Transport layer in the TCP/IP model.

2. **User Datagram Protocol (UDP)**
   - **Definition**: A connectionless protocol that does not establish a connection before transmission.
   - **Usage**: Suitable for quick transmissions like DNS requests.
   - **Layer**: Transport layer in the TCP/IP model.

3. **Hypertext Transfer Protocol (HTTP)**
   - **Definition**: Provides a method of communication between clients and website servers.
   - **Port**: 80
   - **Security**: Considered insecure; often replaced by HTTPS.
   - **Layer**: Application layer in the TCP/IP model.

4. **Domain Name System (DNS)**
   - **Definition**: Translates internet domain names into IP addresses.
   - **Port**: Typically uses UDP on port 53, switches to TCP if the reply is large.
   - **Layer**: Application layer in the TCP/IP model.

### Management Protocols

1. **Simple Network Management Protocol (SNMP)**
   - **Definition**: Used for monitoring and managing devices on a network.
   - **Functions**: Can reset passwords, change configurations, and report bandwidth usage.
   - **Layer**: Application layer in the TCP/IP model.

2. **Internet Control Message Protocol (ICMP)**
   - **Definition**: Used by devices to report data transmission errors across the network.
   - **Usage**: Commonly used for troubleshooting with the "ping" command.
   - **Layer**: Internet layer in the TCP/IP model.

### Security Protocols

1. **Hypertext Transfer Protocol Secure (HTTPS)**
   - **Definition**: Provides a secure method of communication between clients and website servers.
   - **Port**: 443
   - **Security**: Uses SSL/TLS encryption.
   - **Layer**: Application layer in the TCP/IP model.

2. **Secure File Transfer Protocol (SFTP)**
   - **Definition**: Secure protocol used to transfer files over a network.
   - **Port**: Typically uses TCP port 22 via SSH.
   - **Security**: Uses AES and other encryption types.
   - **Layer**: Application layer in the TCP/IP model.

## Security Implications of Network Protocols

- **Encryption**: Protocols like HTTPS and SFTP use encryption to protect data in transit. However, they do not conceal the source or destination IP address, meaning some basic information about the traffic can still be learned by malicious actors.

## Key Takeaways

- **Understanding Protocols**: Essential for cybersecurity analysts to mitigate vulnerabilities and prevent attacks.
- **Security**: Knowledge of security protocols helps protect data in transit and ensures secure network communication.

Understanding these basic networking protocols is crucial for entry-level cybersecurity analysts. Familiarity with how these protocols function and their roles in network security will enhance your ability to safeguard networks effectively.