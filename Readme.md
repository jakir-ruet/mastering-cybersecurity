## More About Me – [Take a Look!](http://www.mjakaria.me)

### ISC2

`International Information System Security Certification Consortium` is a globally recognized cybersecurity organization that provides professional certifications, training, and standards for information security.

1. Certified in Cybersecurity `CC` - Begineer Level
2. Systems Security Certified Practitioner `SSCP` - Intermediate Level
3. Certified Information Systems Security Professional `CISSP` - Advanced Level

### Welcome to Certified in Cybersecurity `CC` - Begineer Level

The Certified in Cybersecurity (CC) is an entry-level cybersecurity certification offered by ISC2. Those are the official 5 domains of the Certified in Cybersecurity (CC) from ISC2.

| Domain       | Name                                                          | Weight |
| ------------ | ------------------------------------------------------------- | ------ |
| **Domain 1** | Security Principles                                           | ~26%   |
| **Domain 2** | Business Continuity, Disaster Recovery, and Incident Response | ~10%   |
| **Domain 3** | Access Control Concepts                                       | ~22%   |
| **Domain 4** | Network Security                                              | ~24%   |
| **Domain 5** | Security Operations                                           | ~18%   |

## Domain 1 `Security Principles`

Security principles are the foundational guidelines used to `design`, `implement`, and `manage` secure systems.

### Related Security Terms in Table & Diagram

| **Term**                 | **Scope**             | **Focus**                                      | **Examples**                                            |
| ------------------------ | --------------------- | ---------------------------------------------- | ------------------------------------------------------- |
| **Information Security** | Broadest              | Protecting all forms of information            | Locking file cabinets, encrypting data, access policies |
| **IT Security**          | Subset of InfoSec     | Securing IT systems and digital infrastructure | Antivirus, firewalls, system hardening, secure login    |
| **Cybersecurity**        | Subset of IT Security | Protecting systems from internet-based threats | Phishing protection, DDoS defense, threat hunting, WAF  |

![Set Subset Diagram of Security](/img/security-sets.png)

### CIA (Confidentiality, Integrity & Availability) Model with Diagram

In cybersecurity and information security, the CIA Triad is a foundational model that outlines the three core principles for protecting information.

#### Confidentiality

#### Integrity

#### Availability

| **Component**       | **Meaning**                                  | **Goal**                                                         | **Example**                                                  |
| ------------------- | -------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------ |
| **Confidentiality** | Ensure only authorized users can access data | Prevent unauthorized access, leaks, or spying                    | Using encryption, passwords, and access control lists (ACLs) |
| **Integrity**       | Ensure data is accurate and unchanged        | Prevent unauthorized modification or tampering                   | Checksums, hashes (e.g., SHA-256), digital signatures        |
| **Availability**    | Ensure systems and data are accessible       | Prevent outages and ensure legitimate users can access resources | Redundant servers, load balancing, backups, DDoS protection  |

![CIA (Confidentiality, Integrity & Availability) Model with Diagram](/img/domain-1/cia-triad.png)

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
- `Risk` = `Treat` *`Vulnerability(Likelihood)`* `Impact`
- `Total Risk` = `Treat` *`Vulnerability(Likelihood)`* `Asset Value`
- `Residual Risk` = `Total Risk` - `Countermeasures`

#### Steps of Cybersecurity Risk Management

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

![Risk Assessment Process](/img/domain-1/risk-assessments.png)

##### Qualitative Risk Analysis with the Risk Analysis Matrix

![Qualitative Risk Analysis with the Risk Analysis Matrix](/img/domain-1/risk-analysis-matrix.png)

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

## Domain 2 Business Continuity Plan `BCP`, Disaster Recovery Plan `DRP`, and Incident Response

### Business Continuitity Plan

This is the process of creating the long term stategic business plans, sub-plans, policies and procedures for conitinued operation after a distruptive event.

![Business Continuitity Plan](/img/domain-2/business-continuitity-plan.png)

#### Continuty of Operations Plan `COOP`

#### Crisis Communications Plan `CCP`

![Crisis Communications Plan](/img/domain-2/crisis-communications-plan.png)

#### Cyber Incident Response Plan `CIRO`

#### Ocucupant Emergency Plan `OEP`

#### Business Recevery Plan `BRP`

#### Continuity of Support Plan `CSP`

#### Crise Management Plan `CMP`

### Disater Recovery Plan

It's a lifecycle of mitigation, preparation, response and recover through IT system.

![Disater Recovery Plan](/img/domain-2/disater-recovery-plan.png)

#### Business Impact Plan `BIA`

##### Recovery Time Objective `RTO`

##### Work Recovery Time `WRT`

##### Mean Time Between Failures `MTBF`

##### Mean Time to Repair `MTTR`

##### Minimum Operationg Requirements `MOR`

#### Recovery Point Objective `RPO`

#### Recovery Strategies

##### Redundant Site

##### Hot Site

##### Warm Site

##### Cold Site

##### Reciprocal Agreement Site

##### Subscription/Cloud Site

![Subscription/Cloud Site](/img/domain-2/subscription-cloud-site.png)

##### Mobile Site

##### Lessions Learned

### Incident Management

It's monitoring and detecting security events on our systems and how we react in those events.

![Incident Management](/img/domain-2/incident-management.png)

- Event - An observe change in state
- Alerts - Triggers warnings if certain event happens
- Inconvenience (Non-disasters) - Non-distruptive failures
- Emergency (Criis) - Urgent
- Disaster - Our entire facility is unusable for 24 hours/longer
- Catastrophe - Our facility is destroyed

#### Natural Incident Management

#### Human Incident Management

#### Environmental Incident Management

> Not to be confsed with natural disasters

#### Computer/Cyber Incident Response Tea `CIRT`

##### Senior Management

##### Incident Manager

##### Technical Leads and Teams

##### IT Security

##### PR, Human Resource (HR) and Legal

##### Auditors IT/Financial

## Domain 3 Access Controls Concepts

### Access Controls Concepts

#### Administrative (Directive) Controls

Organizational policies and procedures

#### Physical Controls

Locks, Fences, Guards, Dogs, Gates, Bollards

#### Technical Controls

Hardware, Software, Fireware, Firewalls, Routers, Encryptions

## Domain 4

### Network Security

![OSI Model](/img/domain-4/osi-model.png)

![TCP/IP Model](/img/domain-4/tcp-ip-model.png)

## Domain 4 Network Security

## Domain 5 Security Operations

## With Regards, `Jakir`

[![LinkedIn][linkedin-shield-jakir]][linkedin-url-jakir]
[![Facebook-Page][facebook-shield-jakir]][facebook-url-jakir]
[![Youtube][youtube-shield-jakir]][youtube-url-jakir]

### Wishing you a wonderful day! Keep in touch

<!-- Personal profile -->

[linkedin-shield-jakir]: https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url-jakir]: https://www.linkedin.com/in/jakir-ruet/
[facebook-shield-jakir]: https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white
[facebook-url-jakir]: https://www.facebook.com/jakir.ruet/
[youtube-shield-jakir]: https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white
[youtube-url-jakir]: https://www.youtube.com/@mjakaria-ruet/featured
