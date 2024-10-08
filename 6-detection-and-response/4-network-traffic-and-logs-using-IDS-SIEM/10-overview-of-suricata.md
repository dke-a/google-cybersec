# Overview of Suricata

So far, you've learned about detection signatures and were introduced to Suricata, an intrusion detection system (IDS).

In this reading, you’ll explore more about Suricata and the value of writing customized signatures and configurations. This is an important skill to build in your cybersecurity career as you may be tasked with deploying and maintaining IDS tools.

## Introduction to Suricata

[**Suricata**](https://suricata.io/) is an open-source intrusion detection system, intrusion prevention system, and network analysis tool.

### **Suricata Features**

There are three main ways Suricata can be used:

- **Intrusion Detection System (IDS)**: As a network-based IDS, Suricata can monitor network traffic and alert on suspicious activities and intrusions. Suricata can also be set up as a host-based IDS to monitor the system and network activities of a single host like a computer.
- **Intrusion Prevention System (IPS)**: Suricata can also function as an intrusion prevention system (IPS) to detect and block malicious activity and traffic. Running Suricata in IPS mode requires additional configuration, such as enabling IPS mode.
- **Network Security Monitoring (NSM)**: Suricata helps keep networks safe by producing and saving relevant network logs. Suricata can analyze live network traffic, existing packet capture files, and create and save full or conditional packet captures. This is useful for forensics, incident response, and testing signatures.

## Rules

Rules or signatures are used to identify specific patterns, behavior, and conditions of network traffic that might indicate malicious activity. The terms "rule" and "signature" are often used interchangeably in Suricata. Security analysts use **signatures**, or patterns associated with malicious activity, to detect and alert on specific malicious activity.

### **Components of a Signature**

1. **Action**: Describes the action to take if network or system activity matches the signature (e.g., alert, pass, drop, reject).
2. **Header**: Includes network traffic information like source and destination IP addresses, source and destination ports, protocol, and traffic direction.
3. **Rule Options**: Provide different options to customize signatures.

**Note:** The terms "rule" and "signature" are synonymous in Suricata. Rule order affects the final verdict of a packet, especially when conflicting actions such as a drop rule and an alert rule both match on the same packet.

### **Custom Rules**

Although Suricata comes with pre-written rules, it is highly recommended to modify or customize the existing rules to meet your specific security requirements. Custom rules help tailor detection and monitoring, minimizing the number of false positive alerts that security teams receive.

## Configuration File

Before detection tools are deployed and can begin monitoring systems and networks, you must properly configure their settings. A **configuration file** is used to configure the settings of an application. Suricata's configuration file is **suricata.yaml**, which uses the YAML file format for syntax and structure.

## Log Files

Suricata generates two log files when alerts are triggered:

- **eve.json**: The standard Suricata log file. It contains detailed information and metadata about events and alerts generated by Suricata stored in JSON format. This file is used for more detailed analysis and is better suited for log parsing and SIEM log ingestion.
- **fast.log**: Records minimal alert information, including basic IP address and port details about the network traffic. This file is used for basic logging and alerting but is not suitable for incident response or threat hunting tasks.

**Note:** The main difference between eve.json and fast.log is the level of detail recorded, with eve.json being more detailed.

## Key Takeaways

In this reading, you explored some of Suricata's features, rules syntax, and the importance of configuration. Understanding how to configure detection technologies and write effective rules will provide you with clear insight into the activity happening in an environment, thereby improving detection capability and network visibility.

## Resources for More Information

- [Suricata User Guide](https://suricata.readthedocs.io/en/latest/index.html#)
- [Suricata Features](https://suricata.io/features/)
- [Rule Management](https://suricata.readthedocs.io/en/latest/rule-management/suricata-update.html)
- [Rule Performance Analysis](https://suricata.readthedocs.io/en/latest/configuration/suricata-yaml.html#engine-analysis-and-profiling)
- [Suricata Threat Hunting Webinar](https://youtu.be/kaDGolhTu94)
- [Introduction to Writing Suricata Rules](https://youtu.be/tvoqFBVSShA)
- [Eve.json jq Examples](https://suricata.readthedocs.io/en/latest/output/eve/eve-json-examplesjq.html)