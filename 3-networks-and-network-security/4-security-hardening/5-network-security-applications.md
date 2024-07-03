# Network Security Applications

## Overview
This section covers the topic of network hardening and monitoring. Each device, tool, or security strategy implemented by security analysts further protects—or hardens—the network. This approach of adding layers of security to a network is referred to as defense in depth.

## Devices and Tools for Network Security

### Firewall
- **Function**: Allows or blocks traffic based on a set of rules.
- **Types**: 
  - **Stateless Firewalls**: Operate based on predefined rules.
  - **Stateful Firewalls**: Keep track of information passing through and proactively filter out threats.
  - **Next-Generation Firewalls (NGFWs)**: Inspect packet payloads in addition to headers.
- **Placement**: Between the internal network and external internet.
- **Advantages**: Basic level of security; easy to implement.
- **Disadvantages**: Only filters packets based on header information in basic firewalls; limited by the specificity of rules.

### Intrusion Detection System (IDS)
- **Function**: Monitors system activity and alerts administrators about possible intrusions.
- **Types**:
  - **Signature-based IDS**: Detects known attack signatures.
  - **Anomaly-based IDS**: Detects deviations from normal behavior.
- **Placement**: Behind the firewall, before the LAN.
- **Advantages**: Adds an additional layer of defense; alerts on suspicious activity.
- **Disadvantages**: Can only detect known attacks or obvious anomalies; does not stop incoming traffic; relies on administrators to act on alerts.

### Intrusion Prevention System (IPS)
- **Function**: Monitors system activity for intrusive activity and takes action to stop it.
- **Types**:
  - **Network-based IPS (NIPS)**: Monitors entire network traffic.
  - **Host-based IPS (HIPS)**: Monitors traffic on individual hosts.
- **Placement**: Behind the firewall, before the LAN.
- **Advantages**: Actively stops anomalies; provides high-level security.
- **Disadvantages**: Inline appliance; potential for false positives, blocking legitimate traffic.

### Full Packet Capture Devices
- **Function**: Record and analyze all data transmitted over the network.
- **Advantages**: Useful for detailed analysis and forensic investigations.

### Security Information and Event Management (SIEM)
- **Function**: Collects and analyzes log data to monitor critical activities in an organization.
- **Features**:
  - **Real-time Monitoring**: Aggregates security event data from multiple sources.
  - **Dashboard Interface**: Provides a single pane of glass for monitoring.
  - **Automated Alerts**: Notifies security analysts of suspicious activities.
- **Advantages**: Centralizes data for easier analysis; supports quick response to threats.
- **Disadvantages**: Does not take action to stop or prevent events; requires skilled personnel to interpret and respond to data.

## Benefits of Layered Security
Layered security provides multiple levels of defense, increasing the difficulty for attackers to penetrate the network. Combining different tools enhances security incrementally, from basic firewalls to comprehensive monitoring and prevention systems.

## Key Takeaways
| **Devices / Tools**                                  | **Advantages**                                               | **Disadvantages**                                            |
| ---------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Firewall**                                         | Allows or blocks traffic based on a set of rules.            | Filters packets based only on information provided in the headers. |
| **Intrusion Detection System (IDS)**                 | Detects and alerts admins about possible intrusions and malicious traffic. | Can only scan for known attacks or obvious anomalies; does not stop incoming traffic. |
| **Intrusion Prevention System (IPS)**                | Monitors system activity for intrusions and anomalies; takes action to stop them. | Inline appliance; potential for false positives blocking legitimate traffic. |
| **Security Information and Event Management (SIEM)** | Collects and analyzes log data from multiple network machines; aggregates security events. | Reports on possible security issues; does not take action to stop or prevent events. |

## Conclusion
Security hardening involves layering different security measures to protect the network effectively. Understanding the role of each tool and its place in the network topology helps security analysts implement a robust defense strategy against potential attacks.