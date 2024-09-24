# Decentralized Application Environment for a Company

In this paper I like to show an approach for a company to use the Block Chain technology for data and interaction among
employees, departments and clients.

### What are the main changes an employee is confronted with?

- An employee has to manage a secret key and a user address - like a password and user id.
- Transactions can always be tracked back to the user.
- Transaction costs are paid via the user address.
- 

First a comparison between traditional data and application usage in companies:

| Topic                  | Traditional                                                    | Blockchain                                                                     |   |   |
|------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------------|---|---|
| Data                   | Data is saved internally on DBs or via a private cloud access  | Contract data (e.g. Ethereum, Polygon), decentralized file data (e.g. Arweave) |   |   |
| Application            | Backend-System internally or externally, Installed Application | Decentralised App access blockchain directly                                   |   |   |
| User Authentication    | Login OAuth, etc                                               | User has a secret key, (BYOS: bring your own security)                         |   |   |
| User Admin             | System like LDAP, Active Directory etc.                        | Add remove Users in Smart Contracts                                            |   |   |
| Document Management    | Sharepoint, ...                                                | Smart Contract with decentralized file data (e.g. Arweave)                     |   |   |
| Appliation Manangement | Var.                                                           | Smart Contract Management Contract (see Contract-Registry)                     |   |   |
| Processing Cost        | Internal hardware, Cloud provider cost                         | Blockchain transaction costs (gas price)                                       |   |   |

In contrast to fully transparent public systems (contract) some additional challenges are addressed:

- Data privacy! Data is always and forever public. Encryption is needed!
- User Administration
- Access Management
- Contract and Data Management

This leads to the following functionalities:

- Encrypt data for a specific user group
- Manage the user group (add and remove participants)
- Address to Name and Name to Address management
- Contract Ownership Management
- Key Management
- Transaction cost management

Specific Requirements for a Company:

- An employee has lost the secret key
- An employee might have revealed the secret key

### What are the benefits from D-Apps (Blockchain Apps)

- lower cost for transaction and data
- zero cost for backups
- security breaches can be managed
- ransom attacks are not possible
- denial of service: very low
- application uptime: very high
- build-in un-deniability
- service cost management for clients built-in (value services)
- build-in payment service
- very high interoperability
- new models for privacy
- improvement of productivity (see use cases)


### What are the risk and restrictions?

- Unsafe key management
- Smart Contracts can not be changed after deployment (Design risk)
