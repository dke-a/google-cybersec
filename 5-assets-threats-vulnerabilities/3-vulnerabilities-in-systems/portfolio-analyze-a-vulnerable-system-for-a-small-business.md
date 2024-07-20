# Portfolio Activity: Analyze a Vulnerable System for a Small Business

# **Vulnerability Assessment Report**

**14th July 2024**

------

# **System Description**

The server hardware consists of a powerful CPU processor and 128GB of memory. It runs on the latest version of Linux operating system and hosts a MySQL database management system. It is configured with a stable network connection using IPv4 addresses and interacts with other servers on the network. Security measures include SSL/TLS encrypted connections.

# **Scope**

The scope of this vulnerability assessment relates to the current access controls of the system. The assessment will cover a period of three months, from June 2024 to August 2024. [NIST SP 800-30 Rev. 1](https://docs.google.com/document/d/1pRpdpQMEWskxSkwqEMv8W7A7x8GXQlcn0hEcDzWet3Y/template/preview?usp=sharing&resourcekey=0-3GRRWAd8HryVgof-Jc33yA) is used to guide the risk analysis of the information system.

# **Purpose**

The remote database server is critical to the business operations of the company because its globally distributed employees regularly query, or request, data to find potential customers. It is estimated that the server enables the company to generate around USD 5000 per hour of operation. Ensuring its availability, hence securing the server, is of paramount importance because it directly affects the company’s revenue generating operations

# **Risk Assessment**

| Threat source | Threat event                             | Likelihood | Severity | Risk |
| ------------- | ---------------------------------------- | ---------- | -------- | ---- |
| Employee      | Alter/Delete critical information        | 1          | 3        | 3    |
| Hacker        | Conduct Denial of Service (DoS) attacks. | 2          | 3        | 6    |
| Hardware      | Disrupt mission-critical operations.     | 1          | 3        | 3    |

# **Approach**

Risks considered the data storage and management methods of the business. The likelihood of a threat occurrence and the impact of these potential events were weighed against the risks to day-to-day operational needs.

Users are the entities that most frequently interact with the server. Thus, it is important to review and enforce policies that govern the authorization and privileges of users with regards to data usage.

Since the server is also open to the public, malicious actors may also find ways to overload the server with excessive requests thereby executing a DoS. In addition, they may also find vulnerabilities in the server and collect sensitive and business-critical information.

Lastly, since the server is operational 24x7, it is important to consider the performance of the hardware itself. There is a risk of hardware failure that negatively affects business continuity and revenue.

# **Remediation Strategy**

Implementation of authentication, authorization, and auditing mechanisms ensure that only authorized users access the database server. This includes using strong passwords, role-based access controls, and multi-factor authentication to limit user privileges.

To reduce the risk of malicious actors performing exploits, encryption of data in motion using TLS instead of SSL is used and implemented. Additionally, IP allow-listing corporate offices will prevent not only hackers but also prevent random users from the internet from connecting to the database.

With regards to continuous hardware operations, the company can consider implementing warm standbys of the server with live backups of data. Ensure as well that the proper maintenance is followed in accordance with manufacturer’s guidelines.

---

**END OF PERSONAL WORK**

---



**Guide is found below:**

---

## Activity Overview

In this activity, you will conduct a vulnerability assessment for a small business. This involves evaluating the risks of a vulnerable information system and outlining a remediation plan. The scenario involves a remote database server open to the public, used by employees to query data. Your task is to create a report that explains the risks and how to secure the server.

## Scenario

You are a newly hired cybersecurity analyst for an e-commerce company. The company stores information on a remote database server accessible by employees worldwide. This database has been open to the public since the company's launch three years ago, which poses a significant security risk. Your task is to complete a vulnerability assessment to communicate the risks and provide a remediation plan.

## Step-By-Step Instructions

### Part 1 - Open a Report Template

#### Step 1: Access the Template
Use the following template to construct your written report:

- Click the link and select **Use Template**: [Vulnerability Assessment Report](https://docs.google.com/document/d/1GYQchjHbuWYhl1VLb6jBuCJRsXSDjc9msoOAQPxq_wQ/template/preview?usp=sharing).

OR

- Download the template: [Vulnerability Assessment Report Template DOCX File](https://d3c33hcgiwev3.cloudfront.net/AA2bJWfYQS2T9RaZWsyCGA_b420b19b817e425bb78d6c432fcfa8f1_Vulnerability-assessment-report-template.docx?Expires=1721088000&Signature=UdJ689WboVtTOT3tWcsm4LSOrhkgBW77ZYJgDVjYVWnqY7wWUL1UgnQsGvgKvwG73Nn5ttRpUC-oPMUo~-XIsgtwYH3~IPzmFdi51SeRKt6GcHI0ksUu6O2MvcddwJnTXUUsOfnxxzZtq4WBBwIxU3SSatm-pL-iFRug7afL7Y0_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

#### Step 2: Access Supporting Materials
Use the supporting materials for this course item:

- Click the link and select **Use Template**: [NIST SP 800-30 Rev. 1](https://docs.google.com/document/d/1pRpdpQMEWskxSkwqEMv8W7A7x8GXQlcn0hEcDzWet3Y/template/preview?resourcekey=0-3GRRWAd8HryVgof-Jc33yA).

OR

- Download the supporting materials: [NIST SP 800-30 Rev. 1 DOCX File](https://d3c33hcgiwev3.cloudfront.net/oTLw9sclThSHt1rQL9NxzQ_56dbbc7b9a0b4f7e89eb8cf0d6b75df1_NIST-SP-800-30-Rev.-1.docx?Expires=1721088000&Signature=S7tDguSrHn5jQftf0z7pPIQ63yVYC7xLm~jAkmtYk7Z9ZdiLfHITWFwOKz5IA-xcwkuqykqKmNmHAkloSf-VfXuGJQ1LKnWlSal4Zzy7B5GdB5zT7c24hj4EgVKqzdnUidbMO0kUhlas9IW~ELFR6kXPVZoQyOQZF~7UNkVPgFU_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

#### Step 3: Review Information about the Vulnerable Server
Review the **System Description** and **Scope** sections in the provided template. These sections describe the system being evaluated and the boundaries of the assessment.

### Part 2 - Perform the Risk Assessment

#### Step 1: Explain the Purpose of the Information System
Use the [NIST SP 800-30 Rev. 1](https://docs.google.com/document/d/1Fc4L2azQlnUM-8r43PU9mYlT30BnxTwdjAMqpT7JeZk/edit?resourcekey=0-Q-XglnC3Li7JPK2hIvMkVg#) resource to complete this activity. Write a purpose statement for the **Purpose** section of the report. Consider:
- How is the database server valuable to the business?
- Why is it important to secure the data on the server?
- How might the server impact the business if it were disabled?

#### Step 2: Identify and Analyze Vulnerabilities
Using the provided resources, identify and analyze the vulnerabilities of the open database server. Document these vulnerabilities in the report.

#### Step 3: Perform a Risk Assessment
Assign a risk score to each identified vulnerability based on its potential impact and likelihood. Document the risk assessment in the report.

#### Step 4: Recommend Remediation Steps
Provide remediation steps to address the identified vulnerabilities. This may include:
- Implementing access controls
- Encrypting sensitive data
- Regularly updating software and systems
- Monitoring and logging access to the server

### Questions and Completion
Answer the 5 questions at the end of the activity to test your understanding. Compare your work to the completed exemplar provided in the next course item.

## Key Takeaways
This activity involves conducting a vulnerability assessment, analyzing risks, and recommending remediation steps. Completing this will enhance your skills in identifying and mitigating vulnerabilities in an organization's security systems.