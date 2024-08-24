# Investigating Packet Details with Wireshark

---

## **Introduction**

As a security analyst, analyzing packets is crucial for identifying suspicious activities on a network. Wireshark is a powerful tool that can help you dive deep into packet captures (p-caps) and filter the data to focus on what's most relevant to your investigation.

---

## **Understanding IPv4 and IPv6 Headers**

### **IPv4 Header Fields**
- **Version**: Indicates the IP version, which is IPv4.
- **Internet Header Length (IHL)**: Specifies the length of the IPv4 header.
- **Type of Service (ToS)**: Provides information about packet priority.
- **Total Length**: Indicates the total length of the entire IP packet.
- **Identification**: Identifies fragments of an original IP packet for reassembly.
- **Flags**: Provides information about packet fragmentation.
- **Fragment Offset**: Identifies the sequence of fragments.
- **Time to Live (TTL)**: Limits the packet’s lifespan on the network.
- **Protocol**: Specifies the protocol used for the packet’s data.
- **Header Checksum**: Provides error-checking for the header.
- **Source Address**: Specifies the sender’s IP address.
- **Destination Address**: Specifies the receiver’s IP address.
- **Options**: Optional field for applying security options.

### **IPv6 Header Fields**
- **Version**: Indicates the IP version, which is IPv6.
- **Traffic Class**: Similar to ToS in IPv4; it prioritizes packets.
- **Flow Label**: Identifies packets in a sequence.
- **Payload Length**: Specifies the length of the packet's data.
- **Next Header**: Indicates the type of header following the IPv6 header.
- **Hop Limit**: Similar to TTL in IPv4; limits packet travel time.
- **Source Address**: Specifies the sender’s IP address.
- **Destination Address**: Specifies the receiver’s IP address.

---

## **Using Wireshark for Packet Analysis**

### **Wireshark Overview**
Wireshark is an open-source network protocol analyzer with a graphical user interface (GUI) that allows you to visualize network communications and analyze packets in detail.

### **Display Filters**
Display filters in Wireshark help you focus on specific packets by filtering out unnecessary data. You can filter by protocols, IP addresses, ports, and more.

### **Comparison Operators**
Wireshark supports several comparison operators to refine your filters:

| **Operator Type**        | **Symbol** | **Abbreviation** |
| ------------------------ | ---------- | ---------------- |
| Equal                    | **==**     | eq               |
| Not equal                | **!=**     | ne               |
| Greater than             | **>**      | gt               |
| Less than                | **<**      | lt               |
| Greater than or equal to | **>=**     | ge               |
| Less than or equal to    | **<=**     | le               |

**Example**: To filter packets from IP address `192.168.1.1`:
```plaintext
ip.src == 192.168.1.1
```

### **Common Filters**

- **Protocols**: Filter by protocol type, e.g., `dns`, `http`, `ftp`.

- **IP Address**: Filter by specific IP addresses:

  - **Source IP**: `ip.src == 10.10.10.10`
  - **Destination IP**: `ip.dst == 4.4.4.4`

- **MAC Address**: Filter by MAC address:

  ```
  eth.addr == 00:70:f4:23:18:c4
  ```

- **Ports**: Filter by port number:

  - **UDP**: `udp.port == 53`
  - **TCP**: `tcp.port == 25`

### **Follow Streams**

Wireshark allows you to follow streams (conversations) for specific protocols. This feature reassembles data exchanges into a readable format, which is useful for analyzing the content of communications, such as HTTP request and response messages.

------

## **Key Takeaways**

- **Packet Analysis**: Mastering packet analysis is essential for cybersecurity professionals. Wireshark’s display filters are powerful tools that allow you to isolate and investigate specific network activities.
- **Ongoing Skill Development**: As you continue your cybersecurity journey, practice using tools like Wireshark to deepen your understanding of network traffic and improve your ability to detect and respond to security incidents.

------

## **Resources**

- Explore the full features and capabilities of Wireshark in the [Wireshark Official User Guide](https://www.wireshark.org/docs/wsug_html/).