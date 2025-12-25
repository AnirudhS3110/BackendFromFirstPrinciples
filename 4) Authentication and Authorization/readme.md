# History:
- **Implicit Authentication** :At time where Cryptography was not discovered, people used to authenticate via "TRUST", "i know this peroson", people were trusted based on REPUTATION, but this was not scalable for alrger regions. People used Seals as shown in movies , it was one form of early cryptographic mechanism. These were adopted as teh AUTHENTICATION TOKENS  in medieval period.But it has several vulnerabilities
- This vulnerabilities led to birth of cryptographic methods, people started thinking of CODES
- At times of Industria Evolution, communication services evolved which lead use of Telegraph, for authentication they used some form of PARSE Phrases, it was early form of Shared Secrets
- These were static passwprds., "Something you Possessed(auth through Seals)" got eveolved into "Something you know".
### **Modern times of Computation Arch**:
- First form of computation: mainframes
- This is where passwords came, but at that time passwords were saved as PLAIN text, which possesed Security Vulnerability
- This evolved to storing passwords securely which lead to innovations like Hashing , or other Cryptographic algos

#### Asymmetric Cryptography:
- Two parties Shared secret over a Untrusted Medium
- This became the BACKBONE of MODERN Authentication Protocols
- Every protocol we know are based on Asymmetric Key Cryptography also called (Public Key Infrastructures)
- This led to coming up of protocols like Kubros which introduced Ticket Based Auth
- It relies on Ticket issued by Trusted Third Parties, which is used to verify both user and service Identity which is precursor to Token based AUth system

## MFA(Multi Factor Authentication):
- Around 1990's simple sUsername Passwoerd auth was not safe against Brute Force and Dictionary Attacks, THis lead to MULTI FACTOR Authentication!
- MFA is based on:
- 1) Something you Know (passwords)
- 2) Something You Own(OTP generators)
- 3) Something You are (Biometirc data like FIngerprint / Retina scans)
- Due to this Biometric Authentication  became Ground Breaking Auth system.
- but biometric introduced cahllenges like: False Positives, Template Security

## Auth in Modern Times:
- As Cloud Computing, APi based architecture frameworks Bloomed, they demanded Advanced Auth frameworks, this lead to:
- OAuth 2.0 (Most Popular)
- JWT Tokens
- Zero Trust Architecture
- Password less auth: System like Web Authentication, removes passwords Entirely.
- Decentralized Identity (Used in BlockChain)
### Post Quantum Cryptography: 
- These consists of Cryptographic Algos which are even safer with Quantum Computing
- Once Quantum Computers are avaible to use, They will break al teh cryptographic Algorithms, this lead to RSA and other stuffs , this lead to Public Key, Private key algos, which are very difficult to crack with the  available hardware/ Computation  systems 