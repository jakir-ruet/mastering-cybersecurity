## More About Me – [Take a Look!](http://www.mjakaria.me) 

### Welcome to Mastering Cybersecurity
Cybersecurity is the practice of protecting systems, networks, and data from digital attacks, unauthorized access, damage, or theft. It’s a vast and evolving field that plays a critical role in IT and DevOps, especially in today’s cloud-driven, interconnected world.

## Domain 1 `Security Principles`
### Related Security Terms in Table & Diagram
| **Term**                 | **Scope**             | **Focus**                                      | **Examples**                                            |
| ------------------------ | --------------------- | ---------------------------------------------- | ------------------------------------------------------- |
| **Information Security** | Broadest              | Protecting all forms of information            | Locking file cabinets, encrypting data, access policies |
| **IT Security**          | Subset of InfoSec     | Securing IT systems and digital infrastructure | Antivirus, firewalls, system hardening, secure login    |
| **Cybersecurity**        | Subset of IT Security | Protecting systems from internet-based threats | Phishing protection, DDoS defense, threat hunting, WAF  |

![Set Subset Diagram of Security](/img/security-sets.png)

### Actual Types of Cybersecurity
| **Type of Cybersecurity**                   | **Focus Area**                                                 |
| ------------------------------------------- | -------------------------------------------------------------- |
| **Network Security**                        | Protecting networks, routers, switches, firewalls, IDS/IPS     |
| **Application Security**                    | Securing software applications (web, mobile, APIs)             |
| **Cloud Security**                          | Securing cloud platforms like AWS, Azure, and GCP              |
| **Endpoint Security**                       | Securing user devices (laptops, desktops, smartphones)         |
| **Infrastructure Security**                 | Hardening servers, operating systems, and data centers         |
| **Identity and Access Management (IAM)**    | Controlling user access and enforcing authentication policies  |
| **Data Security**                           | Protecting sensitive data via encryption, masking, and backups |
| **Operational Security (OpSec)**            | Policies and procedures to protect daily operations            |
| **Disaster Recovery & Business Continuity** | Ensuring systems recover after attacks or disasters            |
| **Mobile Security**                         | Securing mobile devices and mobile applications                |
| **IoT Security**                            | Protecting Internet of Things (smart devices, sensors, etc.)   |

### CIA (Confidentiality, Integrity & Availability) Model with Diagram
In cybersecurity and information security, the CIA Triad is a foundational model that outlines the three core principles for protecting information:
| **Component**       | **Meaning**                                  | **Goal**                                                         | **Example**                                                  |
| ------------------- | -------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------ |
| **Confidentiality** | Ensure only authorized users can access data | Prevent unauthorized access, leaks, or spying                    | Using encryption, passwords, and access control lists (ACLs) |
| **Integrity**       | Ensure data is accurate and unchanged        | Prevent unauthorized modification or tampering                   | Checksums, hashes (e.g., SHA-256), digital signatures        |
| **Availability**    | Ensure systems and data are accessible       | Prevent outages and ensure legitimate users can access resources | Redundant servers, load balancing, backups, DDoS protection  |

![CIA (Confidentiality, Integrity & Availability) Model with Diagram](/img/cia-triad.png)

### Opposite of CIA Triad is DAD (Disclosure, Alteration & Destruction)
It's also need to know for security.
| **Component**   | **Meaning**                                             | **Purpose**                  |
| --------------- | ------------------------------------------------------- | ---------------------------- |
| **Disclosure**  | Unauthorized access to information                      | Violates **confidentiality** |
| **Alteration**  | Unauthorized modification of information                | Violates **integrity**       |
| **Destruction** | Unauthorized removal or denial of access to information | Violates **availability**    |

### IAAA (Identification, Authentication, Authorization, and Accountability)
| **Component**      | **Meaning**                                                         | **Purpose**                                   | **Example**                                                 |
| ------------------ | ------------------------------------------------------------------- | --------------------------------------------- | ----------------------------------------------------------- |
| **Identification** | Claiming an identity                                                | Establish *who* the user is                   | Username, user ID, email address                            |
| **Authentication** | Verifying the claimed identity                                      | Ensure the user is who they say they are      | Password, biometric scan, OTP, security token               |
| **Authorization**  | Granting permissions based on authenticated identity                | Control what the user is allowed to do        | Read/write access, admin rights, resource roles             |
| **Accountability** | Tracing actions to a specific identity and holding them responsible | Ensure user actions can be logged and audited | Logs, user activity tracking, audit trails, non-repudiation |

