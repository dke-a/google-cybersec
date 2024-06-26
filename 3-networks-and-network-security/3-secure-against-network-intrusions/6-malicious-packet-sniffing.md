# Malicious Packet Sniffing

## Overview
Packet sniffing is the practice of using software tools to observe data as it moves across a network. It can be used by security analysts to analyze and capture packets for investigating ongoing incidents or debugging network issues. However, malicious actors can also use packet sniffing to gain unauthorized access to information.

## Key Concepts

### Packet Structure
- **Header**: Contains the sender's and receiver's IP addresses.
- **Body**: Contains valuable information like names, dates of birth, personal messages, financial information, and credit card numbers.

### Packet Sniffing
- **Packet Sniffing**: The practice of using software tools to observe data as it moves across a network.

## Types of Packet Sniffing
- **Passive Packet Sniffing**: Data packets are read in transit without altering them.
  - Example: A postal delivery person reading someone else's mail without their knowledge.
- **Active Packet Sniffing**: Data packets are manipulated in transit.
  - Example: A neighbor intercepting and altering a letter before delivering it.

## How Malicious Actors Use Packet Sniffing
- **Interception**: Malicious actors insert themselves between two devices to spy on data packets.
- **Manipulation**: They can change information within the data packets, such as altering a recipient's bank account number.

## Prevention Techniques
- **VPN (Virtual Private Network)**: Encrypts data as it travels across the network, making it unreadable to malicious actors.
- **HTTPS**: Ensures websites use HTTPS, which uses SSL/TLS to encrypt data and prevent eavesdropping.
- **Avoid Unprotected WiFi**: Avoid using unprotected public WiFi networks, which don't use encryption, unless you have a VPN service installed.

## Conclusion
Understanding how threat actors use packet sniffing and implementing preventive measures like VPNs, HTTPS, and avoiding unprotected WiFi can protect against these malicious activities.

---

# Real-life DDoS Attack

## Overview
This case study examines a significant DDoS attack in 2016 against DNS servers, causing major outages for multiple organizations with millions of daily users.

## DNS Servers
- **DNS Servers**: Translate website domain names into the IP addresses of the systems hosting the websites.

## 2016 DDoS Attack on DNS Servers
### Leading Up to the Attack
- **Botnet Creation**: University students created a botnet intended to attack gaming servers and networks.
  - **Botnet**: A collection of malware-infected computers controlled by a single threat actor.
  - **Botnet Attack**: Cyber criminals instruct all bots in the botnet to send data packets to a target system simultaneously.

### The Day of the Attack
- **Date**: October 21, 2016
- **Time**: 7:00 a.m.
- **Impact**:
  - Tens of millions of DNS requests overwhelmed the DNS service provider's system, causing it to shut down.
  - Websites using the service provider became unreachable, affecting users in North America and Europe.
- **Recovery**: Systems were restored after two hours. Subsequent botnet attacks were mitigated due to improved preparedness.

## Key Takeaways
- **Impact of DDoS Attacks**: 
  - **Financial Loss**: Disruption of services can lead to significant financial losses.
  - **Reputation Damage**: Public knowledge of a successful attack can harm an organization's reputation.
  - **Operational Disruption**: Inability to meet customer needs during the attack.
- **Mitigation Strategies**:
  - **Preparedness**: Having a robust incident response plan can mitigate the impact of attacks.
  - **Dynamic Scaling**: Distributing operations across hosts that can be dynamically scaled ensures continuity if baseline infrastructure goes offline.
  - **Continuous Learning**: Security analysts must stay educated on the latest threats and mitigation techniques.

## Conclusion
DDoS attacks can have severe consequences for organizations. Understanding the mechanics and impacts of such attacks is crucial for security analysts to develop effective protection and response strategies.