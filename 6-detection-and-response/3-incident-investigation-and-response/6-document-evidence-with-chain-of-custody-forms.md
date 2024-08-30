### Document Evidence with Chain of Custody Forms

**Chain of Custody:**
- **Definition:** Chain of custody is the process of documenting the possession and control of evidence during an incident's lifecycle. This documentation is critical for ensuring that evidence is accurately tracked and remains untampered with throughout the investigation.
- **Importance:** Ensures transparency and integrity of the evidence, which is essential if the evidence is to be used in legal proceedings.

**Key Components of a Chain of Custody Form:**
1. **Description of Evidence:**
   - Includes identifying information such as location, hostname, MAC address, or IP address.
2. **Custody Log:**
   - Details the names of individuals who transferred and received the evidence, along with the date, time, and purpose of the transfer.

**Example Walkthrough: Chain of Custody in Action**

- **Scenario:** During an incident response, Aisha, a security analyst, identifies a compromised hard drive that needs to be examined by the forensics team.
  1. **Initial Steps by Aisha:**
     - **Write Protection:** Aisha first ensures that the hard drive is write-protected, preventing any data on the disk from being edited or erased.
     - **Hash Calculation:** She then calculates and records a cryptographic hash of an image of the hard drive. This hash serves as a unique fingerprint for the data on the disk.
  2. **Transfer of Evidence:**
     - **Transfer to Colin:** Aisha is instructed to transfer the hard drive to Colin in the forensics department.
     - **Logging in Chain of Custody:** Colin logs the receipt of the hard drive in the chain of custody form, ensuring transparency in the movement of evidence.
  3. **Further Transfer:**
     - **Transfer to Nav:** Colin examines the hard drive and then sends it to Nav, another analyst. Again, the transfer is logged in the chain of custody form.
     - **Final Transfer to Arman:** Nav receives the compromised hard drive and eventually sends it to her manager, Arman. Each transfer is meticulously recorded.
  4. **Tamper Detection:**
     - **Integrity Check:** If there is any suspicion of tampering, the original hash that Aisha documented can be used to verify the integrity of the data. If the hash matches, the data has remained intact.

**Key Points:**
- **Transparency:** A documented paper trail describes who handled the evidence, why, when, and where they handled it.
- **Integrity:** Any transfer of the hard drive is logged to maintain the integrity, reliability, and accuracy of the evidence.
- **Legal Admissibility:** A break in the chain of custody could affect the admissibility of the evidence in legal proceedings.

**Broken Chain of Custody:**
- **Definition:** Occurs when there are inconsistencies in the collection and logging of evidence.
- **Impact:** Can compromise the integrity and reliability of evidence, potentially rendering it inadmissible in court.