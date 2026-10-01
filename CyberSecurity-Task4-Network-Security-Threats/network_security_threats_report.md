# Common Network Security Threats

## Introduction

The world has grown into an interconnected community with an almost total dependence on technology and the internet. Most people conduct their daily activities using one or more digital devices. For speed and accessibility, we rely on the internet, a network connecting devices and people across the world.

Since the emergence of the internet and its associated technologies, security has been a vital concern. Unlike the paper era, where physical location was one of the biggest barriers to accessing information, the technological era has given individuals with the technical knowledge the ability to attempt to access systems from almost anywhere in the world through the internet. These individuals are commonly referred to as hackers.

However, the era of Artificial Intelligence (AI) has introduced additional concerns. Today's security threats do not only come from knowledgeable hackers with years of experience, tools, and technical skills. They can also involve individuals with internet access, a capable AI system, and a sufficiently descriptive prompt. For this reason, network security matters now more than ever.

Network threats come in many ways and through many different creative channels; some, I am sure, have not even been recorded. Among the many threats that can compromise network security, some of the most common include Denial-of-Service (DoS/DDoS), Man-in-the-Middle (MITM) attacks, IP spoofing, and DNS poisoning/spoofing. These are the threats I will be shining a little light on in this research report.

---

## 1. DoS / DDoS

### 1.1 How It Works

A Denial-of-Service (DoS) attack is one of the oldest and most effective network threats known to man. It is usually carried out by overwhelming a target device or service with a high volume of requests in a short period of time, making the device or service unavailable to legitimate users. Some of these requests may be ones the device cannot efficiently handle, which can cause its resources to become exhausted and the system to become slow or unresponsive.

If I were to explain this with an analogy, a DoS attack is like giving a notebook full of assignments to a toddler in preschool, where all the assignments are mathematics questions meant for high school students, and then telling the toddler to finish them before eating. This is similar to what happens to a computer under a resource-exhaustion attack: it is presented with more work than it can effectively handle, leaving fewer resources available for legitimate tasks. In severe cases, the device or service may become incapable of sending or receiving requests or performing expected functions in response to other events, such as a legitimate user trying to access an application.

A Distributed Denial-of-Service (DDoS) attack does practically the same thing, but in this case, the traffic being generated toward the target comes from **multiple systems**, often distributed across different networks and locations. This makes the attack more difficult to stop because the malicious traffic is not coming from a single source.

### 1.2 Real-World Example

#### October 2023: Google Mitigates 398 Million RPS Attack

In October 2023, Google reported that it had mitigated what was, at the time, the largest recorded Distributed Denial-of-Service (DDoS) attack, which peaked at **398 million requests per second (RPS)**. The attack used a technique known as **HTTP/2 Rapid Reset**, which exploited a weakness in the HTTP/2 protocol.

HTTP/2 is important to how modern browsers communicate with websites because it allows them to request resources such as text, images, and other content. In an HTTP/2 Rapid Reset attack, attackers send a large number of requests to a website and then immediately cancel those requests. This request-and-cancel process can be repeated at a very high rate, placing significant pressure on the target's resources and potentially making the service unavailable.

### 1.3 Impact

The impact of a DoS/DDoS attack on the target is numerous and extremely harmful. When the target is a website or an internet-facing service like Google, that service can become unreachable. The target’s ability to process incoming requests can become exhausted, along with its available resources. Businesses hosted on these devices can suffer losses. Critical applications in places like hospitals and military organizations can become unavailable. Organizations can lose time and money. Attacks on large companies can also affect others at the same time, either directly or indirectly. Sometimes, recovery can take longer than the attack itself.

### 1.4 Mitigation

There are several mitigation strategies that can be used, but these are the top few I chose to outline.

1. **Filter Network Traffic**

   In any case, if the network flood exceeds the network's capability or capacity, it is vital for the incoming traffic upstream to be intercepted so that the attack traffic can be filtered from legitimate traffic before all users are restricted from the network resources. When the various sources of the attack are found, the next logical step is to block them, block the ports being exploited, or simply block the protocols being used for the transportation of the traffic itself.

2. **Response Rate Limiting**

   Response Rate Limiting simply reduces the rate at which a system responds to unusually high volumes of requests at a time. This would restrict the potency of the attack to an extent until the attack is stopped.

3. **Load Balancing**

   Like the name suggests, load balancing is the process of spreading incoming traffic across multiple systems so no one system becomes overwhelmed. This is what helped keep Google services running during its 398 million RPS DDoS attack.

---

## 2. Man-in-the-Middle (MITM)

### 2.1 How It Works

A Man-In-The-Middle attack is said to have happened when an attacker positions or plants themselves between two or more networked devices to do anything from data manipulation and stealing to other attacks, all while exploiting the common features of network protocols. One common way this can be done is by using Address Resolution Protocol (ARP) poisoning to position the attacker between two devices on a network.

