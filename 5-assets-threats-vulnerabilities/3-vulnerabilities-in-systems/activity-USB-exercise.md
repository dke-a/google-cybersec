## Parking Lot USB Exercise

### Activity Overview

In this activity, you will assess the attack vectors of a USB drive. You will consider a scenario of finding a USB drive in a parking lot from both the perspective of an attacker and a target.

USBs, or flash drives, are commonly used for storing and transporting data. However, some characteristics of these small, convenient devices can also introduce security risks. Threat actors frequently use USBs to deliver malicious software, damage other hardware, or even take control of devices. USB baiting is an attack in which a threat actor strategically leaves a malware USB stick for an employee to find and install to unknowingly infect a network. It relies on curious people to plug in an unfamiliar flash drive that they find.

### Scenario

You are part of the security team at Rhe/torical Hospital and arrive to work one morning. On the ground of the parking lot, you find a USB stick with the hospital's logo printed on it. There’s no one else around who might have dropped it, so you decide to pick it up out of curiosity.

You bring the USB drive back to your office where the team has virtualization software installed on a workstation. Virtualization software can be used for this very purpose because it’s one of the only ways to safely investigate an unfamiliar USB stick. The software works by running a simulated instance of the computer on the same workstation. This simulation isn’t connected to other files or networks, so the USB drive can’t affect other systems if it happens to be infected with malicious software.

### Work Done

#### Step 1: Access the Template

To use the template for this course item, click the link and select Use Template.

[Parking Lot USB Exercise Template](https://docs.google.com/document/d/1GYQchjHbuWYhl1VLb6jBuCJRsXSDjc9msoOAQPxq_wQ/template/preview?usp=sharing)

OR

If you don’t have a Google account, you can download the template directly from the following attachment.

[Parking Lot USB Exercise Template DOCX File](https://d3c33hcgiwev3.cloudfront.net/AA2bJWfYQS2T9RaZWsyCGA_b420b19b817e425bb78d6c432fcfa8f1_Vulnerability-assessment-report-template.docx?Expires=1721088000&Signature=UdJ689WboVtTOT3tWcsm4LSOrhkgBW77ZYJgDVjYVWnqY7wWUL1UgnQsGvgKvwG73Nn5ttRpUC-oPMUo~-XIsgtwYH3~IPzmFdi51SeRKt6GcHI0ksUu6O2MvcddwJnTXUUsOfnxxzZtq4WBBwIxU3SSatm-pL-iFRug7afL7Y0_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

#### Step 2: Review the USB Contents

You create a virtual environment and plug the USB drive into the workstation. The contents of the device appear to belong to Jorge Bailey, the human resource manager at Rhetorical Hospital.

The USB drive contains a mix of personal and work-related files, such as family and pet photos, a new hire letter, and an employee shift schedule. 

### Analysis

| **Category**         | **Details**                                                  |
| -------------------- | ------------------------------------------------------------ |
| **Contents**         | The USB drive contains multiple files that include PII, such as a resume, new hire letter, and wedding list. It also has sensitive work files like employee budget and shift schedules. Storing personal and work files together is not safe as it increases the risk of compromising both types of data. |
| **Attacker Mindset** | The information on the USB drive can be used to damage its owner, related individuals, and the company. For instance, attackers could use the personal information to target Jorge’s relatives or use the work-related data to gain unauthorized access to the business systems. |
| **Risk Analysis**    | Various types of malicious software could be hidden on the device, including executable malware that activates when a file is opened or non-executable files that trigger malicious scripts, such as MS Office files. If the drive were infected and discovered by another employee, it could severely compromise the company’s information assets. Sensitive information found on such a device could be used to understand internal workings and identify security gaps. For example, an attacker could study employee work schedules to emulate actions undetected or leak financial information, damaging the company’s reputation and potentially leading to financial account hacking. |