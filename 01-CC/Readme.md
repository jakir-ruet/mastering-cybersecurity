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

Security principles are the foundational guidelines used to `design`, `implement`, and `manage` secure systems. This chapter is foundational; all other domains build on it.

**Topics**

- Information Security, IT Security, Cybersecurity
- CIA Triad & IAAA
- Privacy
- Risk & Incident Management
- Access Control
- Governance, Laws, Regulations
- ISC² Ethics

### Information Security, IT Security, Cybersecurity

**Information Security:** All information (paper, voice, data, human knowledge).
**IT Security:** Hard/software + data (servers, networks, computers, firmware).
**Cybersecurity:** IT Security accessible via the internet.

**Summary Table**

| **Term**                 | **Scope**             | **Focus**                                      | **Examples**                                            |
| ------------------------ | --------------------- | ---------------------------------------------- | ------------------------------------------------------- |
| **Information Security** | Broadest              | Protecting all forms of information            | Locking file cabinets, encrypting data, access policies |
| **IT Security**          | Subset of InfoSec     | Securing IT systems and digital infrastructure | Antivirus, firewalls, system hardening, secure login    |
| **Cybersecurity**        | Subset of IT Security | Protecting systems from internet-based threats | Phishing protection, DDoS defense, threat hunting, WAF  |

![Set Subset Diagram of Security](/img/security-sets.png)

### CIA (Confidentiality, Integrity & Availability) Model with Diagram

In cybersecurity and information security, the CIA Triad is a foundational model that outlines the three core principles for protecting information.

#### Confidentiality - Keep data secret

- **Tools:**AES256, SSL/TLS, access control, MFA
- **Threats:** Social engineering, keyloggers, IoT backdoors

#### Integrity - Data is not altered, keep accuiracy

- **Tools:** Checksums, message digests (MD5, SHA1/2), digital signatures
- **Threats:** Code injection, encryption attacks

#### Availability - Data accessible when needed

- **Tools:** IPS/IDS, patch management, redundancy, HA
- **Threats:** DDoS, hardware failure, application failure

| **Component**       | **Meaning**                                  | **Goal**                                                         | **Example**                                                  |
| ------------------- | -------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------ |
| **Confidentiality** | Ensure only authorized users can access data | Prevent unauthorized access, leaks, or spying                    | Using encryption, passwords, and access control lists (ACLs) |
| **Integrity**       | Ensure data is accurate and unchanged        | Prevent unauthorized modification or tampering                   | Checksums, hashes (e.g., SHA-256), digital signatures        |
| **Availability**    | Ensure systems and data are accessible       | Prevent outages and ensure legitimate users can access resources | Redundant servers, load balancing, backups, DDoS protection  |

![CIA (Confidentiality, Integrity & Availability) Model with Diagram](/01-CC/img/domain-1/cia-triad.png)

### Opposite of CIA Triad is DAD (Disclosure, Alteration & Destruction)

- **Disclosure:** Unauthorized access
- **Alteration:** Data changed
- **Destruction:** Data or systems destroyed

It's also need to know for security.

| **Component**   | **Meaning**                                             | **Purpose**                  |
| --------------- | ------------------------------------------------------- | ---------------------------- |
| **Disclosure**  | Unauthorized access to information                      | Violates **confidentiality** |
| **Alteration**  | Unauthorized modification of information                | Violates **integrity**       |
| **Destruction** | Unauthorized removal or denial of access to information | Violates **availability**    |

### IAAA – Identity & Access (Identification, Authentication, Authorization, and Accountability)

- **Identification:** Who you are (username, ID, SSN)
- **Authentication:** Prove it (MFA recommended)
  - **Type 1 (Knowledge):** Passwords, PINs, passphrases
  - **Type 2 (Possession):** ID cards, tokens, single-use passwords
  - **Type 3 (Biometrics):** Fingerprint, iris, face
- **Authorization:** What you can access (DAC, MAC, RBAC, ABAC, Context/Content-based)
- **Accountability:** Track actions → non-repudiation, Traces an Action to a Subject's Identity.

> **Biometric Notes:**

