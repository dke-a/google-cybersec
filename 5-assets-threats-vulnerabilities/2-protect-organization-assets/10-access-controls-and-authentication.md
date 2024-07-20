# Access Controls and Authentication Systems

## Overview
Protecting data is a fundamental feature of security controls. While hashing and encryption are powerful tools, managing who or what has access to information is key to safeguarding it. The next series of controls we'll explore are access controls, which manage access, authorization, and accountability of information.

## The AAA Framework
Access control systems are commonly broken down into three functions known as the Authentication, Authorization, and Accounting (AAA) framework. Each control has its own protocols and systems that make them work. This section focuses on the first function, authentication.

### Authentication
Authentication systems serve a basic purpose: they ask anything attempting to access information, "Who are you?" Responses to this question can be based on three factors of authentication:
1. **Knowledge:** Something the user knows, such as a password or the answer to a security question.
2. **Ownership:** Something the user possesses, such as a one-time passcode (OTP) sent via text or email.
3. **Characteristic:** Something the user is, such as biometrics like fingerprint scans or facial recognition.

For authentication to be successful, the information provided must match the information on file. If the credentials match, access is granted; if not, access is denied.

### Single Sign-On (SSO)
Single Sign-On (SSO) is a technology that combines several different logins into one. It establishes a user's identity once, allowing them to gain access to company resources faster without the need to re-authenticate multiple times. However, SSO presents a significant vulnerability if used alone, as it can be compromised if it relies on just a single factor of authentication.

### Multi-Factor Authentication (MFA)
Multi-Factor Authentication (MFA) is a security measure that requires a user to verify their identity in two or more ways to access a system or network. MFA combines two or more independent credentials, such as knowledge and ownership, to prove that someone is who they claim to be. SSO and MFA are often used together to ensure convenient access that is also secure.

## Key Takeaways
- **Access Controls:** Security controls that manage access, authorization, and accountability of information.
- **Authentication:** The process of verifying the identity of a user based on knowledge, ownership, or characteristics.
- **Single Sign-On (SSO):** Combines multiple logins into one for faster access, but is vulnerable if used alone.
- **Multi-Factor Authentication (MFA):** Requires two or more forms of verification to ensure secure access.
  

Next, we'll explore the second part of the AAA framework: Authorization.