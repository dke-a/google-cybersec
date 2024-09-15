# Examine Signatures with Suricata

Previously, you explored signature-based analysis and learned how to read signatures used in network-based intrusion detection systems (NIDS). In this session, we will use an open-source signature-based IDS called Suricata to examine a signature**. Suricata is a popular NIDS technology that comes with pre-written signatures, which can be customized or supplemented with your own rules.**

## Setting Up and Navigating Suricata

On a Linux machine running Ubuntu, with Suricata already installed, we start by exploring its configuration files:

1. **Change Directory**: Navigate to the `/etc/suricata` directory, where all of Suricata's configuration files are located.
2. **List Directory Contents**: Use the `ls` command to list the contents of the Suricata directory. Focus on the `rules` folder, which contains pre-written signature files and is where custom signatures can also be added.
3. **Navigate to Rules Folder**: Use the `cd` command to move into the `rules` folder.
4. **List Rule Templates**: Again, use the `ls` command to list the files in this folder. You'll find rule templates for different protocols and services.

## Examining a Custom Signature

Using the `less` command, examine the `custom.rules` file:

- **Comments**: Lines starting with a `#` are comments, meant to provide context and are ignored by Suricata.
- **Example**: The first line says, "Custom rules example for HTTP connection," indicating that this file contains custom rules for HTTP connections.

### Breakdown of the Signature

1. **Action**: The first word in the signature is the action, which is `alert` in this case. This means that the signature will generate an alert when the specified conditions are met.
2. **Header**: The header specifies the protocol (HTTP), source IP address (`HOME_NET`), source port (`ANY`), and the destination IP address (`EXTERNAL_NET`) and destination port (`ANY`). The arrow `->` indicates the direction of traffic from the home network to the external network.
3. **Rule Options**: Enclosed in parentheses and separated by semicolons, these options provide additional parameters for the signature. Key options include:
   - **Message (`msg`)**: Displays "GET on wire" when the alert is triggered.
   - **Flow (`flow`)**: Indicates the direction of network traffic flow; in this case, `established`, meaning a successful connection has been made.
   - **Content (`content`)**: Specifies the content to inspect within the packet. Here, it looks for the text `GET`, which is an HTTP request method used to retrieve data from a server.

### Summary of the Signature

This signature alerts anytime Suricata detects the text `GET` in an HTTP connection from the home network going to the external network.

## Key Takeaways

- **Customization**: Every environment is different, so IDS signatures must be tested, tailored, or even created to effectively detect threats and minimize false positives.
- **Hands-On**: As a security analyst, you may be involved in testing, modifying, or creating IDS signatures to improve threat detection.

Understanding how to navigate, examine, and customize signatures in Suricata is crucial for effective network monitoring and intrusion detection.