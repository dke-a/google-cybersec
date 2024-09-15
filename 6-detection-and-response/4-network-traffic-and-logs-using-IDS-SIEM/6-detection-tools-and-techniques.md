# Detection Tools and Techniques

In this reading, you’ll explore the different types of Intrusion Detection System (IDS) technologies and the alerts they produce. Additionally, you'll examine the two common detection techniques used by these systems: signature-based analysis and anomaly-based analysis. Understanding the capabilities and limitations of IDS technologies and their detection techniques will help you better identify, analyze, and respond to security events.

## Intrusion Detection Systems (IDS)

An Intrusion Detection System (IDS) is an application that monitors system activity and alerts on possible intrusions. IDS technologies are vital for monitoring systems and networks to identify indications of malicious activity. Depending on where you set up an IDS, it can be either host-based or network-based.

### Host-based Intrusion Detection System (HIDS)

A Host-based Intrusion Detection System (HIDS) is an application installed on a host (an endpoint such as a computer or server) that monitors the activity on that specific host. HIDS are typically installed on all endpoints to detect security threats. They monitor internal activities on the host, such as unauthorized application installations, and generate alerts when something unusual is detected. HIDS can also monitor file systems, system resource usage, and user activity.

### Network-based Intrusion Detection System (NIDS)

A Network-based Intrusion Detection System (NIDS) monitors network traffic and data by inspecting traffic from various devices across the network. NIDS software is installed on devices located at specific points in the network. When malicious network traffic is detected, NIDS logs the activity and generates an alert. Using a combination of HIDS and NIDS provides a multi-layered approach to intrusion detection, offering a comprehensive view of network and host activities.

## Detection Techniques

Detection systems employ different techniques to identify threats and attacks. The two most common techniques used by IDS technologies are signature-based analysis and anomaly-based analysis.

### Signature-based Analysis

**Signature-based analysis** is a detection method that relies on predefined patterns (signatures) associated with known malicious activities. Signatures can include patterns like binary sequences, specific IP addresses, or malicious scripts.

- **Advantages:**
  - **Low rate of false positives**: This method is efficient at detecting known threats because it compares activity directly to known signatures, leading to fewer false positives.
- **Disadvantages:**
  - **Evasion**: Attackers can modify their behaviors or malware code to bypass detection by altering the signature.
  - **Need for updates**: The signature database requires constant updates as new threats are discovered.
  - **Inability to detect unknown threats**: This method is ineffective against unknown threats like zero-day attacks.

### Anomaly-based Analysis

**Anomaly-based analysis** is a detection method that identifies abnormal behavior by comparing current activity against a baseline of normal or expected behavior. This technique has two phases:

- **Training phase**: A baseline of normal system behavior is established by collecting data.
- **Detection phase**: Current system activity is compared against the baseline, and deviations are logged and alerted.

- **Advantages:**
  - **Detection of new and evolving threats**: This method can identify previously unknown threats that signature-based systems may miss.
- **Disadvantages:**
  - **High rate of false positives**: Non-malicious deviations from the baseline can be incorrectly flagged as threats.
  - **Risk of pre-existing compromise**: If an attacker is present during the training phase, their behavior may be included in the baseline, leading to missed detections.

## Key Takeaways

IDS technologies are crucial tools in the cybersecurity arsenal. A NIDS monitors network activity, while a HIDS monitors individual endpoints. IDS technologies generate alerts based on their detection techniques, such as signature-based or anomaly-based analysis, to identify and respond to potential security incidents.