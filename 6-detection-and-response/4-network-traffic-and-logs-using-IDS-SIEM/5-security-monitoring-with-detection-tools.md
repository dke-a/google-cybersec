# Security Monitoring with Detection Tools

Detection requires data from various data sources, and different detection technologies monitor devices and log various types of system activity, like network and endpoint telemetry.

## Telemetry

Telemetry refers to the collection and transmission of data for analysis. While logs record events on systems, telemetry describes the data itself. For example, packet captures are considered network telemetry. Logs and telemetry serve as sources of evidence for security professionals during investigations.

## Intrusion Detection Systems (IDS)

An Intrusion Detection System (IDS) is an application that monitors activity and alerts on possible intrusions. It monitors different parts of a system or network, including endpoints and networks.

### Endpoint Monitoring

- **Endpoint**: Any device connected to a network, such as laptops, tablets, desktops, or smartphones. Endpoints are key targets for malicious actors as they serve as entry points into a network.
- **Host-based Intrusion Detection System (HIDS)**: An application installed as an agent on a single host (e.g., a laptop or server) to monitor the host's activity. HIDS detects suspicious activity, records output as logs, and generates alerts when something unusual is detected.

### Network Monitoring

- **Network-based Intrusion Detection System (NIDS)**: A system that collects and analyzes network traffic and data. NIDS works similarly to packet sniffers, monitoring network traffic at specific points in the network.
- Multiple IDS sensors can be deployed across the network to ensure adequate visibility. When suspicious or unusual network activity is detected, NIDS logs it and generates an alert.

## Detection Methods

### Signature Analysis

- **Signature Analysis**: A detection method used by IDS to find events of interest based on predefined rules (signatures). If monitored activity matches the rules in the signature, the IDS logs it and sends out an alert.
- Example: A signature can be configured to generate an alert if three consecutive failed login attempts occur, indicating a potential password attack.

### IDS Logs

- IDS technologies record the information of the devices, systems, and networks they monitor as IDS logs. These logs can be sent, stored, and analyzed in a centralized log repository like a Security Information and Event Management (SIEM) system.

## Key Takeaways

Security monitoring with detection tools involves gathering and analyzing data from various sources, such as endpoints and networks, to detect and respond to potential security threats. Intrusion Detection Systems (IDS) play a crucial role in this process by monitoring activity and generating alerts based on detection methods like signature analysis.