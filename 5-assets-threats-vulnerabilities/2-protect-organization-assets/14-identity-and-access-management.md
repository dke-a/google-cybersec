# Identity and Access Management

## Introduction
Security goes beyond simply combining processes and technologies to protect assets; it ensures these measures create a secure environment supporting a comprehensive defense strategy. Two fundamental security principles that limit access to organizational resources are:

- **Principle of Least Privilege:** A user is only granted the minimum level of access and authorization required to complete a task or function.
- **Separation of Duties:** Users should not be given levels of authorization that would allow them to misuse a system.

Both principles support each other. For example, under least privilege, an individual who approves IT purchases shouldn't have the authorization to approve purchases from every department. Under separation of duties, the person who can approve purchases from the IT department should be different from the person who inputs new purchases.

## Identity and Access Management (IAM)
As organizations rely more on technology, regulatory agencies demand greater proof of their efforts to prevent threats. Identity and Access Management (IAM) helps manage digital identities within an organization. Both IAM and AAA (Authentication, Authorization, and Accounting) systems authenticate users, determine their access privileges, and track their activities.

IAM ensures the right user is granted access to the right resources at the right time and for the right reasons, based on organizational policies and processes.

### Authenticating Users
To ensure the right user is attempting to access a resource, some form of proof is required. Authentication factors include:

- **Knowledge:** Something the user knows (e.g., a password).
- **Ownership:** Something the user possesses (e.g., a one-time passcode).
- **Characteristic:** Something the user is (e.g., biometric data).

Technologies like Single Sign-On (SSO) and Multi-Factor Authentication (MFA) enhance authentication processes by combining different login methods and requiring multiple forms of verification.

### User Provisioning
User provisioning involves creating and maintaining a user's digital identity. For example, when a new instructor is hired, a college might create a new user account that grants access to instructor-only resources. Security analysts are involved in both provisioning and deprovisioning users, ensuring that access rights are managed appropriately.

### Granting Authorization
Authorization ensures the right resources are made available to authenticated users. Common frameworks include:

- **Mandatory Access Control (MAC):** Based on a strict need-to-know basis, access is granted manually by a central authority. Common in government agencies.
- **Discretionary Access Control (DAC):** The data owner decides access levels, such as sharing access to a Google Drive folder.
- **Role-Based Access Control (RBAC):** Authorization is based on a user's role within the organization. For example, a marketing user may access user analytics but not network administration.

### Access Control Technologies
Access control technologies automate and streamline the authentication and authorization process, reducing errors and risks. Organizations may develop custom access control systems or opt for third-party solutions that offer comprehensive tools for securing information systems.

## Key Takeaways
Controlling access involves a collection of systems and tools. IAM and AAA frameworks implement least privilege and separation of duties. As a security analyst, you may be responsible for user provisioning and collaborating with IAM or AAA teams. Familiarity with these models helps organizations achzXieve their security objectives, ensuring the right user is granted access to the right resources at the right time and for the right reasons.

## Resources for More Information
The identity and access management industry is rapidly growing. Staying informed is crucial.

- **IDPro:** A professional organization dedicated to sharing essential IAM industry knowledge.