- **Errors:**FRR (False Reject), FAR (False Accept), CER (Crossover Error Rate)
- **Types:** Physiological (fingerprint, iris), Behavioral (typing rhythm, gait)
- **Privacy is critical:** biometrics cannot be “replaced” like passwords

> **Notes**

- **DAC** > Discretionary Access Control
- **MAC** > Mandatory Access Control,
- **RBAC** > Role-Based Access Control,
- **ABAC** > Attribute-Based Access Control

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

In cybersecurity, Human right; protection from unauthorized observation or intrusion. Privacy refers to the rights and control individuals have over their personal information, including how it is collected, used, stored, and shared.

**`General Data Protection Regulation` (GDPR):** It is a comprehensive legal framework enacted by the European Union (EU) that governs how organizations collect, process, and protect the personal data of individuals within the EU and the European Economic Area (EEA).

**Individual Rights Under GDPR**

The regulation grants several key rights to individuals, including:

- **Right to Access:** The right to see what data an organization has about them.
- **Right to Erasure:** Also known as the "right to be forgotten," allowing individuals to ask for their data to be deleted.
- **Right to Portability:** The right to move their data from one service provider to another.
- **Right to Rectification:** The right to have inaccurate personal data corrected.

#### Privacy vs Confidentiality

| **Aspect**         | **Privacy**                                        | **Confidentiality**                                |
| ------------------ | -------------------------------------------------- | -------------------------------------------------- |
| **Focus**          | Protecting personal or sensitive information       | Preventing unauthorized access to data             |
| **Concerned With** | Data ownership, user rights, and consent           | Data security and access control                   |
| **Legal Basis**    | Often governed by privacy laws (e.g., GDPR, HIPAA) | Typically enforced by security policies            |
| **Example**        | GDPR compliance, cookie consent                    | Encryption, firewalls, access control lists (ACLs) |

### Risk Management?

Risk management is the process of identifying, assessing, and controlling threats to an organization's digital assets, systems, and data. The goal is to reduce the likelihood and impact of cybersecurity incidents. Risk calculation by following formula;

- `Risk` = `Threat` x `Vulnerability (Likelihood)` Or
- `Risk` = `Threat` x `Vulnerability (Likelihood)` x `Impact`
- `Total Risk` = `Threat` x `Vulnerability (Likelihood)` x `Asset Value`
- `Residual Risk` = `Total Risk` - `Countermeasures`

**Key Components**

1. `Asset` 👉 Example: database, server, credentials
2. `Threat` 👉 Example: hacker, malware, insider
3. `Vulnerability` 👉 Example: open port, weak password
4. `Impact` 👉 Example: data loss, downtime

#### Risk Lifecycle: Identify → Assess → Respond → Monitor

- **Qualitative:** Likelihood & impact (High/Medium/Low/Extreme)
- **Quantitative:** Assign numeric cost ($), calculate ALE, SLE, TCO
- **Risk Response:** Accept, Mitigate, Transfer, Avoid (Never reject)

**Indicators: In Summary Table**

| Acronym | Full Name                 | Purpose                  | Example                                 |
| ------- | ------------------------- | ------------------------ | --------------------------------------- |
| KPI     | Key Performance Indicator | Tracks ongoing progress  | Number of sales calls per week          |
| KGI     | Key Goal Indicator        | Confirms final outcome   | Total annual revenue target             |
| KRI     | Key Risk Indicator        | Warns of potential risks | Number of cybersecurity breach attempts |

#### Steps of Risk Management

| **Step**                | **Description**                                                           |
| ----------------------- | ------------------------------------------------------------------------- |
| **1. Identify Risks**   | Discover vulnerabilities, threats, assets, and potential attack vectors   |
| **2. Assess Risks**     | Evaluate likelihood and impact `Risk = Likelihood × Impact`               |
| **3. Prioritize Risks** | Rank risks based on criticality and business impact                       |
| **4. Threat Risks**     | Choose mitigation strategy: avoid, transfer, mitigate, or accept the risk |
| **5. Monitor & Review** | Continuously track risk posture and update strategies as threats evolve   |

#### Risk Assessment

Risk Assessment is the process of evaluating risks to determine their likelihood, impact, and priority so organizations can decide how to manage them. `Two` ways measeure risk like

![Risk Assessment Process](/01-CC/img/domain-1/risk-assessments.png)