The Address Resolution Protocol, as its name suggests, resolves IPv4 addresses into link-layer addresses. If there is a point where a device cannot identify an IP address in its cache and its related MAC address, it sends out a broadcast ARP request. When the device with the requested IP address receives this request, it replies with its MAC address so communication can take place. It is at this point that an attacker can interfere by sending a forged ARP response containing their own MAC address. This can cause the victim device to associate the legitimate IP address with the attacker's MAC address, causing traffic intended for the legitimate device to pass through the attacker's system.

In a nutshell, **this is one technique attackers can use to position themselves in the middle of network communication and perform a MITM attack.**

### 2.2 Real-World Example

#### 2012: Flame Malware Hijacks Microsoft Update

In 2012, security researchers discovered that the **Flame** cyberespionage malware was using a Man-in-the-Middle attack to spread itself across machines on a local network. The attack intercepted requests from infected machines attempting to connect to Microsoft's Windows Update service and redirected those requests to a malicious server instead.

The malicious server then delivered a fake Windows Update containing Flame malware. Because the malicious file was signed with a fraudulent Microsoft certificate, it could appear to the victim's computer as legitimate Microsoft software. The attackers achieved this by exploiting a vulnerability in Microsoft's certificate infrastructure.

### 2.3 Impact

When a MITM attack is successfully launched and executed, it can have dire effects on a system. Some attackers use this connection to deliver malware to a device, while others use it as a platform for data manipulation, network sniffing, and network traffic redirection or modification. Some attacks also allow attackers to gain access to network credentials such as passwords, logins, access credentials and tokens. Others can be used to perform relay attacks, while some can serve as a platform for launching major attacks such as Denial-of-Service (DoS) attacks.

### 2.4 Mitigation

There are several mitigation strategies that can be used, but these are the top few I chose to outline.

1. **Filter Network Traffic**

   To stop some of the attacks being launched by an attacker on a network, you can use network appliances and host-based security software to block unnecessary network traffic within the network environment.

2. **Encrypt Sensitive Information**

   There could always be the possibility that a device is compromised and there is an attacker somewhere in the network at all times. So, to prevent them from gaining access to vital and sensitive information, you should encrypt it with a good encryption algorithm. This ensures that even if an attacker gets hold of it, it cannot be used.

3. **Network Segmentation**

   When a network is divided into multiple parts or segments instead of everything being together on one network, it limits the scope of a potential MITM attack on the network and the individual devices on that network.

---

## 3. IP Spoofing

### 3.1 How It Works

IP spoofing is a technique used in network attacks where an attacker forges the source IP address of packets to make them appear as though they came from another trusted system. This is generally done by first identifying the IP address of a trusted system and then modifying the packets sent by the attacker so that their source IP address is replaced with the address of the trusted system. At this point, the destination computer may be fooled into believing that the packets came from a legitimate and trusted source.

The end goal of IP spoofing can vary depending on the attack. It can be used to bypass certain forms of network filtering, hide the actual source of traffic, or enable other attacks such as reflection and amplification attacks.

### 3.2 Real-World Example

#### 2019: WS-Discovery Reflection DDoS Attacks

In 2019, researchers reported a new type of DDoS attack that abused vulnerabilities in the **Web Services Dynamic Discovery (WS-Discovery)** protocol. WS-Discovery is designed to allow devices on the same network to discover and communicate with each other, but thousands of internet-exposed devices could also respond to specially crafted requests. Attackers could send WS-Discovery requests to these vulnerable devices while **spoofing the source IP address of the intended victim**. The devices would then send their responses toward the victim instead of the actual attacker. Because the responses could be much larger than the original requests, the technique could amplify the amount of traffic directed at the target. This is an example of the **reflection amplification** technique described by MITRE.

### 3.3 Impact

IP spoofing as an attack makes it harder to trace an attacker since all traffic is made to look like it comes from a legitimate source. It can greatly support Distributed Denial-of-Service attacks, which could potentially exhaust network bandwidth. It can also be used to redirect large amounts of traffic toward a victim through reflection attacks. This can cause network services to become slow or completely unavailable to legitimate users. Another impact is that it can make source-based security controls less effective, since the source address in the packet cannot always be trusted. It can also cause third-party systems to become unintentionally involved in an attack when their responses are redirected toward the spoofed victim.

### 3.4 Mitigation

1. **Source Address Validation**

   Instead of networks blindly trusting and accepting the IP address on a packet, they can validate it to make sure the traffic is coming from a legitimate source.

2. **Access Control Lists (ACLs)**

   Access Control Lists should be configured on network devices to control which source addresses are permitted on a particular interface or within a network.

3. **Unicast Reverse Path Forwarding (uRPF)**

   uRPF checks whether traffic arriving from a source address is consistent with the routing information available to the network device.

---

## 4. DNS Spoofing / Poisoning

### 4.1 How It Works

