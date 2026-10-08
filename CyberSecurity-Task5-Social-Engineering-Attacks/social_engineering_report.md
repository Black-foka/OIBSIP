# Social Engineering Attacks

## Introduction

In this current technological climate, there are so many ways an attacker can try to break into your system to do anything from gaining access to sensitive information to uploading malicious software onto your system. A group of these have been termed Social Engineering because these group of techniques rely on acceptable social interactions to manipulate user to achieve their desired outcome instead of technically breaking into the system itself.

NIST defines social engineering as **deceiving an individual into revealing sensitive information, obtaining unauthorized access, or committing fraud by gaining the person's trust**.

This means that the main component of a successful social engineering attack is the people or users themselves. It can only work if the attack is able to successful gain the trust of the user and that user intend would knowing or unknowing grant the attacker access to launch the attack on the individual or the larger organization is general.

These groups of attacks are high effective because of its helps the attack by pass the demanding and usually difficult process of breaking into the system technically, they instead manipulate an unexpecting user. SANS' **2025 Security Awareness Report** surveyed more than **2,700 security awareness practitioners from over 70 countries**. In that survey, **80% of organizations identified social engineering as their number-one human-related risk**. SANS also reported that phishing remained the leading social-engineering threat; while smishing and vishing were increasing in frequency and sophistication.

In this report, I am going to touch on some of the most well used social engineering tactics like phishing, pretexting, baiting and quid pro quo, how it works and their various prevention to help teach a little something that can be vital to you.

---

## 1. Phishing

Phishing is simply the use of deceptive emails and other various messages to trick a user into opening a harmful link or downloading malicious files onto a system.

### 1.1 How It Works

Since this is not a technical break-in but a social one, there is no technical breakdown of how it actually works. However, CISA provides a breakdown of the process into three main stages:

#### 1. Select Bait

This is the stage where an attacker selects the potential candidate or candidates for the attack and engineers an email or message to look like it comes from a trusted source, such as a friend, family member, coworker, or organization. These messages are designed to create a sense of urgency or make a request that encourages the user to perform an action that helps the attacker achieve their goal.

#### 2. Set Hook

In this message, the attacker provides a hook, usually in the form of a link to a website or a file to be downloaded. The message encourages the user to click the link or open or download the file, often by creating a sense of urgency and making the user feel that they need to act quickly before it is too late.

#### 3. Catch the Phish

The process is only successful if the user falls for the bait and performs the action requested by the attacker. Once the action is completed, the attacker may obtain sensitive information or get the victim to download and execute malware, which can then compromise the individual's system or potentially affect the wider organization.

### 1.2 Types of Phishing

There are several ways that a phishing attack can be executed.

1. **Spear Phishing**  
   This type of phishing is carried out when an attacker adds personalised information and details about the user in order to gain the user's trust. As the word *spear* suggests, this is a direct attack engineered for a particular person or organisation.

2. **Whaling**  
   This is a phishing attack directed towards a high-profile person, or a *whale* in a manner of speaking, with the aim of stealing sensitive and high-value information.

3. **Vishing**  
   This is a phishing technique that uses voice communication to interact with the user and attempt to gain their trust or convince them to provide sensitive information or perform an action.

4. **Smishing**  
   This is phishing carried out through text messaging to get the victim to click on a link, download files or applications, or begin a conversation with the attacker.

### 1.3 Real-World Example: 2011 RSA SecurID Attack

In 2011, RSA Security was targeted by a spear-phishing attack. Attackers sent employees a malicious Excel attachment disguised as a recruitment document. When an employee opened it, the attackers gained access to RSA's network and stole information related to its SecurID authentication products. The stolen information was later linked to attacks against organisations that used SecurID.

The incident shows how a simple phishing message can become the starting point for a much larger security breach.

### 1.4 Prevention Recommendations

