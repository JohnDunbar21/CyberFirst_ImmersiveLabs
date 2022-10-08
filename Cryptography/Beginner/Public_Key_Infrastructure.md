# Public Key Infrastructure

## Quick Summary
Public Key Infrastructure (PKI) is a framework that enables entities (users and servers) to securely exchange information using digital certificates and encryption pairs. In today’s digital age, PKI works as a guard to shield confidential information from one party to another.

### What Is Public Key Infrastructure?
Public key infrastructure, also known as PKI, is a combination of the cryptographic technologies and procedures used to secure data and authenticate entities. More specifically, PKI is the set of hardware, software, policies, processes, and procedures required to create, manage, distribute, use, store, and revoke digital signatures and public keys. This foundation enables the use of technologies, such as digital signatures and encryption, across systems.

PKI is the essential backbone of digital certificate systems that confirm the identity of people, devices, and applications. Digital certificates act as a passport, confirming that an entity is who they claim to be. Certificates can be assigned to users, but also computers, software packages, or anything else that needs proof of identity. PKI is fundamental for digitally signing documents and authenticating user certificates.

PKI describes the framework for the technology as a whole; it is not a single, physical entity. Several elements are required to ensure effective use of PKI authentication.

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/ec0DD3J1pKRFiIFQrGiLTLH1PbdoB5Lf5Z1WWZdZ2oM.png">

### How Does It Work?
PKI utilises asymmetric encryption keys, which means a public and private key pair is required. These cryptographic key pairs verify the identity and legitimacy of people, devices, and services, enabling controlled access to systems and resources, protection of data, and accountability in transactions.

A user’s public key is – as the name suggests – publicly available to any user or system, and can be viewed by anyone, whereas the private key is owned by a single individual and is typically kept confidential and away from prying eyes. This is now a fundamental component in the world of eCommerce. Whenever a transaction is processed online, the customer uses the public key of the application to encrypt their sensitive information. The server then uses its private key to decrypt the customer’s information, protecting the customer's details from being intercepted and read by a malicious entity.

A **Certificate Authority (CA)** is used to authenticate the digital identities of users (individuals, servers, etc.) and to prevent falsified entities. CAs represent the people, processes, and tools used to create the **digital certificates** used in the authentication process. There are globally trusted certificate authorities in which registration typically requires a manual vetting process. This is because any certificate they sign automatically becomes trusted. CAs therefore need to be secure as they have far-reaching impacts if breached. In creating certificates, CAs manage the public keys and credentials for a user's data encryption. If a user retrieves a public key from a trusted certificate authority, they can be assured that the public key is valid. The user can also trust that the certificate and its associated public key belong to the entity specified by the distinguished name.

Additionally, a **Registration Authority (RA)** is authorised (with the aid of the **CA**) to offer **digital certificates** to entities. Certificate history and facts are saved on a **certificate store**, which is grounded on a particular computer and acts as a storage space for all memory applicable to the certificate's history, such as issued certificates and personal encryption keys.

Lastly, a **Validation Authority (VA)** is a body that checks the validity of an electronic certificate by referring to a list of invalid certificates and confirms whether the electronic certificate was issued by a sufficiently trustworthy CA.

Here is an example of how these elements work together:

1. A user applies for a certificate with their public key at an **RA**.
2. The RA confirms the user’s identity to the **CA** which in turn issues the certificate.
3. The certificate is then ready for use and the user can digitally sign a contract using their new certificate.
4. The identity is checked by the contracting party with a VA which again receives information about issued certificates by the CA.

To conclude, PKI uses digital certificates to authenticate using asymmetric encryption and therefore governs encryption keys by issuing and managing these digital certificates. Digital signing helps ensure that data comes from a legitimate source and hasn’t been altered in transit. 

### Who And What Uses It?
In today's connected world, vast amounts of our valuable information are constantly transmitted and it's important that this information is securely trusted and protected against attacks. PKI works as a guard to shield confidential information from one party to another.

By using an asymmetric key encryption system, PKI secures sensitive electronic records in transit between parties and provides a key to encrypt and decrypt the digital data. This helps to protect what you do and the information you send and receive online. The most common applications of PKI include the web, Wi-Fi authentication, email security, and Virtual Private Networks (VPNs). A padlock icon in your browser signifies that the site uses a TLS/SSL certificate, which is based on PKI. TLS/SSL certificates exist on websites so that site visitors know they’re only sending information to the intended recipient.

Here is an example of how TLS/SSL PKI authentication works if someone navigates to **immersivelabs.online**:

1. Your web client connects to the immersivelabs.online webserver to get the server's certificate and public key.
2. The web client then verifies whether that site’s certificate originates from a trusted source by looking in your browser/computer's certificate store.
3. The client encrypts a piece of data using the certificate's public key and sends it to the server. If the server can read it, it proves that the server has the correct private key and it's connecting to the right server.

From eCommerce transactions on your website to emails that contain sensitive information, your data is secure because of PKI.

To summarise, PKI works in three key ways:

1. **PKI authenticates you and your server**: It allows site users’ web browsers to authenticate your server before connecting to it, so it can verify that they’re connecting to a legitimate server. You can also use client certificates to limit access to authenticated users, which gives greater control over your network and other IT systems.
2. **PKI facilitates encryption and decryption**: It enables you to use digital certificates and public encryption pairs to encrypt and decrypt data.
3. **PKI ensures the integrity of your data**: It helps to protect against tampering of data by facilitating digital signatures to confirm that it has come from a specific identity.