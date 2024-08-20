# Overview of Detection Tools

---

## **Introduction to Detection Tools**

### **Why You Need Detection Tools**
- **Purpose:** Detection tools in cybersecurity work similarly to home security systems but focus on protecting networks and systems from unwanted and unauthorized access.
- **Function:** These tools continuously monitor systems and networks for suspicious activity. When something unusual is detected, an alert is triggered to notify security professionals, who then investigate and potentially stop the intrusion.

---

## **Comparison of IDS, IPS, and EDR Tools**

| **Capability**               | **IDS** | **IPS** | **EDR** |
| ---------------------------- | :-----: | :-----: | :-----: |
| Detects malicious activity   |    ✓    |    ✓    |    ✓    |
| Prevents intrusions          |   N/A   |    ✓    |    ✓    |
| Logs activity                |    ✓    |    ✓    |    ✓    |
| Generates alerts             |    ✓    |    ✓    |    ✓    |
| Performs behavioral analysis |   N/A   |   N/A   |    ✓    |

---

## **Overview of IDS Tools**
- **Intrusion Detection System (IDS):**
  - **Function:** Monitors system activity and generates alerts on potential intrusions. IDS tools provide continuous network monitoring to detect threats but do not stop them.
  - **Example:** An IDS might alert security teams to a suspicious login attempt from an unknown IP address but will not prevent further actions.
  - **Popular IDS Tools:** Zeek, Suricata, Snort®, Sagan.

### **Detection Categories in IDS:**
- **True Positive:** Correctly detects the presence of an attack.
- **True Negative:** Correctly identifies that no malicious activity exists.
- **False Positive:** Incorrectly identifies legitimate activity as malicious, leading to unnecessary investigations.
- **False Negative:** Fails to detect an actual threat, leaving the system vulnerable to attacks.

---

## **Overview of IPS Tools**
- **Intrusion Prevention System (IPS):**
  - **Function:** Monitors for and alerts on intrusions like an IDS but also takes steps to prevent the activity and reduce its impact.
  - **Example:** An IPS might send an alert and modify access control lists (ACLs) to block malicious traffic.
  - **Note:** Many tools, such as Suricata, Snort, and Sagan, offer both IDS and IPS capabilities.

---

## **Overview of EDR Tools**
- **Endpoint Detection and Response (EDR):**
  - **Function:** Monitors endpoints (e.g., computers, phones, tablets) for malicious activity, logs and analyzes this activity, and can automatically respond to threats.
  - **Unique Feature:** EDR tools use behavioral analysis, powered by machine learning and AI, to identify unusual patterns that indicate a threat.
  - **Automation:** EDR tools can automatically block malicious processes without manual intervention.
  - **Popular EDR Tools:** Open EDR®, Bitdefender™ Endpoint Detection and Response, FortiEDR™.

---

## **Key Takeaways**
- **Awareness:** Detection tools like IDS, IPS, and EDR provide organizations with visibility into the activity on their networks and systems.
- **Functionality:** These tools are critical for detecting, logging, alerting, and preventing potential malicious activities, thereby securing organizational assets.

---