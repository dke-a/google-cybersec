# Cryptography and Cloud Security

## Introduction
Cloud networks need to be secured through a mixture of security hardening practices and cryptography, similar to on-premise networks. This reading will cover common cloud security hardening practices, considerations for implementing cloud security measures, and the fundamentals of cryptography.

## Cloud Security Hardening
Various techniques and tools are used to secure cloud network infrastructure and resources. Common cloud security hardening techniques include:

### Identity Access Management (IAM)
- **Definition**: A collection of processes and technologies that help organizations manage digital identities and authorize user access to cloud resources.
- **Importance**: Ensures only authorized users can access critical cloud operations.

### Hypervisors
- **Type One Hypervisors**: Run on the hardware of the host computer (e.g., VMware's ESXi).
- **Type Two Hypervisors**: Operate on the software of the host computer (e.g., VirtualBox).
- **Role of CSPs**: CSPs manage hypervisors and ensure regular patches and updates. Vulnerabilities or misconfigurations can lead to VM escapes.

### Baselining
- **Definition**: Establishing a fixed reference point to compare changes made to a cloud environment.
- **Examples**: Restricting access to the admin portal, enabling password management, file encryption, and threat detection services for SQL databases.

### Cryptography in the Cloud
- **Encryption**: The process of converting information into ciphertext, unreadable without the encryption key. Modern encryption relies on the secrecy of the key rather than the algorithm.
- **Importance**: Provides data integrity and confidentiality, securing sensitive data in the cloud.

### Cryptographic Erasure
- **Definition**: Erasing the encryption key used to encrypt data, making the data undecipherable.
- **Method**: Crypto-shredding destroys all copies of the key to prevent future data access.

## Key Management
Modern encryption relies on secure key management. Measures to protect data include:

### Trusted Platform Module (TPM)
- **Definition**: A computer chip that securely stores passwords, certificates, and encryption keys.

### Cloud Hardware Security Module (CloudHSM)
- **Definition**: A computing device that provides secure storage for cryptographic keys and processes cryptographic operations.

### CSPs and Key Management
- **Audits and Security Reports**: Organizations can request audits and security reports from CSPs.
- **Customer Responsibility**: Customers can provide their own encryption keys and are responsible for keeping them confidential.

## Shared Responsibility Model
- **Definition**: CSPs are responsible for securing cloud infrastructure, while organizations are responsible for securing assets and processes in the cloud.
- **Importance**: Ensures clear boundaries of responsibility between CSPs and customers.

## Key Takeaways
- **Cloud Security Hardening**: Critical for securing public cloud environments and improving organizational security.
- **Techniques**: Include IAM, baselining, securing hypervisors, cryptography, and cryptographic erasure.
- **Shared Responsibility**: Both CSPs and customers have defined roles in maintaining cloud security.

Understanding these aspects of cloud security helps organizations better protect their cloud infrastructure and maintain a secure environment for their data and applications.