1. **Use Multi-Factor Authentication (MFA)**  
   Organizations should enable MFA on accounts, especially those containing sensitive information. Where possible, phishing-resistant MFA should be used because it provides stronger protection against stolen credentials.

2. **Don't Click Links from Unexpected Messages**  
   Users should avoid accessing links from unexpected emails or messages. Instead, they should visit the organization’s official website directly to verify the request.

3. **Use Strong, Unique Passwords and a Password Manager**  
   Users should use different passwords for different accounts and consider using a password manager to generate and securely store them. This limits the damage if one password is compromised through phishing.

4. **Train Users to Recognize and Report Phishing**  
   Organizations should regularly train employees to recognize suspicious messages and understand how to report suspected phishing attempts.

---

## 2. Pretexting

This is a social engineering tactic that uses a fake scenario or false story to convince the target to provide information or perform a task.

### 2.1 How It Works

The fake story or scenario in question is what we call the **pretext**. A pretext consists of two main elements: **character** and **situation**.

The **character** is the role the attacker is portraying or playing in the story. This is done to build confidence with the victim and make the story believable. For this reason, the attacker may impersonate a person of authority, such as a boss, or someone the victim trusts, such as a close friend or family member.

The **situation** is the plot or story the attacker has created. It provides the reason for the action they are asking the victim to perform. The situation could be something generic, such as asking someone to update their account information, or it could be carefully created around a specific victim.

### 2.2 Real-World Example: 2024 Hong Kong Deepfake Scam

In 2024, an employee in Hong Kong was targeted by attackers who used AI-generated video and audio to impersonate senior company executives during a video conference. The attackers created a false situation that convinced the employee that the instructions were coming from company leadership. The employee eventually transferred approximately HKD 200 million to the attackers.

This case shows how pretexting can be effective even when the attacker does not directly exploit a technical vulnerability. By creating a believable scenario and impersonating trusted individuals, the attackers were able to convince the victim to take the desired action.

### 2.3 Prevention Recommendations

1. **Verify Unusual Requests Independently**  
   Employees should verify unexpected requests for sensitive information or financial transactions through a separate, trusted communication channel before taking action.

2. **Provide Regular Security Awareness Training**  
   Organisations should train employees to recognise impersonation, unusual requests, urgency, and other signs of pretexting. Training can also include examples of real-world attacks.

3. **Use Clear Authorisation Procedures**  
   Sensitive actions such as transferring money or sharing confidential information should require additional verification or approval rather than relying on a single person's request.

---

## 3. Baiting

This is a social engineering tactic that uses some form of bait to lure a victim into downloading malicious software or other compromising files. This bait can be in two forms: physical and digital.

With **physical baiting**, the bait is usually a physical object, such as a USB flash drive infected with malicious code. Once the USB is inserted into a system and the malicious file is opened or executed, it can allow the attacker to compromise the system or install malicious files.

**Digital baiting** can be as simple as an advertisement offering a free movie download. The moment you try to download the movie, you may end up downloading a malicious file instead.

### 3.1 Real-World Example: Raspberry Robin

In 2022, Microsoft documented a malware campaign known as Raspberry Robin that spread through infected USB drives. The drives contained files designed to appear harmless and encourage users to open them. Once the malicious file was executed, the malware could spread to other systems through additional USB devices. Microsoft observed the malware affecting hundreds of machines within one organisation.

This shows how baiting can take advantage of a user's curiosity or trust instead of relying only on a technical vulnerability. The USB drive acts as the bait, while the malicious file is what allows the attack to begin.

### 3.2 Prevention Measures

1. **Do Not Use Unknown USB Devices**  
   Employees should avoid connecting USB drives or other removable devices whose source is unknown or cannot be verified. CISA specifically recommends against connecting unknown USB devices to important systems.

2. **Use Security Controls for Removable Media**  
   Organisations should control the use of USB devices and use security software to detect malicious files before they can affect a system.

