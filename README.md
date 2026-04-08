# SOC L1 Journey

## SOC FUNDAMENTALS:-

A **SOC** (**S**ecurity **O**perations **C**enter) is a dedicated facility operated by a specialized security team. This team aims to continuously monitor an organization’s network and resources and identify suspicious activity to prevent damage. This team works 24 hours a day, seven days a week.

**Your Daily Duties**

As a Junior Security Analyst, also called a SOC Level 1 Analyst, you work in a 24/7 SOC team and mostly review the security alerts together with your colleagues. To do it efficiently, you will need practice and skills learned through this path. During your work shift, you would typically:

- Monitor and investigate various security alerts
- Participate in  brainstorms and workshops
- Cooperate with other teams to keep your company safe
- Constantly learn and discover new attacks and defenses

The main focus of the SOC team is to keep **Detection** and **Response** intact. The SOC team has some resources available in the form of security solutions that help them achieve this. These solutions integrate the whole company’s network and all the systems to monitor them from one centralized location. Continuous monitoring is required to detect and respond to any security incident.

![image.png](images/image.png)

**Detection:-**

- Detect vulnerabilities
- Detect unauthorized activity
- Detect policy violations
- Detect intrusions

**Response:-**

- **Support with the incident response**

![image.png](images/image%201.png)

- The **People** are known as the SOC team. This team has the following roles and responsibilities.

![image.png](images/image%202.png)

- Each role has its own **Processes**, just as we saw the role of Level 1 SOC Analysts as the first responders to carry out alert triage and determine if it is harmful. Let’s discuss some important processes involved in a SOC.

![image.png](images/image%203.png)

- The **Technology** portion in the SOC pillars refers to the security solutions. These security solutions efficiently minimize the SOC team's manual effort to detect and respond to threats.
- Example:-EPP, IDS/IPS, XDR, SOAR, and more.

## **Scenario**

You are the Level 1 Analyst of your organization’s SOC team. You receive an alert that a port scanning activity has been observed on one of the hosts in the network. You have access to the SIEM solution, where you can see all the associated logs for this alert. You are tasked to view the logs individually and answer the question to the 5 Ws given below.

**Note**: The vulnerability assessment team notified the SOC team that they were running a port scan activity inside the network from the host: `10.0.0.8`

| **Case** | **Actual Situation** | **SIEM Alert** | **Example in Your Scenario** | **Conclusion** |
| --- | --- | --- | --- | --- |
| **True Positive (TP)** | Real malicious port scan | Alert generated | Unknown attacker scanning network | ✅ Correct detection |
| **False Positive (FP)** | Legitimate activity | Alert generated | Vulnerability team (IP: 10.0.0.8) scanning | ❌ Benign but flagged |
| **True Negative (TN)** | No attack | No alert | Normal network traffic | ✅ Correctly ignored |
| **False Negative (FN)** | Real malicious port scan | No alert | Attacker scans but SIEM misses it | ❌ Missed threat |

Scenario Answer

| **Observed Activity** | **Source IP** | **Reality** | **Alert Status** | **Result** |
| --- | --- | --- | --- | --- |
| Port Scan | 10.0.0.8 | Authorized (Vuln Team) | Alert Triggered | **False Positive** |

Easy Way to Remember

- True = Correct
- False = Wrong
- Positive = Predicted YES
- Negative = Predicted NO

## **Security Hierarchy**

Cyber security priorities are different for every company. For law firms, the goal is the privacy of the legal documents. For factories, the availability of production lines. For hospitals, patient safety. That's why every company has a unique security approach and security team structure. Let's take a look at the high-level example of it:

![image.png](images/image%204.png)

Blue Team is about defensive security, meaning it constantly monitors for attacks and tries to respond to them quickly. Depending on a company's size and sector, Blue Team can include a lot of different roles and subdepartments, usually counting 3 to 50 members total. Now, let's explore the most common Blue Team departments.

![image.png](images/image%205.png)

- **L1 Analysts**: Junior members who triage alerts and pass complex cases to L2
- **L2 Analysts:** Experienced members who investigate more advanced attacks
- **Engineers**: Experts in configuring security tools like  EDR or SIEM
- **Manager**: A person who manages the whole SOC  team
    
    ## **Cyber Incident Response Team (CIRT)**
    

![image.png](images/image%206.png)

**Specialized Defensive Roles**

![image.png](images/image%207.png)

## **Internal SOC vs MSSP**

| **Topic** | **Internal SOC** | **MSSP** |
| --- | --- | --- |
| **ScenarioExample** | You work in a SOC team of the bank and protect the bank's systems | You work for a global MSSP protecting its sixty customers in Europe |
| **WorkingPace** | You usually have calm shifts without too much time pressure | Your shift usually starts from a queue of urgent alerts to analyze |
| **SecurityTools** | You work with just a few tools, but need to know them very well | You have to work with sixty diverse security tools and platforms |
| **IncidentPractice** | You saw and learned from just two major cyber attacks last year | Every week, you deal with attacks and breaches, and can learn from it |

## **Next Steps**

Your most natural next step after L1 is to become a SOC L2 analyst, but you are free to choose another path! While handling a SIEM alert, you might notice that engineering work appeals to you more. During a cyber attack, you may be fascinated by CIRT actions. You may also find yourself well-suited as a manager and build your path to the CISO role. No matter what, your first year or two is to get real work experience, and to spend this time effectively, follow the tips below!

