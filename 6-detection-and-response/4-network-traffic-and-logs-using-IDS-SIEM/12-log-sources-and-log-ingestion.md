# Log Sources and Log Ingestion

In this reading, you’ll explore the importance of log ingestion in the context of security information and event management (SIEM) tools. Understanding how log sources are ingested into SIEM tools is crucial for security analysts to identify, prioritize, and respond to security incidents.

## SIEM Process Overview

Previously, we covered the SIEM process, which consists of three key steps:

1. **Collect and Aggregate Data**: SIEM tools gather event data from various sources within an organization's environment.
2. **Normalize Data**: The collected data is normalized to a standard format, making it easier to read, search, and analyze. It's important to note that SIEM tools differ in their data normalization capabilities.
3. **Analyze Data**: After normalization, SIEM tools analyze and correlate the data to detect patterns that may indicate unusual or malicious activity.

This reading focuses on the first step—data collection and aggregation.

## Log Ingestion

Data is essential for SIEM tools to function effectively. SIEM tools must first collect data using a process called **log ingestion**. Log ingestion involves collecting and importing data from log sources, such as servers, into a SIEM tool. This process creates a copy of the event data, which is retained in the SIEM’s storage for analysis and processing, while the original logs remain unmodified.

The event data collected includes critical activities like authentication attempts, network activity, and more, providing a centralized platform for security analysts to analyze and respond to incidents.

### Log Forwarders

There are multiple ways for SIEM tools to ingest log data. While data can be manually uploaded, this method is often inefficient and time-consuming, especially in environments with thousands of systems and devices. To streamline this process, organizations often use **log forwarders**.

**Log Forwarders** are software tools that automate the collection and transmission of log data to a SIEM tool. Some operating systems come with native log forwarders, while others require the installation of third-party log forwarding software. After installation, the software is configured to specify which logs to forward and where to send them, such as to a SIEM tool for further processing and analysis.

**Note**: Many SIEM tools come with their proprietary log forwarders, but they can also integrate with open-source log forwarders. The choice of log forwarder depends on factors such as system requirements, compatibility with existing infrastructure, and specific organizational needs.

## Key Takeaways

SIEM tools rely on data to perform effectively. As a security analyst, you will use SIEM tools to access events and analyze logs during incident investigations. You may also be tasked with configuring a SIEM to collect log data. Understanding how data is ingested into SIEM tools is critical, as it helps you identify log sources and the origins of security incidents.

## Resources

If you’d like to learn more about the log ingestion process for specific SIEM tools, here are some resources:

- [Guide on getting data into Splunk](https://docs.splunk.com/Documentation/SplunkCloud/9.0.2303/Data/Howdoyouwanttoadddata)
- [Guide on data ingestion into Chronicle](https://cloud.google.com/chronicle/docs/data-ingestion-flow)

**Pro Tip:** Later in this module, you'll use Splunk Cloud to upload data, perform basic searches, and answer questions. Follow the instructions in the [Follow-along guide for Splunk sign-up](https://www.coursera.org/learn/detection-and-response/supplement/Wg478/follow-along-guide-for-splunk-sign-up) to get started with Splunk. The verification email might take some time to arrive, so consider signing up now!