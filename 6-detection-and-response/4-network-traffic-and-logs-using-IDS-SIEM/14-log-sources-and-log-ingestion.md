# Log Sources and Log Ingestion

This session focused on the significance of log ingestion in the context of Security Information and Event Management (SIEM) tools, which are essential for monitoring and analyzing critical activities within an organization.

## SIEM Process Overview

The SIEM process involves three main steps:

1. **Collect and Aggregate Data**:
   - SIEM tools collect event data from various sources across the network.
   - These sources can include servers, network devices, applications, and more.
2. **Normalize Data**:
   - Collected data is normalized, meaning it is transformed into a standard format.
   - Normalization ensures consistency in data structure, making it easier to read, search, and analyze.
   - It’s important to note that not all SIEM tools have the same capabilities for data normalization.
3. **Analyze Data**:
   - After normalization, the data is analyzed and correlated by the SIEM tool.
   - This analysis helps identify patterns that may indicate unusual or malicious activity.

## Log Ingestion

Log ingestion is the process by which SIEM tools collect and import data from various log sources. This process is crucial for the effective functioning of SIEM tools.

### How Log Ingestion Works:

- **Data Collection**: SIEM tools create a copy of event data received from log sources and store it within their own database. This allows the tool to analyze and process the data without altering the original logs.
- **Centralized Analysis**: By centralizing log data, SIEM tools provide a unified platform for security analysts to investigate incidents and respond effectively.

### Log Forwarders

Log forwarders are commonly used to automate the process of collecting and sending log data to SIEM tools.

- Native vs. Third-Party Forwarders

  :

  - Some operating systems come with native log forwarders.
  - In the absence of native forwarders, third-party software can be installed and configured to perform this task.

- Configuration

  :

  - Log forwarders are configured to specify which logs to forward and to which SIEM tool.
  - Once forwarded, the SIEM tool processes and normalizes the data, making it easier to search and analyze.

**Note**: Many SIEM tools have their own proprietary log forwarders, but they can also integrate with open-source alternatives.

## Key Takeaways

- **Data Ingestion is Vital**: SIEM tools rely on data to function effectively. Understanding how log sources are ingested is crucial for identifying and responding to security incidents.
- **Configuration Skills**: As a security analyst, you may need to configure SIEM tools to collect log data, making this knowledge essential for your career.

## Resources for Further Learning

- [Guide on getting data into Splunk](https://docs.splunk.com/Documentation/SplunkCloud/9.0.2303/Data/Howdoyouwanttoadddata)
- [Guide on data ingestion into Chronicle](https://cloud.google.com/chronicle/docs/data-ingestion-flow)

**Pro Tip**: You’ll use Splunk Cloud later in this module for hands-on practice, including uploading data, performing searches, and answering related questions.