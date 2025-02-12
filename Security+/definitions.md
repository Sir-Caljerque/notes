---
id: definitions
aliases: []
tags: []
---

# Security+ Acronyms by Topic

## Cryptography
- **AES**: Advanced Encryption Standard - Symmetric encryption standard widely used for securing sensitive data. AES supports key sizes of 128, 192, and 256 bits.
- **DES**: Data Encryption Standard - Outdated symmetric encryption algorithm, now considered insecure due to its short key length (56 bits).
- **3DES**: Triple Data Encryption Standard - An improvement on DES that applies the DES algorithm three times to each data block, but still considered weak compared to modern standards.
- **RSA**: Rivest-Shamir-Adleman - A widely used asymmetric encryption algorithm for secure data transmission. It uses a pair of keys: one public and one private.
- **ECC**: Elliptic Curve Cryptography - A form of asymmetric encryption that uses elliptic curves, providing the same level of security as RSA but with shorter key sizes.
- **SHA**: Secure Hash Algorithm - A family of cryptographic hash functions (e.g., SHA-1, SHA-256, SHA-512) used to ensure data integrity by generating fixed-size output from input data.
- **HMAC**: Hash-based Message Authentication Code - A mechanism for message authentication using a hash function and a secret key, ensuring both data integrity and authenticity.
- **PKI**: Public Key Infrastructure - A framework for managing digital keys and certificates to facilitate secure communications over a network.
- **CA**: Certificate Authority - A trusted organization that issues digital certificates as part of a PKI, ensuring the authenticity of public keys.
- **CSR**: Certificate Signing Request - A request generated by an entity to obtain a digital certificate from a CA, containing information such as the public key and domain name.
- **X.509**: Standard for Public Key Certificates - A standard defining the format of digital certificates, commonly used in PKI to validate identities.
- **PFS**: Perfect Forward Secrecy - A feature of cryptographic systems that ensures session keys are not compromised even if private keys are leaked in the future.

## Authentication and Authorization
- **AAA**: Authentication, Authorization, and Accounting - A framework for managing access to networks and resources, focusing on verifying identity (authentication), determining access levels (authorization), and tracking usage (accounting).
- **RADIUS**: Remote Authentication Dial-In User Service - A protocol used to manage authentication, authorization, and accounting for remote users connecting to a network.
- **TACACS+**: Terminal Access Controller Access Control System Plus - A protocol similar to RADIUS but provides more granular control over authentication and authorization, commonly used in network devices like routers and switches.
- **LDAP**: Lightweight Directory Access Protocol - A protocol used to access and manage directory services, commonly used for storing and retrieving user credentials and access rights.
- **SAML**: Security Assertion Markup Language - A standard for exchanging authentication and authorization data between parties, typically used for single sign-on (SSO) implementations.
- **OAuth**: Open Authorization - A protocol for token-based authorization, commonly used to allow third-party applications to access resources without sharing user credentials.
- **OIDC**: OpenID Connect - An authentication protocol built on top of OAuth 2.0, allowing users to authenticate with third-party identity providers.
- **MFA**: Multi-factor Authentication - A security process that requires two or more forms of verification (e.g., password, token, biometric) to authenticate a user.
- **2FA**: Two-factor Authentication - A specific form of MFA that uses exactly two factors to authenticate a user, usually something they know (password) and something they have (token).
- **FIDO**: Fast Identity Online - A set of open standards for passwordless authentication, typically using biometric data or cryptographic tokens for verification.
- **IAM**: Identity and Access Management - A framework for managing digital identities and controlling access to resources within an organization.
- **RBAC**: Role-based Access Control - A method of restricting system access based on users' roles within an organization, with permissions assigned to roles rather than individuals.
- **ABAC**: Attribute-based Access Control - A model where access decisions are based on attributes (e.g., user attributes, resource attributes) rather than roles.

