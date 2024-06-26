# Brute Force Attacks and OS Hardening

In this reading, you’ll learn about brute force attacks, how vulnerabilities can be assessed using virtual machines and sandboxes, and ways to prevent brute force attacks using a combination of authentication measures. Implementing various OS hardening tasks can help prevent brute force attacks. An attacker can use a brute force attack to gain access and compromise a network.

## Brute Force Attacks

### Definition
A brute force attack is a trial-and-error process of discovering private information by guessing passwords or encryption keys. Attackers use various techniques to guess passwords, including simple brute force attacks and dictionary attacks.

### Types of Brute Force Attacks
- **Simple Brute Force Attacks**: Attackers guess a user's login credentials by entering combinations of usernames and passwords until they find one that works.
- **Dictionary Attacks**: Attackers use a list of commonly used passwords and stolen credentials from previous breaches to access a system. This method is named because it originally used words from the dictionary to guess passwords.

### Tools Used in Brute Force Attacks
- **Automated Software Tools**: Attackers often use automated tools to speed up the process of guessing passwords and reduce the time and effort involved in brute force attacks.

## Assessing Vulnerabilities

### Virtual Machines (VMs)
- **Definition**: VMs are software versions of physical computers that provide an isolated environment for running code.
- **Uses**: VMs are useful for testing potentially malicious code, investigating infected machines, and running malware in a constrained environment. VMs can be deleted and replaced with a pristine image after testing.
- **Risks**: There is a small risk that malicious programs can escape virtualization and access the host machine.

### Sandbox Environments
- **Definition**: A sandbox is a testing environment that allows software or programs to be executed separately from the network.
- **Uses**: Sandboxes are used for testing patches, identifying bugs, detecting cybersecurity vulnerabilities, and simulating attack scenarios.
- **Risks**: Some malware can detect if it is running in a VM or sandbox environment and behave harmlessly, making detection more challenging.

## Prevention Measures

### Salting and Hashing
- **Hashing**: Converts information into a unique value that cannot be decrypted to obtain the original text.
- **Salting**: Adds random characters to hashed passwords to increase their length and complexity, making them more secure.

### Multi-Factor Authentication (MFA) and Two-Factor Authentication (2FA)
- **MFA**: Requires a user to verify their identity using a combination of authentication factors such as passwords, fingerprints, facial recognition, or one-time passwords (OTP).
- **2FA**: A type of MFA that uses only two forms of verification.

### CAPTCHA and reCAPTCHA
- **CAPTCHA**: A test that distinguishes between humans and bots, preventing automated software from brute forcing passwords.
- **reCAPTCHA**: A free CAPTCHA service from Google that helps protect websites from bots and malicious software.

### Password Policies
- **Guidelines**: Policies include guidelines on password complexity, update frequency, reuse restrictions, and login attempt limits before account suspension.

## Key Takeaways
- **Brute Force Attacks**: A trial-and-error method of guessing passwords, which can be done manually or through software tools.
- **Assessing Vulnerabilities**: Using sandboxes and virtual machines to test suspicious files, check for vulnerabilities, and simulate attacks.
- **Prevention Measures**: Implementing salting and hashing, MFA/2FA, CAPTCHA/reCAPTCHA, and strong password policies to protect against brute force attacks.

These practices help secure systems and prevent unauthorized access through brute force attacks.