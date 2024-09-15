# Components of a Detection Signature

As a security analyst, you may be tasked with writing, customizing, or testing signatures using IDS tools. Signatures are crucial for specifying detection rules, which outline the types of network intrusions you want an IDS (Intrusion Detection System) to detect. A typical IDS signature consists of three primary components: action, header, and rule options. Understanding these components will enable you to read and create effective detection signatures.

## Action

The **action** is the first item specified in a signature and determines what the IDS should do if the rule criteria are met. Actions vary across different NIDS (Network Intrusion Detection System) rule languages, but common actions include:

- **alert**: Generates an alert if the rule criteria are met.
- **pass**: Ignores the traffic that matches the rule.
- **reject**: Rejects the traffic and sends a notification.

For example, if a rule specifies to alert on suspicious network traffic that establishes an unusual connection to a port, the IDS will inspect the traffic packets and send out an alert if the conditions are met.

## Header

The **header** of the signature defines the network traffic that the signature applies to. This includes details such as:

- **Source and destination IP addresses**: Identifies the origin and target of the traffic.
- **Source and destination ports**: Specifies the ports used by the traffic.
- **Protocols**: Indicates the protocol (e.g., TCP, UDP) used by the traffic.
- **Traffic direction**: Shows the direction in which the traffic is flowing.

### Example of a Header

A typical header might look like this:

`TCP 10.120.170.17 any -> 133.113.202.181 80`

In this example:
- **TCP** is the protocol.
- **10.120.170.17** is the source IP address.
- **any** indicates any source port.
- **->** represents the direction of traffic from the source to the destination.
- **133.113.202.181** is the destination IP address.
- **80** is the destination port.

## Rule Options

**Rule options** allow you to customize the signature with additional parameters, helping to refine the detection process. These options can include:

- **msg**: Specifies the alert message text.
- **sid**: Stands for Signature ID, which assigns a unique identifier to each signature.
- **rev**: Indicates the revision number of the signature, which changes with each update.

### Example of Rule Options

Rule options are typically enclosed in parentheses and separated by semi-colons:

`(msg: "This is a message."; sid:1001; rev:1;)`

In this example:
- **msg**: The alert will print "This is a message."
- **sid**: The unique signature ID is 1001.
- **rev**: The revision number is 1, indicating the first version of the signature.

## Key Takeaways

- **Action**: Determines what the IDS should do when the rule matches.
- **Header**: Defines the network traffic to be inspected by the signature.
- **Rule Options**: Allow for further customization and refinement of the signature.

By understanding and configuring these components, you can create effective IDS signatures that help in detecting and responding to network intrusions.