## Networking and Protocols
- **IPSec**: Internet Protocol Security - A suite of protocols used to secure Internet Protocol (IP) communications by authenticating and encrypting each IP packet in a data stream.
- **SSL**: Secure Sockets Layer - A now-deprecated cryptographic protocol used to secure communications over a network. SSL has been replaced by TLS (Transport Layer Security).
- **TLS**: Transport Layer Security - A cryptographic protocol used to secure communications over a network, succeeding SSL. It is widely used in HTTPS to secure web traffic.
- **VPN**: Virtual Private Network - A technology that creates a secure connection over the internet or other untrusted networks, ensuring confidentiality and data integrity.
- **PPTP**: Point-to-Point Tunneling Protocol - An older and insecure VPN protocol that encapsulates PPP packets within IP packets for tunneling. It is rarely used today due to security weaknesses.
- **L2TP**: Layer 2 Tunneling Protocol - A more secure VPN protocol that combines with IPsec for encryption, offering stronger security than PPTP.
- **UDP**: User Datagram Protocol - A connectionless protocol used for fast, low-latency communications where error correction and reliability are less critical.
- **TCP**: Transmission Control Protocol - A connection-oriented protocol that ensures reliable data transmission by providing error checking and retransmission.
- **DNS**: Domain Name System - A system that translates human-readable domain names (e.g., www.example.com) into IP addresses used by computers to identify each other on the network.
- **DHCP**: Dynamic Host Configuration Protocol - A network protocol used to dynamically assign IP addresses to devices on a network.
- **ARP**: Address Resolution Protocol - A protocol used to map an IP address to a MAC address, enabling communication on a local network.
- **NAT**: Network Address Translation - A method used to modify IP address information in packet headers to facilitate communication between different networks, commonly used in home routers.
- **NIDS**: Network Intrusion Detection System - A system designed to monitor network traffic for signs of malicious activity or policy violations.
- **NIPS**: Network Intrusion Prevention System - A system that actively prevents potential attacks by monitoring network traffic and taking action to block harmful packets.

## Security Technologies and Concepts
- **IDS**: Intrusion Detection System - A security system designed to detect and alert administrators about potentially malicious activity or policy violations within a network or system.
- **IPS**: Intrusion Prevention System - Similar to an IDS but with the added capability to block malicious activities in real-time.
- **DLP**: Data Loss Prevention - A set of tools and processes used to monitor and prevent the unauthorized access, use, or transmission of sensitive data.
- **WAP**: Wireless Access Point - A device that allows wireless devices to connect to a wired network using Wi-Fi.
- **WPA**: Wi-Fi Protected Access - A security protocol designed to secure wireless networks. WPA2 and WPA3 are improved versions of WPA.
- **WPA2**: Wi-Fi Protected Access 2 - An updated version of WPA with stronger encryption and security features.
- **WPA3**: Wi-Fi Protected Access 3 - The latest Wi-Fi security standard, providing enhanced protection against brute-force attacks and improving encryption protocols.
- **MAC**: Mandatory Access Control - A security model that uses labels and classifications to enforce strict access controls based on the classification of data and the clearance of users.
- **DAC**: Discretionary Access Control - A model where the owner of the resource determines who can access it, typically using file permissions.
- **MALWARE**: Malicious Software - Generic term for software designed to harm, exploit, or otherwise compromise the functionality or data of a system.
- **ALE** Annual loss expectancy - How much money you lose in a span of 12 months
- **SLE** single loss expectancy - money loss if one event occurs, like a server going down
- **RTO** Recovry time objective - how fast you can get everything ready if event occurs ... How long it takes to get service up
- **RPO** Recovery point objective - How much tolerance you have / how much data you're willing to lose until action needs to be taken
- **ARO** annualized rate of occurance - event frequency / how many times a server crashes in a span of time

## Risk Management and Incident Response
- **HA**: High availability
- **MTTR**: Mean Time to Recovery - A metric used to measure the average time it takes to restore a system or application after an outage or disruption.
- **MTBF**: Mean Time Between Failures - A measure of the expected time between system failures, used to predict system reliability.
- **RTO**: Recovery Time Objective - The targeted duration of time within which a business process must be restored after a disaster to avoid unacceptable consequences.
- **RPO**: Recovery Point Objective - The maximum acceptable amount of data loss measured in time, used to determine how frequently data backups should occur.
- **BIA**: Business Impact Analysis - A process used to identify the effects of disruptions to business operations and prioritize recovery efforts.
- **SLA**: Service Level Agreement - A formal contract between a service provider and a customer, defining the level of service expected, including uptime and support.
- **COOP**: Continuity of Operations Plan - A plan that ensures essential operations can continue during and after a disaster or disruption.
- **BCP**: Business Continuity Plan - A comprehensive plan that ensures the ongoing operation of critical business functions after a disruption.
- **DRP**: Disaster Recovery Plan - A strategy to recover and protect IT infrastructure and data in the event of a disaster.
- **IRP**: Incident Response Plan - A set of procedures to follow when responding to a security incident or breach to mitigate damage and recover systems.
- **FIPS**: Federal Information Processing Standards - A set of standards issued by the U.S. government to ensure the security and privacy of sensitive data.

