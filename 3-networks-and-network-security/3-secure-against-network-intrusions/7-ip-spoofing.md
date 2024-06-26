# IP Spoofing

## Overview
IP spoofing is a network attack where an attacker changes the source IP address of a data packet to impersonate an authorized system and gain access to a network. This attack allows the hacker to communicate over the network with the target computer, bypassing firewall rules that may prevent outside traffic.

## Types of IP Spoofing Attacks

### On-Path Attack
- **Description**: An attacker places themselves in the middle of an authorized connection and intercepts or alters the data in transit.
- **Mechanism**:
  - The attacker gains access to the network.
  - Positions themselves between two devices (e.g., a web browser and a web server).
  - Sniffs packet information to learn the IP and MAC addresses of the devices.
  - Pretends to be one of the devices to intercept or alter communications.

### Replay Attack
- **Description**: An attacker intercepts a data packet in transit and delays or repeats it at another time.
- **Mechanism**:
  - Intercepts a legitimate network transmission.
  - Delays the packet, causing connection issues.
  - Repeats the transmission at a later time to impersonate the authorized user.

### Smurf Attack
- **Description**: A combination of a DDoS attack and an IP spoofing attack.
- **Mechanism**:
  - Attacker sniffs an authorized user's IP address.
  - Floods the target IP address with packets.
  - Overwhelms the target computer, potentially bringing down a server or the entire network.

## Preventing IP Spoofing

### Encryption
- **Purpose**: Ensures data in network transfers cannot be read by malicious actors.
- **Implementation**: Use encryption protocols such as SSL/TLS to protect data in transit.

### Firewalls
- **Purpose**: Firewalls can be configured to protect against IP spoofing.
- **Configuration**:
  - Create rules to reject all incoming traffic that has the same IP address as the local network.
  - If a firewall receives a data packet from the internet where the sender's IP address matches the private network's address, the firewall will deny the transmission.
  - This prevents malicious actors from spoofing IP addresses to appear as if they are from within the local network.

## Key Takeaways
- **IP Spoofing**: Attackers change the source IP address of a data packet to impersonate an authorized system.
- **On-Path Attack**: Interception and alteration of data between two communicating devices.
- **Replay Attack**: Delaying or repeating intercepted data packets.
- **Smurf Attack**: Combining IP spoofing with DDoS to flood and overwhelm a target.
- **Prevention**: Use encryption to protect data and configure firewalls to reject spoofed IP addresses.

Understanding IP spoofing and its variations is crucial for securing networks against unauthorized access and data breaches.