1. **Qualitative Risk Analysis** It's a subjective method used to `prioritize risks` by `evaluating` their `likelihood` and `impact` using descriptive scales (e.g., `Low`, `Medium`, `High`) rather than numerical data.

**Key Characteristics**

- No complex calculations (unlike ARO, ALE)
- Uses ratings (High/Medium/Low)
- Fast and easy to perform
- Based on expert opinion and experience
- Often visualized using a risk matrix

**Example**

| Risk         | Likelihood | Impact | Risk Level |
| ------------ | ---------- | ------ | ---------- |
| DDoS Attack  | High       | High   | Critical   |
| Data Leak    | Medium     | High   | High       |
| Laptop Theft | Low        | Medium | Medium     |

**Risk Matrix Concept**

| Likelihoods | Low Impact | Medium Impact | High Impact |
| ----------- | ---------- | ------------- | ----------- |
| High        | Medium     | High          | Critical    |
| Medium      | Low        | Medium        | High        |
| Low         | Low        | Low           | Medium      |

**When to Use**

- Early stage risk assessment
- When data is limited
- Quick decision-making needed
- Business-level discussions

1. **Quantitative Risk Analysis** It's a `systematic`, `data-driven` process that evaluates risks by `assigning numerical values`vsuch as monetary `cost`, `time impact`, or `probability` to determine their potential effect on project objectives.

It provides an objective and detailed assessment of risk exposure, particularly in complex environments, by applying analytical techniques such as `Monte Carlo simulation` and `Expected Monetary Value` (EMV).

**Key Quantitative Risk Terms**

| Term                                | Meaning / Formula                                         | Notes                        |
| ----------------------------------- | --------------------------------------------------------- | ---------------------------- |
| **Asset Value (AV)**                | The monetary value of the asset being protected           | E.g., a server worth $50,000 |
| **Exposure Factor (EF)**            | % of asset lost if risk occurs                            | E.g., 25% damage → EF = 0.25 |
| **Single Loss Expectancy (SLE)**    | Monetary loss from a single incident                      | **SLE = AV × EF**            |
| **Annual Rate of Occurrence (ARO)** | Estimated frequency per year a risk may occur             | E.g., 2 times/year → ARO = 2 |
| **Annual Loss Expectancy (ALE)**    | Expected annual monetary loss                             | **ALE = SLE × ARO**          |
| **Risk Score**                      | Could be qualitative (High/Med/Low) or quantitative (ALE) | Helps prioritize risk        |

**Risk Table**

| Asset           | Threat      | AV ($)  | EF (%) | SLE ($) | ARO (per year) | ALE ($) | Notes                         |
| --------------- | ----------- | ------- | ------ | ------- | -------------- | ------- | ----------------------------- |
| Web Server      | DDoS Attack | 50,000  | 20%    | 10,000  | 2              | 20,000  | Could mitigate with WAF       |
| Database        | Ransomware  | 100,000 | 50%    | 50,000  | 0.5            | 25,000  | Backup reduces EF             |
| Employee Laptop | Theft       | 2,000   | 100%   | 2,000   | 1              | 2,000   | Use encryption & policies     |
| Network Switch  | Fire        | 20,000  | 30%    | 6,000   | 0.1            | 600     | Fire suppression reduces risk |

##### Qualitative Risk Analysis with the Risk Analysis Matrix

![Qualitative Risk Analysis with the Risk Analysis Matrix](/01-CC/img/domain-1/risk-analysis-matrix.png)

Where, L = Low, M = Medium, H = High, E = Extreme Risk

##### Qualitative vs Quantitative

| Feature   | Qualitative     | Quantitative  |
| --------- | --------------- | ------------- |
| Data Type | Descriptive     | Numerical     |
| Speed     | Fast            | Slower        |
| Accuracy  | Lower           | Higher        |
| Example   | High/Medium/Low | ARO, SLE, ALE |

**Key Characteristics**

- Data-driven and numerical (cost, time, probability)
- Objective and fact-based
- Uses mathematical/statistical methods (Monte Carlo, EMV)
- Produces measurable outputs (ARO, SLE, ALE)
- Focuses on financial impact
- Detailed and in-depth analysis
- Supports decision-making and budgeting
- Requires time, tools, and reliable data

