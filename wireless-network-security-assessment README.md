# Wireless Network Security Assessment (Controlled Lab)

## Disclaimer
This assessment was conducted in a controlled lab environment using a wireless network and devices owned by me. The project was performed strictly for educational and defensive security purposes.

---

## Executive Summary

This project evaluates the security posture of a home wireless network in a controlled lab environment.  
The objective was to identify potential weaknesses in the wireless configuration, assess associated risks, and implement mitigation strategies to improve overall network security.

The assessment identified weak password practices and insecure configuration settings that could expose the network to unauthorized access. Remediation measures were applied to significantly strengthen the wireless security posture.

---

## Objective

- Assess wireless network security configuration  
- Identify potential vulnerabilities or weak settings  
- Evaluate associated risks  
- Implement mitigation controls  
- Document findings in a structured security report  

---

## Lab Environment

- Kali Linux (Security Testing Environment)  
- Personal Home Router (WPA2-PSK Configuration)
- Laptop Client Device  
- Private Controlled Network (bikinibottom)
 
---

## Wireless Reconnaissance

As part of the assessment, the wireless environment was passively analyzed in a controlled lab setting to identify encryption protocols and authentication mechanisms in use.

The objective of this phase was to determine:

- Encryption standard (WPA2 / WPA3)
- Authentication method (PSK)
- General network security posture

![WhatsApp Image 2026-03-01 at 11 07 15 AM](https://github.com/user-attachments/assets/aafb97e1-3d94-48ee-aed2-564576224535)

The reconnaissance confirmed that the lab network was configured using *WPA2-PSK*.

---

## Technical Insight: WPA2 4-Way Handshake

WPA2-PSK authentication relies on a 4-way handshake process that allows both the client device and the access point to verify possession of the pre-shared key without transmitting the password directly.

During this exchange:

- Cryptographic nonces are generated
- Session keys are derived
- Encrypted communication is established using AES

Although the password is never transmitted, the authentication exchange can be passively captured within wireless range.

The image below shows a successful capture of the WPA2 authentication exchange
![WhatsApp Image 2026-03-01 at 11 21 15 AM](https://github.com/user-attachments/assets/1b8e2e02-afa7-4f7e-b197-aab829a5352a)

This confirms that:

- The access point uses WPA2-PSK
- The 4-way handshake process was observed
  
---

## Controlled Password Strength Validation

In the controlled lab environment, the authentication exchange was used solely to evaluate password strength resilience.

This validation demonstrated that weak password structures significantly reduce resistance against offline dictionary-based attempts.
The image below shows the successful validation of the lab password, confirming insufficient entropy.
<img width="1570" height="736" alt="image" src="https://github.com/user-attachments/assets/ae6e84bf-201c-46eb-bc5a-a5a9d2f83b93" />

All testing was performed exclusively on personally owned infrastructure.
---

## Risk Analysis

WPA2-PSK security depends heavily on the entropy of the pre-shared key.

If a password lacks sufficient complexity:

- Captured authentication exchanges may enable offline password testing
- Attackers within wireless range could potentially recover weak credentials
- Unauthorized network access could occur

*Risk Type:* Weak Authentication  
*Severity:* Medium–High  

---

## Mitigation Implemented

To eliminate the identified risk, the following measures were applied:

- Replaced weak password with a 16+ character randomized key
- Upgraded to WPA3 where supported
- Disabled WPS
- Reviewed administrative security settings

---

## Post-Mitigation Outcome

After implementing security hardening controls:

- Strong encryption configuration confirmed
- High-entropy password enforced
- Reduced exposure to offline password recovery risk
- Overall wireless attack surface significantly minimized

---

## Professional Takeaway

This assessment reinforced a fundamental cybersecurity principle:

Even when cryptographic protocols are strong, weak password policies can undermine overall system security.

Proper configuration, strong entropy, and proactive hardening are essential to maintaining resilient wireless infrastructure.


## Skills Demonstrated

- Wireless Security Fundamentals  
- Risk Assessment  
- Security Hardening  
- Technical Documentation  
- Analytical Thinking  
- Defensive Security Mindset  

---

## Author

Efrén Navarro  
Aspiring Cybersecurity Analyst and Penetration Tester
