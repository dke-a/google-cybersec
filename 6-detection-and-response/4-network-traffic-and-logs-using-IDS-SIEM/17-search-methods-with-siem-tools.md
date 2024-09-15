# Search Methods with SIEM Tools

- **SIEM Overview**: Security Information and Event Management (SIEM) tools are essential for collecting and analyzing log data to monitor an organization's critical activities. As a security analyst, familiarity with different SIEM tools and their search methods is vital for effective security investigations.

## Splunk Searches

- **Search Processing Language (SPL)**: Splunk uses its proprietary SPL to search and retrieve events from indexes. SPL allows you to perform various tasks, including filtering results and transforming them into charts.

- **Basic SPL Search Example**:

  - index=main fail

    :

    - **index=main**: Retrieves events from the "main" index.
    - **fail**: Searches for events containing the term "fail."

- **Pipes in SPL**:

  - The pipe character **|** is used to chain commands together, allowing the output of one command to be used as the input for the next.
  - **Example**: `index=main fail | chart count by host` - This command retrieves events from the "main" index containing "fail" and then creates a chart based on the count of events by host.

- **Wildcard Usage**:

  - The asterisk ***** is used as a wildcard to match any character in a search term.
  - **Example**: `index=main fail*` - This expands the search to include events containing terms like "failed" or "failure."

## Chronicle Searches

- **Unified Data Model (UDM) Search**:
  - Default search method in Chronicle, used to query normalized data for faster results.
  - **Example**: `metadata.event_type = "USER_LOGIN"` - Searches for events related to user logins.
- **UDM Fields**:
  - **Entities**: Information about devices, users, or processes involved in an event.
  - **Event Metadata**: Basic event descriptions, including timestamps.
  - **Network Metadata**: Details about network-related events and protocols.
  - **Security Results**: Security outcomes, like antivirus detections.
- **Raw Log Search**:
  - Used when data isn’t found through normalized searches; searches through unparsed logs, making it slower.
  - **Pro Tip**: Supports regular expressions for more refined searches.

## Key Takeaways

- **Efficiency**: Understanding how to leverage search methods in SIEM tools like Splunk and Chronicle is crucial for quickly finding relevant event data, detecting threats, and responding to security incidents.

## Resources for More Information

- **Splunk’s Search Manual**: [Get started with SPL](https://docs.splunk.com/Documentation/Splunk/9.0.1/Search/GetstartedwithSearch)
- **Chronicle's Quickstart Guide**: [Types of Searches in Chronicle](https://cloud.google.com/chronicle/docs/review-security-alert)