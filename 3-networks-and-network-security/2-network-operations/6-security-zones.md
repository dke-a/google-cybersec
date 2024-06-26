# Security Zones

## Introduction to Security Zones
- **Security Zones**: Segments of a network designed to protect the internal network from external threats, such as the internet.
- **Network Segmentation**: The practice of dividing a network into segments, each with its own access permissions and security rules.
  - **Purpose**: To control who can access different segments, maintain privacy within corporate groups, and prevent issues from spreading across the network.
  - **Example**: A hotel offering free public Wi-Fi has an unsecured guest network separate from an encrypted staff network.

## Types of Security Zones
- **Uncontrolled Zone**: Networks outside the organization's control, like the internet.
- **Controlled Zone**: Subnets within the organization that protect the internal network from the uncontrolled zone.

### Subnetworks (Subnets)
- **Subnets**: Smaller networks within an organization's network, providing privacy for different departments.
  - **Example**: At a university, separate subnets for faculty and students to isolate contamination and protect the overall network.

### Types of Networks within the Controlled Zone
1. **Demilitarized Zone (DMZ)**
   - **Location**: Outer layer of the controlled zone.
   - **Functions**: Contains public-facing services accessible from the internet.
     - **Components**: Web servers, proxy servers, DNS servers, email servers, file servers.
   - **Purpose**: Acts as a network perimeter to protect the internal network.
   
2. **Internal Network**
   - **Location**: Inside the DMZ.
   - **Functions**: Contains private servers and sensitive data.
   
3. **Restricted Zone**
   - **Location**: Inside the internal network.
   - **Functions**: Protects highly confidential information.
   - **Access**: Only accessible to employees with specific privileges.

## Structure of Security Zones
- **DMZ Placement**: Ideally situated between two firewalls.
  - **First Firewall**: Filters traffic entering the DMZ from the uncontrolled zone.
  - **Second Firewall**: Filters traffic entering the internal network from the DMZ.
  - **Restricted Zone Firewall**: Additional firewall for the restricted zone.

### Benefits
- **Multi-layer Defense**: Ensures multiple layers of protection:
  - Attacks penetrating the DMZ cannot easily reach the internal network.
  - Attacks penetrating the internal network cannot access the restricted zone.

## Role of Security Analysts
- **Access Control Policies**: Regulate access control policies on firewalls.
- **Traffic Control**: Restrict IPs and ports to control traffic reaching the DMZ and internal network.
  - **Example**: Allow only HTTPS traffic to access web servers in the DMZ.

## Key Takeaways
- **Importance**: Security zones are crucial for securing networks, especially in large organizations.
- **Essential Knowledge**: Understanding security zones and their functions is essential for security analysts.

This structured approach to understanding security zones provides a comprehensive view of how network segmentation and security zones protect an organization's network from external and internal threats.