3. **Train Employees to Recognise Baiting Attempts**  
   Security awareness training should teach employees not to open unexpected files, use unknown USB drives, or download software from untrusted sources.

---

## 4. Quid Pro Quo

Quid pro quo is a social engineering tactic where an attacker offers a service, benefit, or reward in exchange for sensitive information or an action from the victim. For example, an attacker may pretend to provide technical support and ask the victim for information in return for their help. The tactic relies on the victim believing that they are receiving something valuable in exchange.

### 4.1 Prevention

1. **Verify Unexpected Offers or Requests**  
   Confirm that the person or service making the offer is legitimate before providing any sensitive information.

2. **Do Not Exchange Sensitive Information for Unsolicited Help or Rewards**  
   Users should be cautious when someone offers a service, prize, or benefit in exchange for passwords or other confidential information.

3. **Provide Security Awareness Training**  
   Employees should be trained to recognise social engineering tactics and understand when a request should be reported or verified.

---

## 5. Comparison Table

This table summarises the main social engineering attacks covered in this report.

| Attack Type | Primary Target | Psychological Lever Exploited | Best Countermeasure |
| --- | --- | --- | --- |
| **Phishing** | Email and messaging users | Urgency, fear, trust | MFA and phishing awareness training |
| **Pretexting** | Individuals with access to sensitive information | Trust, authority, familiarity | Independent verification of requests |
| **Baiting** | Curious or unsuspecting users | Curiosity, desire for free items or content | Avoid unknown devices and files |
| **Quid Pro Quo** | Users seeking help, services, or rewards | Reciprocity, trust | Verify the person and offer before sharing information |

---

## 6. Organisational Recommendations

### Employee Security Awareness Training Checklist

Organisations should provide regular security awareness training to help employees recognise and respond to social engineering attacks. A basic training checklist should include:

1. **Teach Employees to Recognise Common Social Engineering Attacks**  
   Training should cover phishing, pretexting, baiting, and other common tactics, including the warning signs associated with each attack.

2. **Teach Employees to Verify Unusual Requests**  
   Employees should know how to independently verify unexpected requests for sensitive information, payments, or access before taking action.

3. **Teach Employees How to Report Suspicious Activity**  
   Employees should know exactly who to contact and what process to follow when they encounter a suspicious message, request, file, or device.

4. **Conduct Regular Awareness Training and Simulations**  
   Training should not be a one-time activity. Organisations should regularly update employees and can use simulated phishing exercises to test and improve their awareness.

5. **Create a Culture Where Employees Can Report Mistakes Safely**  
   Employees should be encouraged to report suspicious activity, even when they have already interacted with it. A supportive reporting culture allows organisations to respond quickly and reduce potential damage.

---

## 7. References

1. Cybersecurity and Infrastructure Security Agency (CISA). (2025). *Four Cybersecurity Essentials for SLTTs*. [CISA: Four Cybersecurity Essentials](https://www.cisa.gov/resources-tools/resources/four-cybersecurity-essentials-sltts)

2. National Institute of Standards and Technology (NIST). (2025). *Phishing*. [NIST: Phishing Guidance](https://www.nist.gov/itl/smallbusinesscyber/guidance-topic/phishing)

3. National Institute of Standards and Technology (NIST). (2023). *NIST Phish Scale User Guide*. [NIST: Phish Scale User Guide](https://www.nist.gov/publications/nist-phish-scale-user-guide)

4. SANS Institute. (2025). *SANS 2025 Security Awareness Report: Embedding a Strong Security Culture*. [SANS: 2025 Security Awareness Report](https://www.sans.org/white-papers/sans-2025-security-awareness-report)

5. Microsoft. (2022). *Raspberry Robin: Worm part of larger ecosystem facilitating pre-ransomware activity*. [Microsoft Security: Raspberry Robin](https://www.microsoft.com/en-us/security/blog/2022/10/27/raspberry-robin-worm-part-of-larger-ecosystem-facilitating-pre-ransomware-activity/)