## Threats and Vulnerabilities
- **APT**: Advanced Persistent Threat - A long-term, targeted cyberattack, often aimed at stealing sensitive information or compromising a network.
- **DDoS**: Distributed Denial of Service - An attack that uses multiple systems to flood a network or server with traffic, making it unavailable to legitimate users.
- **DoS**: Denial of Service - An attack aimed at disrupting the availability of a service or network by overwhelming it with traffic.
- **MITM**: Man-in-the-Middle - An attack where the attacker intercepts and potentially alters communications between two parties without their knowledge.
- **SQLi**: SQL Injection - A type of attack where an attacker injects malicious SQL code into a database query to manipulate or access sensitive data.
- **XSS**: Cross-site Scripting - A vulnerability in web applications where attackers inject malicious scripts into webpages viewed by other users.
- **CSRF**: Cross-site Request Forgery - An attack that tricks a user into performing unintended actions on a website without their consent.
- **RAT**: Remote Access Trojan - A type of malware that allows an attacker to remotely control an infected system without the user's consent.
- **VLAN**: Virtual Local Area Network - A logical segmentation of a network that allows devices to communicate as if they are on the same local network, regardless of their physical location.

## Security Controls and Management
- **SIEM**: Security Information and Event Management - A system used to collect, analyze, and respond to security events and incidents across a network.
- **SOC**: Security Operations Center - A centralized unit that monitors and responds to security incidents and threats in an organization.
- **CISO**: Chief Information Security Officer - The executive responsible for overseeing and implementing the organization's information security program.
- **CISM**: Certified Information Security Manager - A certification for professionals who manage and oversee information security programs within an organization.
- **CISSP**: Certified Information Systems Security Professional - A globally recognized certification for professionals who design, implement, and manage security programs.
- **ISO**: International Organization for Standardization - An independent, non-governmental organization that develops international standards, including security frameworks like ISO 27001.
- **SOC 2**: Service Organization Control 2 - A framework for managing and securing data, specifically for cloud service providers and SaaS companies.
- **HIPAA**: Health Insurance Portability and Accountability Act - A U.S. law that sets standards for protecting sensitive patient health information.
- **PCI-DSS**: Payment Card Industry Data Security Standard - A set of security standards aimed at protecting cardholder data during transactions.
- **GDPR**: General Data Protection Regulation - A regulation in the EU that sets guidelines for the collection and processing of personal data of individuals within the EU.
- **NIST**: National Institute of Standards and Technology - A U.S. federal agency that develops cybersecurity standards, guidelines, and best practices.
- **CVE**: Common Vulnerabilities and Exposures - A publicly available list of known cybersecurity vulnerabilities and exposures in software and hardware.

## Cloud Security
- **SaaS**: Software as a Service - A cloud computing service model where software applications are delivered over the internet on a subscription basis.
- **PaaS**: Platform as a Service - A cloud computing service model that provides a platform and environment for developers to build, deploy, and manage applications.
- **IaaS**: Infrastructure as a Service - A cloud computing service model that provides virtualized computing resources, such as virtual machines, storage, and networking.
- **DaaS**: Desktop as a Service - A cloud-based service that provides virtual desktops to end-users, allowing them to access their desktop environment remotely.
- **CASB**: Cloud Access Security Broker - A security tool that provides visibility and control over cloud service usage, helping to enforce security policies.
- **VPC**: Virtual Private Cloud - A private network within a public cloud that allows an organization to isolate its resources while still using cloud infrastructure.
- **MDM**: Mobile Device Management - A security solution for managing and securing mobile devices within an organization, often used to enforce policies such as encryption and remote wipe.
- **COPE**: Corporate Owned, Personally Enabled - A mobile device management strategy where the organization provides employees with devices that they can use for both personal and professional purposes, but with management and security controls in place.