**When to Use**

- For high-value or critical systems
- When financial impact needs to be measured
- In complex projects with many variables
- When reliable historical data is available
- For strategic and business decisions
- After qualitative risk analysis to refine priorities

#### Risk Threatment Strategies

| **Strategy** | **Meaning**                                 | **Example**                                   |
| ------------ | ------------------------------------------- | --------------------------------------------- |
| **Avoid**    | Eliminate the risk entirely                 | Shut down unused services                     |
| **Transfer** | Shift the risk to a third party             | Buy cybersecurity insurance                   |
| **Mitigate** | Reduce the impact or likelihood of the risk | Implement firewalls, patch systems            |
| **Accept**   | Acknowledge the risk and take no action     | Accept low-risk vulnerability due to low cost |

#### Security Control Categories

1. **Administrative (Managerial) Controls**

- Policies, procedures, guidelines
- Security awareness training
- Risk assessments
- Access control policies

2. **Technical (Logical) Controls**

- Firewalls, IDS/IPS
- Encryption, MFA
- Access control systems
- Antivirus, patch management

3. **Physical Controls**

- Locks, fences, security guards
- CCTV, biometric access
- Alarm systems
- Data center security

4. **Operational Controls**

- Incident response procedures
- Backup and recovery processes
- Change management
- Patch management
- Monitoring and logging
- Job rotation and separation of duties
- Security awareness training
- Data handling procedures

#### Functional Types of Security Controls

- **Preventive Controls** – stop incidents (firewall, access control)
- **Detective Controls** – detect incidents (logs, IDS)
- **Corrective Controls** – fix after incident (backup, patching)
- **Deterrent Controls** – discourage attacks (warning signs)
- **Compensating Controls** – alternative when primary control not possible
- **Recovery Controls** – restore systems (disaster recovery, backups)

#### Access Control Models

| Model                 | Full Name                              | Key Feature / Focus                          | Notes / Example                                                                      |
| --------------------- | -------------------------------------- | -------------------------------------------- | ------------------------------------------------------------------------------------ |
| DAC                   | Discretionary Access Control           | Owner discretion; focus on availability      | Users control access to their own resources                                          |
| MAC                   | Mandatory Access Control               | Labels & clearance; focus on confidentiality | Access based on security labels and clearances                                       |
| RBAC                  | Role-Based Access Control              | Role-based; focus on integrity               | Users assigned roles with specific permissions                                       |
| ABAC                  | Attribute-Based Access Control         | Attributes-based; environment-aware          | Access determined by user, resource, and environment attributes                      |
| Context/Content-based | Context / Content-Based Access Control | Access based on time, location, data content | Example: restricting sensitive data outside office hours or from untrusted locations |

### Governance vs Management

**Governance (C-Level):** Strategy, direction, objectives, risk appetite
**Management:** Execution, risk tolerance, alignment with governance

> **Key C-Level Roles:** `CEO`, `CIO`, `CTO`, `CSO`, `CISO`, `CFO`

### Laws & Regulations

- **Criminal Law:** Society as victim
- **Civil Law:** Individuals as victims
- **Administrative/Regulatory Law:** HIPAA, FDA, FAA, etc.
- **Private Regulations:** PCI-DSS, Contracts
- **Religious & Customary Law:** Region-specific conduct rules

> **Notes**

- `HIPAA` – Health Insurance Portability and Accountability Act.
- `PHI` - Protected Health Information.
- `ECPA` – Electronic Communications Privacy Act.
- `PATRIOT` - Providing Appropriate Tools Required to Intercept and Obstruct Terrorism.
- `CFAA` – Computer Fraud and Abuse Act.
- `PCI-DSS` – Payment Card Industry Data Security Standard.
- `GDPR` – General Data Protection Regulation.
- `FDA` – Food and Drug Administration.
- `FAA` – Federal Aviation Administration.

### ISC2 Code of Ethics

The ISC2 Code of Ethics is a set of `professional` rules and guidelines for `cybersecurity` professionals.

