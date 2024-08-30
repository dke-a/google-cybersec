### Analyze Indicators of Compromise with Investigative Tools

In the realm of cybersecurity, security analysts rely on a variety of tools and techniques to detect and analyze potential threats. This section focuses on how investigative tools are employed during investigations to analyze suspicious **Indicators of Compromise (IoCs)** and how these tools help build context around alerts. An IoC is observable evidence that may suggest a potential security incident has occurred.

#### Adding Context to Investigations

The **Pyramid of Pain** illustrates the varying levels of difficulty attackers face when their activities, identified as IoCs, are detected and blocked by security teams. However, identifying and blocking a single IoC, such as an IP address, is often insufficient. Attackers can easily pivot and continue their malicious activities using different resources.

**Key Concept**: Focusing on a single IoC without considering the broader context is like observing only one part of a larger picture, potentially missing out on critical details of an ongoing or past attack.

To gain a comprehensive understanding of an attack, security analysts use **threat intelligence**—evidence-based information about existing or emerging threats. By adding context to IoCs, such as linking a suspicious IP address to other related artifacts like abnormal network communications or unusual processes, security teams can develop a more detailed picture of a security incident. This expanded view allows for faster detection and a more informed response strategy.

#### The Power of Crowdsourcing

**Crowdsourcing** in cybersecurity involves gathering threat information through public collaboration. This practice allows security teams to benefit from the collective knowledge of the global cybersecurity community, which includes industry experts, government agencies, and other organizations.

**Without Crowdsourcing**: Incident response was traditionally performed in isolation, with each organization addressing threats independently. This approach often led to duplicated efforts and missed opportunities for collaboration.

**With Crowdsourcing**: Organizations can share and access a wide range of threat intelligence data, improving their detection capabilities and enabling them to defend against threats more effectively.

**Examples**:
- **Information Sharing and Analysis Centers (ISACs)**: These centers focus on collecting and sharing sector-specific threat intelligence within industries such as energy, healthcare, and finance.
- **Open-source Intelligence (OSINT)**: OSINT involves collecting and analyzing publicly available information to generate actionable intelligence. It’s particularly useful for understanding threats, threat actors, and vulnerabilities.

#### VirusTotal

[**VirusTotal**](https://www.virustotal.com/gui/home) is a widely-used service that allows users to analyze suspicious files, domains, URLs, and IP addresses for malicious content. VirusTotal aggregates data from multiple security vendors, providing a comprehensive overview of the potential threats associated with an IoC.

**Key Features**:
1. **Detection**: Lists detection verdicts from third-party security vendors, indicating whether an IoC is malicious, suspicious, or safe.
2. **Details**: Provides additional information from a static analysis of the IoC, including hashes, file types, creation time, and more.
3. **Relations**: Shows related IoCs connected to the artifact, such as contacted URLs, domains, and IP addresses.
4. **Behavior**: Displays observed behaviors of an artifact when executed in a controlled environment, including network communications and system changes.
5. **Community**: A platform where VirusTotal users can share comments and insights about an IoC.
6. **Vendors’ Ratio and Community Score**: The vendors' ratio indicates how many security vendors have flagged the IoC as malicious, and the community score reflects the consensus of VirusTotal users.

**Caution**: Data uploaded to VirusTotal is publicly shared with the entire community, so it’s important to avoid submitting personal or sensitive information.

#### Other Investigative Tools

**Jotti Malware Scan**:
- [Jotti's Malware Scan](https://virusscan.jotti.org/) allows users to scan suspicious files with multiple antivirus programs. However, it has limitations on the number of files that can be submitted.

**Urlscan.io**:
- [Urlscan.io](https://urlscan.io/) is a service that scans and analyzes URLs, providing a detailed report on the URL’s characteristics and potential risks.

**MalwareBazaar**:
- [MalwareBazaar](https://bazaar.abuse.ch/browse/) is a repository for malware samples, offering a valuable resource for research and threat intelligence gathering.

#### Key Takeaways

As a security analyst, it’s crucial to understand how to effectively analyze IoCs and add context to your investigations. Doing so improves detection capabilities and enables you to make informed decisions when responding to potential threats.

These tools and techniques are essential for developing a comprehensive understanding of security incidents and for implementing effective defense strategies against evolving cyber threats.