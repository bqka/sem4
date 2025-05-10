![[Pasted image 20250421020110.png]]

![[Pasted image 20250421020439.png]]

## ****Functions of Session Layer****

The session layer performs several different as well as important functions that are needed for establishing as well as maintaining a safe and secure connection:

1. ****Session Establishment**** : It establishes and manages sessions between communicating parties that cab be connection-oriented or connectionless. It also maps sessions to transport connections.
2. ****Communication Synchronization**** : It ensures reliable connectivity and recovery by using ****synchronization bits**** and ****checkpoints**** in data stream.
3. ****Activity Management**** : It allow the user to divide data into logical units called activities. An activity can be processed on its own and each activity is independent of activities that come before and after it.
4. ****Dialog Management**** : It refers to deciding whose turn it is to talk. Some applications uses a ****token mechanism**** for half-duplex mode, where only one party holds the token to transmit data while other supports full-duplex mode for simultaneous data transmission.
5. ****Data Transfer :**** It manages data exchange between systems.
6. ****Resynchronization :**** In this,  all the tokens are restored to the positions that were set during synchronization. The various options for resynchronization includes set, abandon and restart.

## ****Working of Session Layer****

- The Session Layer manages communication sessions between applications over a network.
- It establishes connections, negotiating session parameters like authentication and communication direction (full-duplex or half-duplex).
- It oversees data exchange by using tokens to manage transmission rights and prevent collisions.
- Synchronization techniques are implemented, inserting checkpoints for recovery in case of disruptions.
- It ensures orderly communication, reducing message loss, duplication, or errors caused by overlapping communication.
- The Session Layer gracefully terminates the session, ensuring all data is exchanged and both sides agree to close

# RPC


![[Pasted image 20250510055447.png]]
![[Pasted image 20250510055639.png]]
![[Pasted image 20250510055719.png]]

## Significance of Firewalls in Network Security

