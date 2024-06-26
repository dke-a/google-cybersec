# Overview of Interception Tactics

In the previous course items, you learned how packet sniffing and IP spoofing are used in network attacks. Because these attacks intercept data packets as they travel across the network, they are called interception attacks.

## Packet Sniffing

### Definition
Packet sniffing is the practice of capturing and inspecting data packets as they travel across a network.

### Mechanism
- **Network Interface Card (NIC)**: Connects a device to a network and reads data transmissions.
  - **Normal Mode**: NIC accepts packets containing the device’s MAC address.
  - **Promiscuous Mode**: NIC accepts all traffic on the network, even packets not addressed to the device.

### Tools
- **Wireshark**: A popular software used to capture and analyze data packets on a network.

### Risks
- **Personal Information**: Captured data may contain sensitive information such as names, dates of birth, and credit card numbers.
- **IP and MAC Addresses**: Can be used for IP spoofing.

## IP Spoofing

### Definition
IP spoofing is a network attack where an attacker changes the source IP address of a data packet to impersonate an authorized system and gain access to a network.

### Common IP Spoofing Attacks

#### On-Path Attack
- **Description**: An attacker intercepts communication between two trusted devices.
- **Mechanism**:
  - Intercepts valuable information like usernames and passwords.
  - Can spoof DNS responses to redirect traffic to malicious sites.
- **Protection**: Encrypt data in transit using TLS.

#### Smurf Attack
- **Description**: Combines IP spoofing with a denial of service (DoS) attack.
- **Mechanism**:
  - Attacker sniffs an authorized user’s IP address.
  - Floods the network with spoofed packets, causing a DoS.
  - Uses protocols like ICMP to overwhelm the network.
- **Protection**: Use advanced firewalls (e.g., NGFW) to detect and block unusual traffic.

#### DoS Attack
- **Description**: Attacker prevents a system from performing legitimate activities or responding to legitimate traffic.
- **Mechanism**:
  - Uses IP packets containing fake IP addresses.
  - Floods the network until the server crashes.
- **Protection**: Implement defense-in-depth strategies, including industry-standard encryption.

## Mitigation Strategies

### Encryption
- **Purpose**: Protects data in transit from being read by malicious actors.
- **Implementation**: Use protocols like SSL/TLS.

### Firewalls
- **Purpose**: Filters incoming and outgoing traffic to prevent unauthorized access.
- **Advanced Firewalls (NGFW)**:
  - Perform deep packet inspection.
  - Detect network anomalies.
  - Block oversized broadcasts and other suspicious activities.

## Key Takeaways
- **Packet Sniffing**: Capturing and analyzing data packets to gather sensitive information.
- **IP Spoofing**: Impersonating an authorized system to gain network access.
- **Common Attacks**: On-path attacks, smurf attacks, and DoS attacks.
- **Mitigation**: Use encryption, advanced firewalls, and defense-in-depth strategies to protect against interception attacks.

Understanding these attacks and how to defend against them is crucial for network security. Analysts need to ensure that multiple layers of defense are in place to mitigate threats and prevent security breaches.