# Access Control Worksheet

## Note about the user:
- **Event Date:** 10/03/23
- **User Role:** Legal/Administrator
- **IP Address:** 152.207.255.255

Event logs are crucial in identifying the who, what, and why of a security incident. They provide detailed records of user activities, helping to trace the source of security breaches.

## Access Control Issue(s):
- **User:** Robert Taylor, Jr.
- **Role:** Contractor with admin access
- **Contract End Date:** 2019
- **Incident:** Account accessed payroll systems in 2023

This incident likely occurred due to misconfiguration or misuse of the system, highlighting how information is shared among employees.

## Recommendations:
1. **Account Expiry Policy:**
   - User accounts, especially for contractors, should automatically expire after 30 days post-contract end date.
   - Implement periodic reviews of user accounts to ensure expired accounts are deactivated promptly.

2. **Access Control Policies:**
   - Limit contractor access to only essential business resources required for their tasks.
   - Regularly audit access permissions to ensure compliance with least privilege and separation of duties principles.

3. **Enable Multi-Factor Authentication (MFA):**
   - Implement MFA for all accounts, especially those with administrative privileges.
   - Encourage or mandate the use of strong, unique passwords for all users.

## Explanation:
The likely scenario involves a former contractor whose account was not deactivated after their contract ended. This presents a security risk as the credentials could be reused or compromised.

Additionally, it’s common for individuals to reuse login credentials across multiple platforms, making them susceptible to credential stuffing attacks if one platform is compromised.

Implementing the following measures can mitigate these risks:
- **Account Expiry Policy:** Ensures that inactive accounts are automatically deactivated, reducing the risk of unauthorized access.
- **Access Control Policies:** Restricting access limits the potential damage in case of a breach and adheres to the principle of least privilege.
- **Multi-Factor Authentication (MFA):** Adds an extra layer of security, making it harder for unauthorized users to gain access even if credentials are compromised.

## Key Takeaways:
This activity underscores the importance of keeping track of user accounts and implementing robust access controls. Without effective access controls, businesses are at risk of unauthorized access and potential data breaches. Establishing clear boundaries on who can access information and what they are allowed to do is a fundamental step in any security plan.