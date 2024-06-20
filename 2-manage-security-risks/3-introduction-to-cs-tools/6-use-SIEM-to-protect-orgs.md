# Use SIEM Tools to Protect Organizations

Previously, you were introduced to security information and event management (SIEM) tools and a few SIEM dashboards. You also learned about different threats, risks, and vulnerabilities an organization may experience. In this reading, you will learn more about SIEM dashboard data and how cybersecurity professionals use that data to identify a potential threat, risk, or vulnerability.

## Splunk

Splunk offers different SIEM tool options: Splunk® Enterprise and Splunk® Cloud. Both allow you to review an organization's data on dashboards. This helps security professionals manage an organization's internal infrastructure by collecting, searching, monitoring, and analyzing log data from multiple sources to obtain full visibility into an organization’s everyday operations.

### Splunk Dashboards and Their Purposes

#### Security Posture Dashboard
- **Purpose**: Designed for security operations centers (SOCs) to display the last 24 hours of an organization’s notable security-related events and trends.
- **Usage**: Security professionals can determine if security infrastructure and policies are performing as designed and monitor and investigate potential threats in real time.

#### Executive Summary Dashboard
- **Purpose**: Analyzes and monitors the overall health of the organization over time.
- **Usage**: Provides high-level insights to stakeholders, such as generating a summary of security incidents and trends over a specific period.

#### Incident Review Dashboard
- **Purpose**: Allows analysts to identify suspicious patterns that can occur in the event of an incident.
- **Usage**: Highlights higher-risk items that need immediate review and provides a visual timeline of the events leading up to an incident.

#### Risk Analysis Dashboard
- **Purpose**: Helps analysts identify risk for each risk object (e.g., a specific user, computer, or IP address).
- **Usage**: Shows changes in risk-related activity or behavior and helps prioritize risk mitigation efforts.

## Chronicle

Chronicle is a cloud-native SIEM tool from Google that retains, analyzes, and searches log data to identify potential security threats, risks, and vulnerabilities. Chronicle allows you to collect and analyze log data according to:

- A specific asset
- A domain name
- A user
- An IP address

### Chronicle Dashboards and Their Purposes

#### Enterprise Insights Dashboard
- **Purpose**: Highlights recent alerts and identifies suspicious domain names in logs, known as indicators of compromise (IOCs).
- **Usage**: Monitors login or data access attempts related to critical assets from unusual locations or devices.

#### Data Ingestion and Health Dashboard
- **Purpose**: Shows the number of event logs, log sources, and success rates of data being processed into Chronicle.
- **Usage**: Ensures log sources are correctly configured and logs are received without error, addressing log-related issues promptly.

#### IOC Matches Dashboard
- **Purpose**: Indicates the top threats, risks, and vulnerabilities to the organization.
- **Usage**: Observes domain names, IP addresses, and device IOCs over time to identify trends and direct focus to the highest priority threats.

#### Main Dashboard
- **Purpose**: Displays a high-level summary of information related to the organization’s data ingestion, alerting, and event activity over time.
- **Usage**: Accesses a timeline of security events to identify threat trends across log sources, devices, IP addresses, and physical locations.

#### Rule Detections Dashboard
- **Purpose**: Provides statistics related to incidents with the highest occurrences, severities, and detections over time.
- **Usage**: Accesses a list of all alerts triggered by a specific detection rule and uses those statistics to manage recurring incidents and establish mitigation tactics.

#### User Sign In Overview Dashboard
- **Purpose**: Provides information about user access behavior across the organization.
- **Usage**: Accesses a list of all user sign-in events to identify unusual user activity and mitigate threats to user accounts and applications.

## Key Takeaways

SIEM tools provide dashboards that help security professionals organize and focus their security efforts. This is important because it allows analysts to reduce risk by identifying, analyzing, and remediating the highest priority items in a timely manner. Later in the program, you’ll have an opportunity to practice using various SIEM tool features and commands for search queries.