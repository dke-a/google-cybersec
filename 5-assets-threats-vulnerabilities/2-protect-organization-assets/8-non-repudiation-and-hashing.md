# Non-repudiation and Hashing

## Overview
Security professionals are always thinking about vulnerabilities to stay ahead of threats. In this reading, you will learn about another security control that helps companies address the weaknesses in encryption keys: hashing.

## Hash Functions
A hash function is an algorithm that produces a code that can't be decrypted. Unlike asymmetric and symmetric algorithms, hash functions are one-way processes that do not generate decryption keys. Instead, these algorithms produce a unique identifier known as a hash value, or digest.

### Example
Imagine a company has an internal application that is used by employees and is stored in a shared drive. After passing through a hashing function, the program receives its hash value. For demonstration purposes, a relatively short hash value is created using the MD5 hashing function. Generally, standard hash functions that produce longer hashes are preferred for being more secure.

If an attacker replaces the program with a modified version that performs malicious actions, the malicious program may work like the original. However, if even one line of code is different from the original, it will produce a different hash value. By comparing the hash values, we can validate that the programs are different. Hash values help us identify when something like this is happening.

### Use of Hashes in Security
In security, hashes are primarily used as a way to determine the integrity of files and applications. Data integrity relates to the accuracy and consistency of information. This is known as non-repudiation, the concept that the authenticity of information can't be denied.

### Generating Hash Values
Hash functions are important security controls that make proven data integrity possible. Analysts use them frequently. One way to do this is by finding the hash value of files or applications and comparing them against known malicious files.

For example, you can use the Linux command line to generate the hash value for any file on your computer. Launch a shell and type the name of the hashing algorithm you want to use. In this case, we use a common one known as sha256. Enter the file name of any file you want to hash, for instance, newfile.txt. The terminal generates this unique hash value for the file.

### Hash Values and Online Databases
These tools can be compared with the hash values of known online viruses. VirusTotal is a popular tool among security practitioners that is useful for analyzing suspicious files, domains, IPs, and URLs.

### Importance of Hash Functions
Even the slightest change in input results in a totally different hash value. Hash functions are intentionally designed this way to assist with matters of non-repudiation. They equip computers with a quick and easy way to compare input and output values and validate data integrity.

## Key Takeaways
- Hash functions produce a unique identifier known as a hash value or digest.
- Hash functions are one-way processes and do not generate decryption keys.
- Hash values help determine the integrity of files and applications.
- Non-repudiation ensures the authenticity of information can't be denied.
- Security practitioners use hash values to compare files and detect changes.
- Tools like VirusTotal are used to analyze suspicious files using hash values.

Hashing is a fundamental concept in maintaining data integrity and ensuring that information has not been altered, which is critical for security professionals.