# Subnetting and CIDR

## Overview of Subnetting
- **Subnetting**: The subdivision of a network into logical groups called subnets, creating a network inside a network.
  - **Function**: Divides a network address range into smaller subnets based on IP addresses and network masks.
  - **Benefits**: 
    - Improves network efficiency.
    - Enhances security by creating security zones.
    - Keeps communications within the same subnet, improving speed and efficiency.

## Security Zones and Network Segmentation
- **Network Segmentation**: Divides a network to protect portions of it from the unsecured global network (internet).
  - **Types of Zones**:
    - **Uncontrolled Zone**: Outside the organization’s control, like the internet.
    - **Controlled Zone**: Internal network segments with specific access controls.
    - **Demilitarized Zone (DMZ)**: Contains public-facing services with access to the internet.
    - **Restricted Zone**: Protects highly confidential information within the internal network.

## Classless Inter-Domain Routing (CIDR)
- **CIDR**: A method of assigning subnet masks to IP addresses to create subnets.
  - **Classless Addressing**: Replaces the outdated classful addressing system (Class A to Class E).
  - **Format**: CIDR IP addresses include a slash (“/”) followed by a number (IP network prefix).
    - **Example**: 
      - Regular IPv4: `198.51.100.0`
      - CIDR: `198.51.100.0/24` (encompasses all IP addresses between `198.51.100.0` and `198.51.100.255`).

## Benefits of CIDR
- **Efficiency**: Reduces the number of entries in routing tables.
- **Expansion**: Provides more available IP addresses within networks.
- **Example Tool**: Online conversion tools like IPAddressGuide can be used to practice converting CIDR to IPv4 addresses and vice versa.

## Security Benefits of Subnetting
- **Bandwidth Utilization**: Uses network bandwidth more efficiently.
- **Network Performance**: Improves network performance.
- **Security**: 
  - Creates isolated subnetworks.
  - Utilizes physical isolation, routing configuration, and firewalls for enhanced security.

## Key Takeaways
- **Subnetting**: A common security strategy used to create smaller networks within a private network.
  - **Purpose**: Improves network efficiency and helps create security zones.
- **CIDR**: Expands available IP addresses and reduces routing table entries, making subnetting more efficient and scalable.

---

This structured approach to subnetting and CIDR provides a comprehensive understanding of how these methods improve network efficiency and security by segmenting networks into smaller, manageable subnets.