DNS spoofing is a tactic an attacker uses to redirect a user to malicious sites using the Domain Name System. It is the job of DNS to take the human-readable website names we use to reach any site of our choice and translate them into machine-readable IP addresses that computers can use to navigate to their destination. However, attackers can find ways to exploit security gaps in the system and provide or insert false DNS information, causing a domain name to resolve to a malicious IP address instead of the legitimate one. This can redirect users to malicious sites without them realizing it. This is how DNS spoofing or poisoning can be carried out.

### 4.2 Real-World Example

#### 2019: Sea Turtle DNS Hijacking Campaign

In 2019, security researchers found a DNS hijacking campaign known as **Sea Turtle**, which targeted about 40 organizations across more than 10 countries. The attackers compromised DNS infrastructure and modified DNS records, causing users trying to access legitimate websites to be redirected to attacker-controlled servers. These servers could then be used to collect sensitive information such as usernames and passwords.

### 4.3 Impact

DNS spoofing has been used by many attackers to redirect legitimate users to illegitimate sites. It can also cause a loss of access or denial of service in cases where DNS spoofing is directly or indirectly related to a Denial-of-Service attack. Some users may also have their credentials for legitimate services, such as usernames and passwords, stolen. Other impacts include malware delivery, traffic interception, and many others.

### 4.4 Mitigation

1. **DNS Security Extensions**

   By using DNS Security Extensions (DNSSEC), we help protect two parts of the CIA triad: **integrity and authenticity**. It also helps prevent attackers from replacing legitimate IP addresses with forged information.

2. **Disable Targeted or Unnecessary Name-Resolution Protocols**

   Disable name-resolution protocols like **LLMNR, mDNS, and NetBIOS** when they are not needed.

3. **Protect DNS Infrastructure and DNS Records**

   Secure authoritative DNS servers and protect the integrity of the DNS information they provide. NIST's DNS deployment guidance specifically addresses protecting DNS infrastructure and DNS information.

---

## 5. Comparison Table

| Threat | Attack Vector | Who Is at Risk | Difficulty to Execute | Ease of Mitigation |
|---|---|---|---|---|
| DoS / DDoS | Overwhelming a device or service with a high volume of requests or traffic | Websites, online services, businesses, critical applications | Medium | Medium |
| MITM | Positioning between networked devices to intercept, manipulate, or redirect communication | Devices and users on vulnerable networks | High | Medium |
| IP Spoofing | Forging the source IP address of network packets | Networks, servers, online services, and third-party systems | Medium | High |
| DNS Spoofing / Poisoning | Manipulating DNS information to redirect users to malicious destinations | Website users, organizations, and DNS infrastructure | High | Medium |

---

## 6. Conclusion

In conclusion, these are some of the most well used and also well researched network threat. My report is only a summary, there are deeper explanations and different real life examples about the threats above. But there are some three take aways that I will leave for any network administrators reading this.

1. **Network attacks can feed into each other.**

   A single vulnerability or successful attack can create an opportunity for another attack. For example, IP spoofing can support DDoS through reflection and amplification, while MITM or DNS spoofing can be used to redirect traffic or steal credentials.

2. **Protect the network at multiple points.**

   No single mitigation is enough for every threat. Network administrators should combine measures such as traffic filtering, encryption, network segmentation, source-address validation, DNSSEC, and protecting DNS infrastructure.

3. **Early detection and prevention matter.**

   The longer an attacker can remain unnoticed or manipulate network traffic, the greater the potential impact. Network administrators should continuously monitor network activity and secure critical systems before they become entry points for further attacks.

---

## 7. References

1. Google Cloud. (2023, October 10). *Google mitigated the largest DDoS attack to date, peaking above 398 million rps.* Google Cloud Blog. https://cloud.google.com/blog/products/identity-security/google-cloud-mitigated-largest-ddos-attack-peaking-above-398-million-rps
2. Greenberg, A. (2019, April 17). *Cyberspies hijacked the internet domains of entire countries.* WIRED. https://www.wired.com/story/sea-turtle-dns-hijacking/
3. MITRE ATT&CK. (2026). *Adversary-in-the-Middle: Name Resolution Poisoning and SMB Relay (T1557.001).* https://attack.mitre.org/techniques/T1557/001/
4. National Institute of Standards and Technology. (2019). *Resilient Interdomain Traffic Exchange: BGP Security and DDoS Mitigation (NIST SP 800-189).* https://csrc.nist.gov/pubs/sp/800/189/final
5. National Institute of Standards and Technology. (2026). *Secure Domain Name System (DNS) Deployment Guide (NIST SP 800-81 Rev. 3).* https://csrc.nist.gov/pubs/sp/800/81/r3/final
6. Zetter, K. (2012, June 4). *Flame hijacks Microsoft Update to spread malware disguised as legit code.* WIRED. https://www.wired.com/2012/06/flame-microsoft-certificate/
