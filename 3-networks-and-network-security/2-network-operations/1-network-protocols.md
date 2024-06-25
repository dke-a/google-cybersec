# Network Protocols

Networks benefit from having rules that ensure data sent over the network gets to the right place. These rules are known as network protocols. Network protocols are a set of rules used by two or more devices on a network to describe the order of delivery and the structure of the data.

## Key Network Protocols

### Transmission Control Protocol (TCP)
- **Definition**: TCP is an internet communications protocol that allows two devices to form a connection and stream data.
- **Function**: Establishes a connection using a process known as a handshake before any further communications can take place.
- **Example**: When you type a website address into your browser, TCP establishes communication with the web server to retrieve the webpage data.

### Address Resolution Protocol (ARP)
- **Definition**: ARP is used to determine the MAC address of the next router or device on the path.
- **Function**: Ensures that data packets get to the right place by mapping IP addresses to MAC addresses.

### Hypertext Transfer Protocol Secure (HTTPS)
- **Definition**: HTTPS is a secure network protocol that provides a secure method of communication between client and website servers.
- **Function**: Allows secure sending and receiving of webpage data between your browser and the web server.
- **Security**: Uses Secure Sockets Layer (SSL) and Transport Layer Security (TLS) to encrypt data, protecting it from malicious actors.

### Domain Name System (DNS)
- **Definition**: DNS is a network protocol that translates internet domain names into IP addresses.
- **Function**: Sends the domain name to a DNS server to retrieve the corresponding IP address, which is then used as the destination address for data packets.

## Scenario Example: Accessing a Website
1. **Step 1**: Type the website address (e.g., www.yummyrecipesforme.org) into the browser.
2. **Step 2**: TCP establishes a connection with the web server using a handshake.
3. **Step 3**: Data packets move across the network, with ARP determining the MAC address of the next router or device.
4. **Step 4**: HTTPS provides a secure method for the browser to request and receive the webpage data.
5. **Step 5**: DNS translates the domain name into an IP address, directing the data packets to the correct web server.

## Importance of Network Protocols in Security
- **HTTPS**: Encrypts data to ensure secure communication between clients and servers, protecting sensitive information from being intercepted by malicious actors.
- **SSL/TLS**: Encryption technologies used by HTTPS to maintain data integrity and security.

## Key Takeaways
- **Network Protocols**: Essential for organizing and securing data transmission across networks.
- **TCP/IP and ARP**: Establish connections and ensure data reaches the correct destination.
- **HTTPS and DNS**: Provide secure communication and accurate routing of data packets.
- **Security**: Protocols like HTTPS play a crucial role in protecting data from malicious actors.

As a security analyst, familiarity with these protocols is crucial for understanding and securing network communications.