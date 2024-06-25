# IP Addresses and Network Communication

## Overview
IP addresses play a crucial role in network communication. They serve as unique identifiers for devices on a network, similar to how a mailing address identifies a house on a street. This section explores the types of IP addresses, their format, and their role in network communication.

## Types of IP Addresses
### IPv4
- **Format**: Written as four sets of 1, 2, or 3-digit numbers separated by decimal points (e.g., 192.168.0.1).
- **Usage**: Initially used for all internet communication.
- **Limitation**: Limited number of addresses, leading to the development of IPv6.

### IPv6
- **Format**: Composed of 32 characters (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).
- **Usage**: Developed to accommodate the growing number of internet-connected devices.
- **Advantage**: Allows for a significantly larger number of unique addresses compared to IPv4.

## Public vs. Private IP Addresses
### Public IP Addresses
- **Assignment**: Assigned by your Internet Service Provider (ISP).
- **Visibility**: Visible to the entire internet.
- **Shared Usage**: All devices on a local network share the same public-facing IP address, similar to how all roommates in a house share the same mailing address.

### Private IP Addresses
- **Usage**: Used within a local network.
- **Visibility**: Only visible to other devices on the same local network.
- **Communication**: Allows devices on the same local network to communicate with each other using unique IP addresses not visible to the rest of the internet.

## MAC Addresses
- **Definition**: A MAC (Media Access Control) address is a unique alphanumeric identifier assigned to each physical device on a network.
- **Function**: Used by network switches to map devices to specific ports.
- **Example**: When a switch receives a data packet, it reads the MAC address of the destination device and uses its MAC address table to direct the packet to the appropriate port.

## Key Takeaways
- **IP Addresses**: Serve as unique identifiers for devices on a network.
- **IPv4 and IPv6**: Two types of IP addresses, with IPv6 developed to address the limitations of IPv4.
- **Public vs. Private IPs**: Public IPs are visible to the entire internet, while private IPs are only visible within a local network.
- **MAC Addresses**: Unique identifiers for physical devices on a network, used by switches to direct data packets.

Understanding the roles and differences between IP and MAC addresses is fundamental for network communication and security.