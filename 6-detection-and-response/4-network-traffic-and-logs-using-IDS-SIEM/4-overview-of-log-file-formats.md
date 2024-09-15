# Overview of Log File Formats

Logs record events that happen on a network or system. In security, logs provide key details about activities across an organization, such as who signed into an application at a specific time. As a security analyst, you will use **log analysis** to examine logs and identify events of interest. It’s crucial to understand different log formats to uncover key details and identify unusual or malicious activity. The following log formats are covered in this reading:

- JSON
- Syslog
- XML
- CSV
- CEF

## JavaScript Object Notation (JSON)

JavaScript Object Notation (JSON) is a lightweight, easy-to-read format used to store and transmit data, particularly in web technologies and cloud environments. JSON uses components such as:

- **Key-value pairs**: e.g., **"Alert": "Malware"**
- **Commas**: e.g., **"Alert": "Malware", "Alert code": 1090, "severity": 10**
- **Double quotes**: Used for strings, e.g., **"Alert": "Malware"**
- **Curly brackets**: Enclose objects, e.g., **"User": {"id": "1234", "name": "user", "role": "engineer"}**
- **Square brackets**: Enclose arrays, e.g., **["Administrators", "Users", "Engineering"]**

## Syslog

Syslog is a standard for logging and transmitting data, often used in Unix® systems. It serves as a:

1. **Protocol**: Transports logs to a centralized server, using ports 514 (plaintext) and 6514 (encrypted).
2. **Service**: Consolidates logs from multiple sources.
3. **Log format**: Consists of a header, structured-data, and a message.

### Syslog Log Example

**<236>1 2022-03-21T01:11:11.003Z virtual.machine.com evntslog - ID01 [user@32473 iut="1" eventSource="Application" eventID="9999"] This is a log entry!**

- **Header**: Contains timestamp, hostname, application name, and message ID.
- **Structured-data**: Includes key-value pairs, e.g., **[user@32473 iut="1" eventSource="Application" eventID="9999"]**.
- **Message**: Provides detailed information about the event.

## XML (eXtensible Markup Language)

XML is a language and format used for storing and transmitting data, native to Windows systems. XML uses:

- **Tags**: Enclose data, e.g., **<tag>data</tag>**
- **Elements**: Combine data and tags, e.g., **<Event><EventID>4688</EventID><Version>5</Version></Event>**
- **Attributes**: Provide additional information within tags, e.g., **<Data Name='SubjectUserSid'>S-2-3-11-160321</Data>**

## CSV (Comma Separated Value)

CSV uses commas to separate data values. Field names might not be included, so understanding the source device's logging structure is essential.

Example: **2009-11-24T21:27:09.534255,ALERT,192.168.2.7, 1041,x.x.250.50,80,TCP,ALLOWED,1:2001999:9,"ET MALWARE BTGrab.com Spyware Downloading Ads",1**

## CEF (Common Event Format)

CEF is a log format that uses key-value pairs to structure data. It includes fields separated by a pipe character **|**. Syslog is often used to transport CEF logs.

### CEF Log Example

**Sep 29 08:26:10 host CEF:1|Security|threatmanager|1.0|100|worm successfully stopped|10|src=10.0.0.2 dst=2.1.2.2 spt=1232**

- **Syslog Timestamp**: **Sep 29 08:26:10**
- **Syslog Hostname**: **host**
- **Version**: **CEF:1**
- **Device Vendor**: **Security**
- **Device Product**: **threatmanager**
- **Device Version**: **1.0**
- **Signature ID**: **100**
- **Name**: **worm successfully stopped**
- **Severity**: **10**
- **Extension**: e.g., **src=10.0.0.2 dst=2.1.2.2 spt=1232**

## Key Takeaways

There is no standard log format, and many different formats exist. As a security analyst, understanding and interpreting these log formats is crucial for effective incident investigation.

## Resources for More Information

- [The Syslog Protocol](https://www.rfc-editor.org/rfc/rfc5424)
- [Test Data Generator Tool](https://generatedata.com/)
- [Date and Time on the Internet: Timestamps](https://www.rfc-editor.org/rfc/rfc3339)