![image.png](images/image%208.png)

## **Humans as Attack Vectors**

**Attacks on Humans**

- Social Engineering attacks
    - Pishing
    - Malware Downloads
    - Deepfakes
    - Impersonation

**Defending Humans**

Defending against threats involves two key tasks: **Mitigation** and **Detection**. Mitigation aims to prevent or reduce the chance and impact of attacks, for example by training employees or deploying a good anti-phishing solution. However, no matter how good mitigation measures are, one day they are bypassed. That's where your SOC skills are vital to detect and investigate advanced attacks that slip through

![image.png](images/image%209.png)

- **Mitigation**
    - **Anti-phishing solution**
    - **Antivirus / EDR solution**
    - **"Trust but verify" principle**
    - **Security awareness training**

## **Systems as Attack Vectors**

**Definition of System**
Where do the banks store your cards, or where are your emails stored? The answer - on a system: a physical server, a virtual machine, or a cloud platform like Microsoft 365. Protecting such systems is crucial: if the attackers breach one user's mailbox via phishing, they compromise a single mailbox, but if they breach a mail server, they now control all thousands of mailboxes. Each system type can have a different value for threat actors, for example:

| **Breached System** | **Attack Value** |
| --- | --- |
| A personal laptop of a school student | Steal Steam profile and add the PC to a botnet |
| A laptop of the bank's senior IT administrator | Get access to the internal banking systems |
| A mail server of a criminal law company | Dump all mailboxes and blackmail the victim |
| A server at the heart of an industrial network | Encrypt the whole network with ransomware |
| A government website management panel | Damage the website content ([defacement(opens in new tab)](https://en.wikipedia.org/wiki/Website_defacement) / activism) |

**Attack on Systems**

- Human-Led Attacks
- Vulnerabilities
    - Software Vulnerabilities
- Supply Chain
- Misconfigurations

**Software Vulnerabilities :**

Every piece of software has flaws, but some take years to be discovered. For example, [Shellshock(opens in new tab)](https://www.invicti.com/blog/web-security/cve-2014-6271-shellshock-bash-vulnerability-scan/), a major Linux vulnerability, existed since 1992 but wasn't found until 2014. In the worst-case scenario, attackers discover the vulnerability before anyone else. This is known as a [zero-day(opens in new tab)](https://en.wikipedia.org/wiki/Zero-day_vulnerability), and only your SOC skills can determine whether it gets detected in time.

Once a vulnerability is made public, it is assigned a Common Vulnerabilities and Exposures ([CVE](https://www.cvedetails.com/cisa-known-exploited-vulnerabilities/kev-1.html)) number. From that moment, it's a race: attackers develop exploits while defenders rush to update their systems. Here is the timeline of how Windows vulnerabilities evolve every year:

![image.png](images/image%2010.png)

Responding to Vulnerabilities

An answer to a CVE is always **a patch** - an update supplied by the software vendor. Even for zero-days, you'll have to wait for a patch, vigilantly monitor for exploitation traces, and try to survive the stressful period before the patch is released. For example, by:

- Restricting access to the system to only trusted ip’s
- Applying temporary measures provided by the vendor
- Blocking known attack patterns on  WAF or IPS

Misconfigurations

On the other hand, a misconfiguration isn't a bug in the software but a mistake in how the system was set up, often by the IT team. These errors happen frequently, usually to make things simpler, like using "1111" instead of typing a long password every time. Let's take a look at some real-world examples.

- How ["123456" password](https://www.bleepingcomputer.com/news/security/123456-password-exposed-chats-for-64-million-mcdonalds-job-chatbot-applications/) exposed chats for 64 million McDonald's job applications
- How a [misconfigured AWS cloud](https://www.bleepingcomputer.com/news/security/capital-one-data-breach-affects-106-million-people-suspect-arrested/#:~:text=intrusion%20occurred%20through%20a%20misconfigured%20web%20application%20firewall) resulted in a breach of 106 million bank customers
- How improperly configured [smart fridges](https://www.sectigo.com/resource-library/when-refrigerators-attack-how-cyber-criminals-infect-appliances-and-how-manufacturers-can-stop-them) are silently used in full-scale botnet attacks

| **Mitigation** | **Description** |
| --- | --- |
| **Patch Management** | A process of tracking and patching the vulnerable systems significantly reduces the chance of a successful attack |
| **Training for IT** | If your IT knows the risks of misconfigurations, they are less likely to leave the systems unprotected |
| **Network Protection** | The system is much harder to breach if access to it is restricted to trusted people or IP addresses |
| **Antivirus Protection** | Same as with attacks on humans, a good antivirus can stop or at least detect many different attacks |

## Rooms 


- [SOC Metrics and Objectives](rooms/SOC%20Metrics%20and%20Objectives/SOC%20Metrics%20and%20Objectives.md)
- [SOC Workbooks and Lookups](rooms/SOC%20Workbooks%20and%20Lookups/SOC%20Workbooks%20and%20Lookups.md)
- [SOC L1 Alert Triage Guide](rooms/SOC-L1-Alert-Triage/SOC-L1-Alert-Triage.md)
- [SOC-L1-Alert-Reporting](rooms/SOC-L1-Alert-Reporting/SOC-L1-Alert-Reporting.md)
  
