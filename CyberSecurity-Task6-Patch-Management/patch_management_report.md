# Patch Management Report

## Contents

- [Introduction](#introduction)
- [Why Patches Matter](#why-patches-matter)
  - [Discovery](#a-discovery)
  - [Reporting Through CVEs](#b-reporting-through-cves)
  - [Exploitation](#c-exploitation)
  - [Real-World Case Studies](#real-world-case-studies)
- [Consequences of Not Patching](#consequences-of-not-patching)
- [Patch Management Lifecycle](#patch-management-lifecycle)
- [Best Practices for Patch Management](#best-practices-for-patch-management)
- [Challenges in Patch Management](#challenges-in-patch-management-and-how-to-overcome-them)
- [References](#references)

## Introduction

To someone who is not an information technology enthusiast, patching simply means repairing or fixing something, like an outfit or a tyre. But in the technological space, patching refers to the process of identifying, prioritising, acquiring, installing, and verifying the installation of patches, updates, and upgrades throughout an organisation.

So, every time you press the "Download All Updates" button or restart your system after an installation, you are participating in the patching process. In a way, you are helping to fix the holes and flaws in your system. But cybersecurity takes it a step further. In the digital world we live in today, not everything is legitimate or comes from a trusted source. Even software updates need to be verified to ensure they are authentic and have not been tampered with. Therefore, patching does not only involve downloading updates, but also identifying the appropriate updates and ensuring they are trustworthy before installation.

Patch management is the process of addressing known vulnerabilities by managing the acquisition, installation, and verification of suitable patches. Within the vulnerability lifecycle, it plays an important role in fixing security weaknesses that attackers could otherwise exploit.

In this report, I will explain what patch management is, why unpatched systems represent one of the largest attack surfaces in cybersecurity, and how organisations can implement an effective patching strategy.

## Why Patches Matter

To understand why patches matter, we first have to understand how vulnerabilities are discovered, reported, and exploited.

### A. Discovery

A software vulnerability is a weakness in an application, operating system, or other technology that could affect its security. Vulnerabilities may be discovered by software developers, security researchers, independent testers, or attackers. Sometimes, someone may stumble upon a vulnerability while using a system. In other cases, people intentionally examine and test systems to identify weaknesses, either to fix them or potentially exploit them in an attack.

### B. Reporting Through CVEs

CVE stands for Common Vulnerabilities and Exposures. It provides standard identifiers for publicly disclosed vulnerabilities, allowing security teams and organisations to refer to the same issue consistently.

There is also CVSS, which stands for Common Vulnerability Scoring System. It provides severity scores to help communicate how serious a vulnerability may be. These scores help organisations prioritise vulnerabilities and decide which ones require more urgent attention.

### C. Exploitation

Exploitation happens when someone takes advantage of a vulnerability to perform an unauthorised action. Depending on the weakness, this might allow an attacker to access information, execute code, or compromise a system.

Once a vulnerability becomes known, attackers may also learn about it and attempt to exploit systems that remain vulnerable. If a patch is released but an organisation fails to install it, the affected systems may remain exposed to attacks that the patch was designed to prevent. This is why identifying vulnerabilities is only part of the job. Organisations must also prioritise and apply appropriate fixes.

### Real-World Case Studies

These two examples demonstrate the consequences of failing to patch vulnerabilities and the importance of an effective patch management strategy.

#### Case Study 1: WannaCry Ransomware (2017)

Microsoft released security update MS17-010 on 14 March 2017 to address vulnerabilities in Windows SMBv1. The WannaCry ransomware outbreak began on 12 May 2017, exploiting a vulnerability addressed by that update to spread among vulnerable systems.

Many affected computers had not installed the available security update. The outbreak demonstrated how delayed patching could leave systems exposed to malware capable of spreading across networks.

> **Lesson:** Organisations should prioritise critical security updates and verify that vulnerable systems have been patched, especially when a vulnerability can be exploited to spread malware.

#### Case Study 2: Equifax Data Breach (2017)

In 2017, attackers exploited a vulnerability in the Apache Struts web application framework to gain access to Equifax's systems. The breach exposed personal information belonging to approximately 147 million people, according to commonly reported figures. The U.S. Government Accountability Office documented access to information belonging to at least 145.5 million individuals.

The GAO found that Equifax failed to properly identify the vulnerable application. An outdated notification list meant the relevant administrators did not receive the vulnerability notice, and a subsequent scan also failed to detect the weakness.

> **Lesson:** Having a patch available is not enough. Organisations also need accurate records of their systems, effective communication about security updates, reliable vulnerability scanning, and verification that patches have been successfully applied.

## Consequences of Not Patching

### 1. Data Breaches

When an organisation fails to patch a known vulnerability, attackers may exploit that weakness to gain unauthorised access to its systems or data. IBM's *2025 Cost of a Data Breach Report* found that the average global cost of a data breach was **US$4.44 million**. This includes costs associated with responding to and recovering from a breach. However, this figure represents an average across the breaches studied, not the cost of every incident or specifically those caused by unpatched systems.

### 2. Ransomware Attacks

Ransomware can prevent an organisation from accessing its files or systems, disrupting services and potentially causing data loss. Unpatched vulnerabilities can provide attackers with a way into systems, although ransomware can also spread through other methods. Verizon's *2025 Data Breach Investigations Report* found that ransomware was present in **44% of the breaches analysed**. The report also found that exploitation of vulnerabilities as an initial access method increased by **34%** compared with the previous year's report. These findings highlight the importance of vulnerability management and timely patching. However, the ransomware statistic does not mean that 44% of breaches were caused by missing patches.

### 3. Compliance Violations

Organisations may have legal and regulatory obligations to protect personal information and maintain appropriate security measures. Failing to apply necessary security updates can contribute to non-compliance if it leaves systems inadequately protected. For example, Ghana's *Data Protection Act, 2012 (Act 843)* requires data controllers to take appropriate and reasonable technical and organisational measures to protect personal data. These measures must also be reviewed and updated as necessary to address new risks.

### 4. Financial Penalties and Recovery Costs

A cyber incident can cost an organisation money through investigations, recovery, legal expenses, lost business, and regulatory penalties where applicable. For example, the European Union's General Data Protection Regulation (GDPR) allows fines of up to **€20 million or 4% of an organisation's total worldwide annual turnover, whichever is higher**, for certain infringements. This is a maximum penalty, not an automatic fine for failing to patch. The applicable penalty depends on the infringement and the circumstances of the case.

## Patch Management Lifecycle

Patch management is not just about downloading and installing updates. There are different stages an organisation has to go through to make sure the right patches are installed properly and that they actually solve the problem they are meant to solve.

### 1. Discovery

This is the first stage, where an organisation identifies the systems, applications, and devices it uses and checks which ones need updates. This helps the IT team know what they are working with and identify systems that may have security weaknesses or missing patches. After all, you cannot fix a problem you do not know exists.

### 2. Assessment

After identifying systems that need updates, the next step is to assess the available patches and determine how urgent they are. Not every vulnerability carries the same level of risk. The IT team considers factors such as the severity of the vulnerability, whether attackers are already exploiting it, and how important the affected system is to the organisation. This helps them decide which patches should be prioritised.

### 3. Testing

Before installing patches across an organisation, it is important to test them to make sure they work as expected and do not cause other problems. Sometimes an update can affect how an application works or create compatibility issues with other software. Testing helps the IT team identify these problems before rolling out the patch to everyone.

### 4. Deployment

Once a patch has been assessed and tested, it can be installed on the affected systems. The IT team decides how and when to deploy it, taking into consideration the urgency of the patch and the possible disruption to users. Critical security patches may need to be installed more urgently than routine updates. However, deployment should still be properly managed to avoid unnecessary downtime or other issues.

### 5. Verification

Installing a patch does not automatically mean the job is done. The final stage is to verify that the patch was installed successfully and that the affected vulnerability has been addressed. The IT team may check the system's update status or scan it again to confirm that it is no longer vulnerable to the issue. If the patch failed to install or some systems were missed, further action will be needed.

## Best Practices for Patch Management

For an organisation to have an effective patch management strategy, it is not enough to install updates whenever they become available. There has to be a proper process in place to ensure that the right updates are installed at the right time. The following are seven practices organisations can adopt.

### 1. Keep an Updated Inventory of All Systems

The first step is to know the systems, applications, and devices an organisation uses. This makes it easier to identify which systems need updates and prevents devices from being overlooked during the patching process.

### 2. Prioritise Critical Security Patches

Not every patch requires the same level of urgency. Organisations should prioritise patches that address severe vulnerabilities, especially those that are already being exploited by attackers. This helps ensure that the most dangerous weaknesses are addressed first.

### 3. Monitor for New Vulnerabilities and Updates

Organisations should regularly check for security advisories, software updates, and newly discovered vulnerabilities. This allows the IT team to identify relevant patches early instead of waiting until a problem occurs.

### 4. Obtain Patches from Trusted Sources

Before installing an update, organisations should ensure that it comes from a legitimate source and has not been tampered with. This is important because installing a malicious or compromised update could introduce new security problems instead of fixing existing ones.

### 5. Test Patches Before Wide Deployment

Where appropriate, patches should first be tested on a small group of systems to identify possible compatibility issues or unexpected problems. This reduces the risk of an update disrupting important applications or services when it is installed across the organisation.

### 6. Automate Routine Patching Where Appropriate

Organisations can use patch management tools to identify missing updates, schedule installations, and manage updates across multiple devices. Automation can reduce manual work and help ensure that systems are not forgotten. However, it should be monitored to make sure updates are installed successfully.

### 7. Verify and Document Every Update

After installing patches, organisations should confirm that the updates were successful and that the relevant vulnerabilities have been addressed. They should also keep records of what was patched, when it was patched, and which systems still require attention. This helps with future maintenance, troubleshooting, and security audits.

## Challenges in Patch Management and How to Overcome Them

Even though patching is important, organisations may face challenges that prevent them from installing updates as quickly as they should. Some of these challenges are explained below, along with ways to address them.

### 1. Legacy Systems

Some organisations still rely on old systems or applications that may no longer receive security updates. In other cases, a new patch may not be compatible with older software or hardware. This makes it difficult to fix vulnerabilities without affecting other operations.

**How to overcome it:** Organisations should identify unsupported systems and plan to upgrade or replace them where possible. If replacement cannot happen immediately, they can apply suitable temporary security measures, restrict access to the vulnerable systems, and monitor them closely.

### 2. Downtime Concerns

Installing patches may require restarting systems or temporarily taking services offline. For organisations that depend on their systems throughout the day, this can disrupt operations and affect users. As a result, some organisations may delay updates to avoid interruptions.

**How to overcome it:** Organisations can schedule routine updates during maintenance periods when fewer people are using the systems. They should also plan for critical updates carefully and communicate expected interruptions to affected users. Where possible, systems can be updated in stages to reduce disruption.

### 3. Testing Requirements

Patches can sometimes introduce bugs, compatibility issues, or unexpected changes to how applications work. Organisations may therefore spend time testing updates before installing them widely. However, lengthy testing can leave vulnerable systems exposed for longer than necessary.

**How to overcome it:** Organisations should establish a clear testing process that considers the urgency of each patch. Critical security updates should receive priority, while routine updates can follow the normal testing schedule. Where appropriate, testing can begin in a controlled environment before the patch is deployed more widely.

### 4. Limited Resources and Staff

Some organisations do not have enough IT staff, time, or funding to monitor every system and install updates promptly. When many devices and applications require attention, it can become difficult to keep track of everything.

**How to overcome it:** Organisations can use patch management tools to automate routine tasks, maintain an accurate inventory of their systems, and prioritise the most serious vulnerabilities. They should also assign clear responsibility for patching so that important updates are not overlooked.

### 5. Remote and Unmanaged Devices

Devices used outside an organisation's network may not always connect to its patch management systems. Some employees may also postpone updates, leaving their devices vulnerable even when patches are available.

**How to overcome it:** Organisations can use centralised device management tools to monitor update status and apply security policies to remote devices. They should also educate employees on the importance of installing updates promptly and provide a way for IT teams to identify devices that remain unpatched.

## References

1. Souppaya,      M., & Scarfone, K. (2022). *Guide to Enterprise Patch Management      Planning: Preventive Maintenance for Technology* (NIST Special      Publication 800-40 Rev. 4). National Institute of Standards and      Technology. [https://doi.org/10.6028/NIST.SP.800-40r4](https://doi.org/10.6028/NIST.SP.800-40r4)
2. Cybersecurity      and Infrastructure Security Agency. (n.d.). *Known Exploited      Vulnerabilities Catalog*. [https://www.cisa.gov/known-exploited-vulnerabilities-catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
3. CVE      Program. (n.d.). *Common Vulnerabilities and Exposures (CVE)*. [https://www.cve.org/](https://www.cve.org/)
4. National      Institute of Standards and Technology. (n.d.). *National Vulnerability      Database: Vulnerability Detail Pages*. [https://nvd.nist.gov/vuln/Vulnerability-Detail-Pages](https://nvd.nist.gov/vuln/Vulnerability-Detail-Pages)
5. Microsoft.      (2017, March 14). *Microsoft Security Bulletin MS17-010: Critical*.      Microsoft Learn. [https://learn.microsoft.com/en-us/security-updates/Securitybulletins/2017/ms17-010](https://learn.microsoft.com/en-us/security-updates/Securitybulletins/2017/ms17-010)
6. U.S.      Government Accountability Office. (2018, August 30). *Data Protection:      Actions Taken by Equifax and Federal Agencies in Response to the 2017      Breach* (GAO-18-559). [https://www.gao.gov/products/gao-18-559](https://www.gao.gov/products/gao-18-559)
