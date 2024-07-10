# Public Key Infrastructure (PKI)

## Overview
Public Key Infrastructure (PKI) is an encryption framework that secures the exchange of information online. It simplifies managing encryption keys and ensures fast, easy, and secure access to information.

## How PKI Works
PKI is a two-step process involving:
1. **Exchange of Encrypted Information:** This can involve asymmetric encryption, symmetric encryption, or both.
2. **Establishing Trust:** Using digital certificates to verify the identity of entities exchanging information.

### Asymmetric Encryption
Asymmetric encryption uses a public and private key pair for data encryption and decryption.

- **Public Key:** Can be shared widely and used to encrypt data.
- **Private Key:** Kept secret by the owner and used to decrypt data.

#### Example
- A public key is like a slot on a locked box where items can be added.
- A private key is like the key that fully opens the box to access the items inside.

Asymmetric encryption ensures secure data exchange but can be slow.

### Symmetric Encryption
Symmetric encryption uses a single secret key for both encryption and decryption of data.

- **Single Secret Key:** Shared among users to encrypt and decrypt data.

#### Example
- The same key is used to open and close a locked box, allowing both adding and accessing items.

Symmetric encryption is faster but less secure compared to asymmetric encryption.

### Combining Asymmetric and Symmetric Encryption
PKI uses both encryption types based on the priority of speed or security.

#### Example
- Mobile chat applications start with asymmetric encryption to establish a secure connection.
- Symmetric encryption takes over for faster communication during the conversation.

## Establishing Trust with Digital Certificates
Digital certificates address the vulnerability of key sharing by establishing trust between computers and networks.

### Digital Certificate
A digital certificate verifies the identity of a public key holder. Most online information exchange uses digital certificates.

#### Creation of a Digital Certificate
1. **Registration:** An online business registers its domain and provides basic information and a public key to a Certificate Authority (CA).
2. **Verification:** The CA verifies the company’s identity using the provided information.
3. **Certificate Issuance:** The CA encrypts the verified data with its private key and creates a digital certificate containing the encrypted company data and the CA's digital signature.

### Role of Digital Certificates
Digital certificates act as digital ID badges online, restricting or granting access to information.

## Summary
PKI combines asymmetric and symmetric encryption with digital certificates to create a secure and trustworthy environment for exchanging information online. This comprehensive approach makes PKI a powerful security control in protecting information privacy.