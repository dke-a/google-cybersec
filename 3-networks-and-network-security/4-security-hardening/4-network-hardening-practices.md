# Network Hardening Practices

## Overview
Network hardening focuses on enhancing the security of network-related elements, such as port filtering, network access privileges, and encryption over networks. Certain tasks are performed regularly, while others are performed once and then updated as needed.

### Regularly Performed Tasks
- **Firewall Rules Maintenance**: Regularly updating and maintaining firewall rules to ensure only necessary traffic is allowed.
- **Network Log Analysis**: Using tools like log analyzers or SIEM (Security Information and Event Management) to examine network logs and identify events of interest. SIEM tools collect and analyze log data, presenting it on a single dashboard (single pane of glass) to monitor critical activities.
- **Patch Updates**: Regularly applying software updates to fix vulnerabilities and improve security.
- **Server Backups**: Regularly backing up server data to ensure data recovery in case of an incident.

### Tasks Performed Once
- **Port Filtering**: Configuring firewalls to block or allow certain port numbers to limit unwanted communication. The principle is to allow only necessary ports and disallow any port not used by normal network operations.
- **Network Access Privileges**: Setting up access controls to ensure only authorized users can access specific parts of the network.
- **Encryption for Communication**: Implementing encryption standards to protect data in transit. Higher encryption standards should be applied to restricted zones containing highly classified or confidential data.

## Key Concepts and Tools
- **Firewall**: A security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules.
- **SIEM (Security Information and Event Management)**: A tool that collects and analyzes log data from various sources, providing a centralized view of security events.
- **Port Filtering**: A firewall function that blocks or allows communication based on port numbers.
- **Network Segmentation**: Dividing a network into isolated subnets to improve security and limit the spread of issues.
- **Encryption Standards**: Rules or methods used to conceal outgoing data and decrypt incoming data, ensuring data security during transmission.

### Example of Network Segmentation
- **Subnet for Departments**: Creating isolated subnets for different departments (e.g., marketing and finance) to ensure issues in one subnet don't spread across the entire network.
- **Security Zones**: Separating different security zones, with restricted zones containing highly classified data having much higher encryption standards.

## Summary
Network hardening involves a combination of regular and one-time tasks aimed at enhancing network security. By maintaining firewall rules, analyzing network logs, applying patch updates, and configuring port filtering and encryption, security analysts can protect against vulnerabilities and ensure the network's integrity. Network segmentation and appropriate access controls further strengthen the security framework.

### Key Takeaways
- Regular maintenance and updates are crucial for network security.
- Port filtering and network segmentation help limit vulnerabilities and control access.
- Encryption standards ensure data security during transmission.
- SIEM tools provide a centralized view of security events, aiding in quick identification and response to threats.

This knowledge is essential for completing security certification programs and is foundational for a career as a security analyst.