#### Classification with example
1. Identification, example - Your name, username, ID number, employee number, SSN etc.
2. Authentication
   - Type 1 Authentication (passwords, pass phrase, PIN, etc.).
   - Type 2 Authentication (ID, passport, smart card, token, cookie on PC, etc.).
   - Type 3 Authentication (Biometrics, Fingerprint, iris scan, facial geometry, etc.).
3. Authorization, example - it's cover ACL, DAC, MAC, RBAC, ABAC, and RUBAC.
4. Accountability, example - Traces an Action to a Subject's Identity.


### Privacy
In cybersecurity, privacy refers to the rights and control individuals have over their personal information, including how it is collected, used, stored, and shared.

#### Privacy vs Confidentiality
| **Aspect**         | **Privacy**                                        | **Confidentiality**                                |
| ------------------ | -------------------------------------------------- | -------------------------------------------------- |
| **Focus**          | Protecting personal or sensitive information       | Preventing unauthorized access to data             |
| **Concerned With** | Data ownership, user rights, and consent           | Data security and access control                   |
| **Legal Basis**    | Often governed by privacy laws (e.g., GDPR, HIPAA) | Typically enforced by security policies            |
| **Example**        | GDPR compliance, cookie consent                    | Encryption, firewalls, access control lists (ACLs) |

### Risk Management?
Risk management is the process of identifying, assessing, and controlling threats to an organization's digital assets, systems, and data. The goal is to reduce the likelihood and impact of cybersecurity incidents. Risk calculation by following formula;
- `Risk` = `Treat` * `Vulnerability(Likelihood)` Or
- `Risk` = `Treat` * `Vulnerability(Likelihood)` * `Impact`
- `Total Risk` = `Treat` * `Vulnerability(Likelihood)` * `Asset Value`
- `Residual Risk` = `Total Risk` - `Countermeasures`

#### Steps of Cybersecurity Risk Management.
| **Step**                | **Description**                                                           |
| ----------------------- | ------------------------------------------------------------------------- |
| **1. Identify Risks**   | Discover vulnerabilities, threats, assets, and potential attack vectors   |
| **2. Assess Risks**     | Evaluate likelihood and impact `risk = likelihood × impact`               |
| **3. Prioritize Risks** | Rank risks based on criticality and business impact                       |
| **4. Treat Risks**      | Choose mitigation strategy: avoid, transfer, mitigate, or accept the risk |
| **5. Monitor & Review** | Continuously track risk posture and update strategies as threats evolve   |

#### Risk Assessment
- `Qualitative Risk Analysis` – How likely is it to happen and how bad is it if it happens?
- `Quantitative Risk Analysis` – What will it actually cost us in $? This is fact-based analysis, Total $ value of asset, math is involved.

![Risk Assessment Process](/img/risk-assessments.png)

##### Qualitative Risk Analysis with the Risk Analysis Matrix.

![Qualitative Risk Analysis with the Risk Analysis Matrix](/img/risk-analysis-matrix.png)

Where, L = Low, M = Medium, H = High, E = Extreme Risk

#### Risk Treatment Strategies
| **Strategy** | **Meaning**                                 | **Example**                                   |
| ------------ | ------------------------------------------- | --------------------------------------------- |
| **Avoid**    | Eliminate the risk entirely                 | Shut down unused services                     |
| **Transfer** | Shift the risk to a third party             | Buy cybersecurity insurance                   |
| **Mitigate** | Reduce the impact or likelihood of the risk | Implement firewalls, patch systems            |
| **Accept**   | Acknowledge the risk and take no action     | Accept low-risk vulnerability due to low cost |

### (ISC)² Code of Ethics
The (ISC)² Code of Ethics guides the professional behavior of all certified cybersecurity professionals under the (ISC)² organization (e.g., CISSP, SSCP, CCSP). All members and candidates are expected to uphold and promote these ethical standards to protect the public interest, maintain professional integrity, and preserve trust in information systems.

## Domain 2 Business Continuity, Disaster Recovery, and Incident Response

## Domain 3 Access Controls Concepts

## Domain 4 Network Security

## Domain 5 Security Operations


## With Regards, `Jakir`

[![LinkedIn][linkedin-shield-jakir]][linkedin-url-jakir]
[![Facebook-Page][facebook-shield-jakir]][facebook-url-jakir]
[![Youtube][youtube-shield-jakir]][youtube-url-jakir]

### Wishing you a wonderful day! Keep in touch.

<!-- Personal profile -->

[linkedin-shield-jakir]: https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url-jakir]: https://www.linkedin.com/in/jakir-ruet/
[facebook-shield-jakir]: https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white
[facebook-url-jakir]: https://www.facebook.com/jakir.ruet/
[youtube-shield-jakir]: https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white
[youtube-url-jakir]: https://www.youtube.com/@mjakaria-ruet/featured
