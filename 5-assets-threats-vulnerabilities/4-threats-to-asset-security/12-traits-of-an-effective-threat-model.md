# Traits of an Effective Threat Model

**Threat modeling** is the process of identifying assets, their vulnerabilities, and how each is exposed to threats. It combines various security activities, such as:

- Vulnerability management
- Threat analysis
- Incident response

## Why Application Security Matters

Applications are essential for many organizations' success, facilitating global connections and data exchange. Key points include:

- **Web-based applications**: Connect users with businesses and partners.
- **Mobile applications**: Primary method for data exchange via smartphones.

### Example
- **Log4Shell vulnerability (CVE-2021-44228)**: A critical Java-based logging library vulnerability allowing remote code execution, potentially impacting millions of devices.

## Defending the Application Layer

Proper testing is required to uncover weaknesses. **Threat modeling** is a primary method to ensure applications meet security requirements. This is typically performed by a **DevSecOps team** (Development, Security, Operations).

### Threat Modeling Process Cycle

1. **Define the scope**
2. **Identify threats**
3. **Characterize the environment**
4. **Analyze threats**
5. **Mitigate risks**
6. **Evaluate findings**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/jcxiyXGsSgiFzXVKEA2MlA_e5fb4921773047658ae29b53532617f1_IkNCZRnA8vFZL9bPa3yahdiNcz5YvwZzxcn1GyvaYWkF00CzvIWq3MkCyR_IgzOSs5bKO7iIiROjznDNMHk60Cun_ZP-OriA0rGw7gQqWHj-jiTAFPzddosn0AJ9zQxySZuHVXi856Oqf1ZWNZBt34U?expiry=1721692800000&hmac=SFFZAUPMiMmcxUSR-_EDrVFppT27BHbzfAduLt6A9DQ)

**Note:** Threat modeling should be incorporated at every stage of the Software Development Lifecycle (SDLC).

## Common Threat Modeling Frameworks

### **STRIDE**

Developed by Microsoft, used to identify vulnerabilities in six attack vectors:
- **Spoofing**
- **Tampering**
- **Repudiation**
- **Information Disclosure**
- **Denial of Service (DoS)**
- **Elevation of Privilege**

### **PASTA (Process of Attack Simulation and Threat Analysis)**

Risk-centric, evidence-based design focusing on:
- Discovering viable threats
- Representing threats as a model
- Incorporating security artifacts

### **Trike**

Open-source methodology focusing on:
- Security permissions
- Application use cases
- Privilege models

### **VAST (Visual, Agile, and Simple Threat)**

Part of ThreatModeler® platform, used for automating threat modeling assessments.

## Participating in Threat Modeling

Performed by experienced security professionals, often involves collaboration. 

### Key Questions to Ask

- What are we working on?
- What kinds of things can go wrong?
- What are we doing about it?
- Have we addressed everything?
- Did we do a good job?

## Key Takeaways

- **Application Security**: Essential due to the reliance on software in daily lives.
- **Threat Modeling**: Main method to ensure data privacy and security controls.
- **Collaboration**: Effective threat modeling requires teamwork and asking the right questions.

Building threat modeling skills involves practice, critical thinking, and applying an attacker mindset.