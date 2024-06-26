# Denial of Service (DoS) Attacks

## Introduction
A Denial of Service (DoS) attack targets a network or server and floods it with network traffic, aiming to disrupt normal business operations. The goal is to overload a network device with so much information that it crashes or becomes unresponsive to legitimate users, causing potential financial loss and vulnerability to other security threats.

## Types of DoS Attacks

### Distributed Denial of Service (DDoS) Attacks
- **Definition**: A type of DoS attack using multiple devices or servers from different locations to flood the target network with unwanted traffic.
- **Impact**: The total amount of traffic overwhelms the target server, causing a denial of service.
- **Example**: Crafting a packet that causes a router to spend extra time processing, thereby overloading it.

### Network Level DoS Attacks
These attacks target network bandwidth to slow down traffic. Common types include:

#### SYN Flood Attack
- **Mechanism**: Simulates the TCP connection process and floods the server with SYN packets.
- **Process**:
  - **Step 1**: Device sends a SYN (synchronize) request to the server.
  - **Step 2**: Server responds with a SYN/ACK packet and leaves a port open.
  - **Step 3**: Device sends an ACK packet, establishing a TCP connection.
- **Attack**: Flooding a server with SYN requests exceeds available ports, overwhelming the server.

#### ICMP Flood Attack
- **ICMP**: Stands for Internet Control Message Protocol, used by devices to report data transmission errors.
- **Mechanism**: Attacker repeatedly sends ICMP packets to a network server.
- **Impact**: Uses up all bandwidth for incoming and outgoing traffic, causing the server to crash.

#### Ping of Death Attack
- **Mechanism**: Hacker sends an oversized ICMP packet (larger than 64 KB) to a system.
- **Impact**: Overloads the system, causing it to crash.
- **Analogy**: Dropping a large rock on a small anthill, crushing the ants and disrupting the colony.

## Key Takeaways
- DoS attacks aim to disrupt normal operations by overloading network resources.
- DDoS attacks amplify the impact by using multiple devices.
- Common DoS attack methods include SYN flood, ICMP flood, and Ping of Death.
- These attacks exploit vulnerabilities in communication protocols and can cause significant disruption and financial loss.

Understanding and mitigating these attacks is crucial for maintaining network security and ensuring continuous business operations.