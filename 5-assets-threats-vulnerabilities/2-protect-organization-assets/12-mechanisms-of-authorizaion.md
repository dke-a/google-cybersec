# The Mechanisms of Authorization

## Introduction
Access control is not just about authentication but also about authorization. One of the critical functions of access controls is assigning responsibility for specific systems and processes. This reading explores the mechanisms of authorization and how they work closely with authentication technologies to protect private information.

## Understanding Authorization
Authorization systems determine what authenticated users are allowed to do. They are influenced by two essential security principles:
1. **Principle of Least Privilege:** Access to information is granted only for the duration it is needed.
2. **Separation of Duties:** Users should not have levels of authorization that allow them to misuse a system, reducing the risk of system failures and inappropriate behavior.

For example, a customer service representative should not be authorized to rate their own performance. Similarly, a single person developing and testing a security system may overlook its weaknesses.

## Key Authorization Technologies
### HTTP Basic Auth
- **HTTP (Hypertext Transfer Protocol):** Establishes communications over a network.
- **Basic Auth:** Sends an identifier each time a user communicates with a webpage. It transmits usernames and passwords openly, making it vulnerable to attacks.
- **HTTPS (Hypertext Transfer Protocol Secure):** An enhanced version that secures sensitive information during transmission.

### OAuth
- **OAuth (Open-Standard Authorization Protocol):** Shares designated access between applications.
- **API Tokens:** Encrypted code blocks containing user information, such as identity and site permissions.
  

OAuth works by allowing users to authorize one service (e.g., Google) to share their profile with another application without transmitting sensitive credentials. For instance, when you use your Google account to create an account on another website, OAuth handles the authorization securely. 

## Authorization in Practice
- **Separation of Duties:** Applies to systems, networks, databases, processes, and more, ensuring that no single user has unchecked power.
- **Role-Based Authorization:** Ensures that authorization is dependent on the system or user's role.

### Example Scenario with OAuth
When you authorize a website to use your Google profile:
1. **Authentication:** Google’s usual login protocols are active, including MFA if enabled.
2. **Authorization:** OAuth sends an API token containing your identity and permissions to the third-party service.
3. **Security:** Your Google password remains secure even if the third-party service is compromised.

## Monitoring Access
In addition to controlling access, monitoring access is crucial. Monitoring helps identify unauthorized access and potential security breaches.

### Key Takeaways
- **Authorization:** Determines what authenticated users can do, following the principles of least privilege and separation of duties.
- **Technologies:** HTTP basic auth, HTTPS, and OAuth are essential authorization tools.
- **Security:** Combining secure authorization methods and monitoring access ensures robust protection of sensitive information.
