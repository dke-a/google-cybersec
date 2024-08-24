# Maintain Awareness with Network Monitoring

---

## **Introduction to Network Traffic and Data**

- **Network Traffic**: The amount of data moving across a network. It includes the type of data being transferred, such as HTTP.
- **Network Data**: The data transmitted between devices on a network.
- **Network Monitoring**: Essential for maintaining situational awareness of activity on a network. It involves collecting and analyzing network traffic to detect suspicious activities.

---

## **Knowing Your Network**

- **Network Communication**: Involves the exchange of data between devices using network protocols.
- **Information Provided by Network Communications**: Includes source and destination IP addresses, data transfer amounts, date and time, and more.
- **Baseline**: A reference point used to identify normal or expected network behavior. Understanding a baseline is critical for identifying deviations and potential security threats.

---

## **Monitoring Your Network**

After establishing a baseline, monitoring focuses on detecting deviations from expected behavior. Key components to monitor include:

### **Flow Analysis**

- **Flow**: Refers to the movement of network communications, including information on packets, protocols, and ports.
- **Ports and Protocols**: Ports are often associated with network protocols (e.g., port 443 is commonly used by HTTPS).
- **Command and Control (C2)**: Techniques used by malicious actors to maintain communication with compromised systems, often using non-standard ports and protocols to avoid detection.

### **Packet Payload Information**

- **Packet Components**: Include details like source and destination IP addresses and packet payload information (the actual data transmitted).
- **Monitoring Payloads**: Helps detect unusual activity, such as unauthorized data transmission (data exfiltration).

### **Temporal Patterns**

- **Time Information**: Useful for understanding network activity patterns. For example, unusual traffic outside normal business hours may indicate a security issue.
- **Off-Baseline Activity**: Should be investigated as it may suggest a potential security incident.

---

## **Protecting Your Network**

- **Security Operations Center (SOC)**: Focuses on maintaining the security of an organization through detection and response.
- **Network Operations Center (NOC)**: Monitors network performance, availability, and uptime, responding to network disruptions.
- **Indicators of Compromise (IoC)**: Signs of potential security incidents detected through network monitoring.

### **Network Monitoring Tools**

- **Intrusion Detection Systems (IDS)**: Monitor system activity and alert on possible intrusions, often focusing on packet payloads to detect threats.
- **Network Protocol Analyzers (Packet Sniffers)**: Capture and analyze network data traffic, allowing detailed manual analysis of network communications. Examples include tools like tcpdump and Wireshark.

---

## **Key Takeaways**

- **Understanding and Monitoring Networks**: Essential for detecting and responding to security incidents. Establishing a baseline of normal traffic behavior aids in identifying deviations that may indicate threats.
- **Network Monitoring Tools**: IDS and packet sniffers are crucial for analyzing and protecting network activities.

---

## **Resources**

- **Network Traffic**: Learn more about the components of network traffic that organizations can monitor from [network traffic - MITRE ATT&CK®](https://attack.mitre.org/datasources/DS0029/).
- **Data Exfiltration Techniques**: Explore different techniques attackers use to exfiltrate data at [data exfiltration techniques - MITRE ATT&CK®](https://attack.mitre.org/tactics/TA0010/).

---