Firewalls are a fundamental component of network security, serving as the first line of defense between trusted internal networks and untrusted external sources such as the internet. Their primary purpose is to prevent unauthorized access, block malicious activities, and protect sensitive data from cyber threats like malware, ransomware, and hacking attempts[2](https://www.fortinet.com/resources/cyberglossary/benefits-of-firewall)[6](https://www.exabeam.com/explainers/network-security/firewalls-for-network-security-importance-types-and-best-practices/)[11](https://nordlayer.com/learn/firewall/what-is-firewall/). By monitoring and controlling incoming and outgoing network traffic based on predefined security rules, firewalls help organizations mitigate risks, maintain data confidentiality and integrity, and ensure compliance with industry regulations[2](https://www.fortinet.com/resources/cyberglossary/benefits-of-firewall)[6](https://www.exabeam.com/explainers/network-security/firewalls-for-network-security-importance-types-and-best-practices/).

Key functions of firewalls include:

- Filtering network traffic to block unauthorized access and malicious content.
    
- Enforcing security policies to restrict access to sensitive resources.
    
- Segmenting networks to limit the spread of threats and reduce attack surfaces.
    
- Generating logs and audit trails for compliance and forensic analysis[6](https://www.exabeam.com/explainers/network-security/firewalls-for-network-security-importance-types-and-best-practices/)[2](https://www.fortinet.com/resources/cyberglossary/benefits-of-firewall).
    

## Types of Firewalls

There are several types of firewalls, each with distinct methods for filtering and controlling network traffic[3](https://www.compuquip.com/blog/types-firewall-architectures)[6](https://www.exabeam.com/explainers/network-security/firewalls-for-network-security-importance-types-and-best-practices/)[12](https://www.paloaltonetworks.com/cyberpedia/what-does-a-firewall-do):

|Firewall Type|Description|
|---|---|
|Packet-Filtering Firewall|Examines packet headers (source/destination IP, port, protocol) and allows or blocks traffic based on rules. Simple and fast, but limited in depth of inspection[3](https://www.compuquip.com/blog/types-firewall-architectures)[10](https://opinnate.com/types-of-filtering-concepts-in-firewall-security/)[12](https://www.paloaltonetworks.com/cyberpedia/what-does-a-firewall-do).|
|Circuit-Level Gateway|Verifies TCP handshakes to ensure session legitimacy but does not inspect packet content. Efficient but less secure against malware[3](https://www.compuquip.com/blog/types-firewall-architectures).|
|Stateful Inspection Firewall|Tracks the state of active connections and makes decisions based on the context of traffic. Provides stronger security than basic packet filtering[3](https://www.compuquip.com/blog/types-firewall-architectures)[4](https://www.tutorchase.com/answers/a-level/computer-science/how-do-firewalls-filter-incoming-and-outgoing-traffic).|
|Proxy Firewall (Application-Level Gateway)|Acts as an intermediary at the application layer, inspecting the full content of traffic and providing deep security checks. Can introduce latency due to thorough inspections[3](https://www.compuquip.com/blog/types-firewall-architectures)[10](https://opinnate.com/types-of-filtering-concepts-in-firewall-security/)[12](https://www.paloaltonetworks.com/cyberpedia/what-does-a-firewall-do).|
|Next-Generation Firewall (NGFW)|Combines traditional firewall functions with advanced features like deep packet inspection, intrusion prevention, application awareness, and real-time threat intelligence[6](https://www.exabeam.com/explainers/network-security/firewalls-for-network-security-importance-types-and-best-practices/).|
|Hardware, Software, and Cloud Firewalls|Firewalls can be delivered as dedicated hardware appliances, software solutions, or cloud-based services, depending on deployment needs and scalability[3](https://www.compuquip.com/blog/types-firewall-architectures)[6](https://www.exabeam.com/explainers/network-security/firewalls-for-network-security-importance-types-and-best-practices/).|

## Role of Firewalls in Filtering Email Traffic

Firewalls play a crucial role in filtering both incoming and outgoing email traffic to protect against spam, malware, phishing, and other email-borne threats[5](https://www.barracuda.com/products/email-protection/spam-malware)[7](https://www.spikenow.com/glossary/email/firewall/)[8](https://www.sophos.com/en-us/products/sophos-email). Specialized email firewalls or secure email gateways use multiple techniques to safeguard email communications:

- **Spam Filtering**: Analyzes email content, sender reputation, and patterns to block unsolicited and potentially harmful emails[7](https://www.spikenow.com/glossary/email/firewall/)[5](https://www.barracuda.com/products/email-protection/spam-malware).
    
- **Malware and Virus Detection**: Scans attachments, links, and embedded content for malicious software, quarantining or blocking suspicious emails before they reach users[5](https://www.barracuda.com/products/email-protection/spam-malware)[7](https://www.spikenow.com/glossary/email/firewall/)[8](https://www.sophos.com/en-us/products/sophos-email).
    
- **Phishing Prevention**: Identifies and blocks phishing attempts by examining sender authenticity, email headers, and content for signs of impersonation or malicious intent[7](https://www.spikenow.com/glossary/email/firewall/)[8](https://www.sophos.com/en-us/products/sophos-email).
    
- **Content and Policy Filtering**: Enforces organizational policies by blocking or encrypting emails containing sensitive data, preventing data leaks and regulatory violations[5](https://www.barracuda.com/products/email-protection/spam-malware)[7](https://www.spikenow.com/glossary/email/firewall/).
    
- **Outbound Filtering**: Prevents compromised internal systems from sending spam or malicious emails, protecting the organization’s reputation and partners[5](https://www.barracuda.com/products/email-protection/spam-malware).
    

Modern email firewalls leverage advanced threat intelligence, machine learning, and behavioral analytics to detect zero-day threats, ransomware, and sophisticated phishing campaigns in real time[8](https://www.sophos.com/en-us/products/sophos-email)[5](https://www.barracuda.com/products/email-protection/spam-malware).

## Conclusion

Firewalls are indispensable for network security, providing robust protection against unauthorized access, malware, and a wide range of cyber threats. By employing various types of firewalls-each with unique strengths-organizations can tailor their defenses to specific risks and operational needs. In the context of email security, firewalls and secure email gateways are vital for filtering harmful traffic, preventing spam, blocking malware, and safeguarding sensitive information from both inbound and outbound threats[5](https://www.barracuda.com/products/email-protection/spam-malware)[7](https://www.spikenow.com/glossary/email/firewall/)[8](https://www.sophos.com/en-us/products/sophos-email).