# Query for Events with Chronicle

- **Chronicle Overview**: Chronicle is a SIEM tool that allows users to search and filter log data using the YARA-L language, which is designed for creating rules to detect specific activities within ingested log data.

- **Search Methods**:

  - **UDM (Unified Data Model) Search**: Default search method that searches through normalized data, making it easier to locate specific events.
  - **Raw Log Search**: Used to search through logs that have not been normalized, useful when data might not have been fully included in the normalized logs or to troubleshoot ingestion problems.

- **UDM Search Example**:

  - Search Query

    : 

    ```
    metadata.event_type = "USER_LOGIN" AND security_result.action = "BLOCK"
    ```

    - **metadata.event_type**: Specifies the type of event, in this case, a user login.
    - **security_result.action**: Specifies the security action, with "BLOCK" indicating a failed or blocked login attempt.

  - Search Results

    :

    - **Timeline Bar Graph**: Visualizes failed login events over time, helping to identify patterns.
    - **List of Events**: Includes timestamps and associated assets (e.g., device names), providing detailed context for each event.

- **Quick Filters**: Located on the left side of the interface, Quick Filters allow users to further refine their search results. For example, filtering by `target.ip` lets you focus on events related to specific IP addresses.

- **Practical Application**: This search capability helps in quickly identifying security incidents, analyzing failed login attempts, and narrowing down results to specific data points, such as IP addresses, for more efficient investigations.