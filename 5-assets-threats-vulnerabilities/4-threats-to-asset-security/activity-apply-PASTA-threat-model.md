# Activity: Apply the PASTA Threat Model Framework

## Activity Overview

In this activity, you will practice using the Process of Attack Simulation and Threat Analysis (PASTA) threat model framework. You will determine whether a new shopping app is safe to launch.

## Scenario

You’re part of the growing security team at a company for sneaker enthusiasts and collectors. The business is preparing to launch a mobile app that makes it easy for their customers to buy and sell shoes. You will perform a threat model of the application using the PASTA framework, going through each of the seven stages to identify security requirements.

## Part 1 - Access the Resources

### Step 1: Access the Template

To use the template for this course item, click the following link and select *Use Template*.

[PASTA worksheet](https://docs.google.com/document/d/1u3aU6ZnWfcjzwZt79OdIwJ27dcyCZYDtmEEMivey3Os/template/preview?resourcekey=0-TAMA_2t0BCj5-BL9wG23Ng)

### Step 2: Access Supporting Materials

The following supporting materials will help you complete this activity. Keep them open as you proceed to the next steps.

- [PASTA data flow diagram](https://docs.google.com/presentation/d/1ol7y79popTFfNHM-90ES-H-i1Lpd0YNvPShxBlXozjg/template/preview?resourcekey=0-DZAkf7Vzh2PXsP-j3oXV-g)
- [PASTA attack tree](https://docs.google.com/presentation/d/1FmWLyHgmq9XQoVuMxOym2PHO8IuedCkan4moYnI-EJ0/template/preview?resourcekey=0-zYPY7AhPJdcClXamlAfOag#slide=id.p)

## Part 2 - Complete the PASTA Stages

### Step 1: Identify the Mobile App’s Business Objectives

The main goal of Stage I of the PASTA framework is to understand why the application was developed and what it is expected to do.

**Description:** Our application should seamlessly connect sellers and shoppers. It should be easy for users to sign-up, log in, and manage their accounts. Data privacy is a big concern for us. We want users to feel confident that we’re being responsible with their information.

Buyers should be able to directly message sellers with questions. They should also have the ability to rate sellers to encourage good service. Sales should be clear and quick to process. Users should have several payment options for a smooth checkout process. Proper payment handling is really important because we want to avoid legal issues.

**Stage I Notes:**
- Seamless connection between sellers and shoppers
- Easy user sign-up, login, and account management
- High priority on data privacy
- Direct messaging between buyers and sellers
- Ability for buyers to rate sellers
- Multiple payment options for smooth checkout
- Proper payment handling to avoid legal issues

### Step 2: Evaluate the App’s Components

In Stage II, the technological scope of the project is defined. Evaluate the application's architecture for security risks.

**Technologies Used:**
- **API**: Adds functionality without programming from scratch, but could be a point of entry for attackers.
- **PKI (AES and RSA)**: Ensures encrypted data exchange, but if not implemented properly, can lead to data breaches.
- **SHA-256**: Protects sensitive user data, but if compromised, can lead to exposure of hashed information.
- **SQL**: Manages data interactions, but susceptible to SQL injection attacks if not properly sanitized.

**Stage II Notes:**
- Prioritize API for evaluation due to its role in integrating various functions, which could introduce vulnerabilities if not properly secured.
- PKI and encryption methods need thorough assessment to ensure secure key exchange and data encryption.
- Evaluate SHA-256 hashing implementation to ensure data integrity.
- SQL must be scrutinized for injection vulnerabilities.

### Step 3: Review a Data Flow Diagram

Analyze how the application handles information. Break down each process, such as allowing buyers to search the database for shoes.

**Stage III Notes:**
- Ensure APIs securely manage data exchange.
- Validate encryption protocols in the data flow diagram.
- Confirm secure SQL queries to prevent injection attacks.

### Step 4: Use an Attacker Mindset to Analyze Potential Threats

Identify potential threats to the application and the processes in the data flow diagram.

**Stage IV Notes:**
- Virus attacks on the authentication system.
- Social engineering attacks targeting employees.

### Step 5: List Vulnerabilities That Can Be Exploited by Those Threats

Consider the attack surface of the technologies listed in Stage II.

**Stage V Notes:**
- Unencrypted data on payment forms.
- Unsanitized inputs leading to SQL injection attacks.

### Step 6: Map Assets, Threats, and Vulnerabilities to an Attack Tree

Use the information gathered to build an attack tree.

**Stage VI Notes:**
- Map SQL injection attacks targeting payment forms.
- Include virus attack vectors on authentication systems.

### Step 7: Identify New Security Controls That Can Reduce Risk

Implement defenses and safeguards to mitigate threats.

**Stage VII Notes:**
- Implement strong API security measures.
- Use encrypted connections (SSL/TLS) for data transfer.
- Enforce strong password policies and multi-factor authentication (MFA).
- Regularly update and patch systems to protect against known vulnerabilities.