- It defines `how security practitioners should behave in a professional and ethical way`.
- It applies to `everyone` holding ISC2 certifications like `CC`, `SSCP` `CISSP`, etc.
- It ensures actions protect people, organizations, and society while maintaining trust in the cybersecurity profession.

> Key idea: `It’s not just laws—it’s about morality, responsibility, and professionalism in cybersecurity.`

#### The Code has two main parts

1. Preamble - `General Principles`
2. Four Canons - `Core Rules`

##### Preamble - `General Principles`/`Ethical Foundation`

The preamble emphasizes:

- Protecting `society`, `public trust`, and `infrastructure`
- Acting with `honesty`, `justice`, `responsibility`
- Providing `competent` and `diligent service`
- Advancing the `security` profession

> In simple terms: `Use your cybersecurity skills for good — not harm.`

##### Four Canons - `Core Rules`

###### Canon 1: Protect Society, the Common Good, Public Trust, and Infrastructure

**Meaning:** This is the `highest priority`. Always think about impact on `people` and `society`.

**Key Responsibilities**

- Avoid actions that could harm public systems
- Report security vulnerabilities responsibly
- Do not exploit systems for personal gain
- Protect critical infrastructure (banks, hospitals, govt systems)

> Real-world Example
If you discover a vulnerability in a banking system → report it responsibly (not exploit it)

###### Canon 2: Act Honorably, Honestly, Justly, Responsibly, and Legally

**Meaning:** Be ethical and lawful in all actions.

**Key Responsibilities**

- Follow laws and regulations
- Do not engage in hacking without authorization
- Avoid conflicts of interest
- Be truthful in reports and communications

> Real-world Example

- Do not falsify security audit results
- Do not access systems without permission

###### Canon 3: Provide Diligent and Competent Service to Principals

**Meaning:** Do your job `properly` and `professionally`. 👉 `Principals` = your employer, client, or organization

**Key Responsibilities**

- Maintain and improve your skills
- Give accurate advice
- Protect client data
- Deliver quality work

> Real-world Example
If you are designing a security system → use best practices, not shortcuts

###### Canon 4: Advance and Protect the Profession

**Meaning:** Help improve the cybersecurity field

**Key Responsibilities**

- Share knowledge
- Support ethical behavior
- Avoid damaging the reputation of cybersecurity professionals
- Mentor others

> Real-world Example

- Contribute to open-source security tools
- Help juniors learn security concepts

##### Easy Way to Remember `Mnemonic: 'SHDP'`

| Canon | Mnemonic | Focus      | Key Idea             |
| :---: | :------: | ---------- | -------------------- |
|   1   |    S     | Society    | Protect people first |
|   2   |    H     | Integrity  | Be legal & honest    |
|   3   |    D     | Work       | Do your job well     |
|   4   |    p     | Profession | Improve the field    |

## Domain 2 Business Continuity Plan `BCP`, Disaster Recovery Plan `DRP`, and Incident Response

### Business Continuitity Plan

This is the process of creating the long term stategic business plans, sub-plans, policies and procedures for conitinued operation after a distruptive event.

![Business Continuitity Plan](/01-CC/img/domain-2/business-continuitity-plan.png)

#### Continuty of Operations Plan `COOP`

#### Crisis Communications Plan `CCP`

![Crisis Communications Plan](/01-CC/img/domain-2/crisis-communications-plan.png)

#### Cyber Incident Response Plan `CIRO`

#### Ocucupant Emergency Plan `OEP`

#### Business Recevery Plan `BRP`

#### Continuity of Support Plan `CSP`

#### Crise Management Plan `CMP`

### Disater Recovery Plan

It's a lifecycle of mitigation, preparation, response and recover through IT system.

![Disater Recovery Plan](/01-CC/img/domain-2/disater-recovery-plan.png)

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

![Subscription/Cloud Site](/01-CC/img/domain-2/subscription-cloud-site.png)

##### Mobile Site

##### Lessions Learned

### Incident Management

It's monitoring and detecting security events on our systems and how we react in those events.

![Incident Management](/01-CC/img/domain-2/incident-management.png)

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

![OSI Model](/01-CC/img/domain-4/osi-model.png)

![TCP/IP Model](/01-CC/img/domain-4/tcp-ip-model.png)

## Domain 4 Network Security

## Domain 5 Security Operations
