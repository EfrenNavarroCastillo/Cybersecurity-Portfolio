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

## Scope

The scope of this assessment was limited to:

- A personal wireless router  
- A controlled client device  
- Local wireless network configuration  

---

## Lab Environment

- Kali Linux (Security Testing Environment)  
- Personal Home Router (WPA2-PSK Configuration)  
- Laptop Client Device  
- Private Controlled Network  

---

## Methodology (High-Level)

The following methodology was applied:

1. Wireless network reconnaissance  
2. Encryption protocol identification  
3. Security configuration analysis  
4. Password strength evaluation  
5. Risk assessment  
6. Implementation of security hardening measures  

This methodology follows a simplified penetration testing lifecycle adapted for a controlled lab environment.

---

## Findings

### 1. Weak Password Configuration

![WhatsApp Image 2026-03-01 at 10 37 16 AM](https://github.com/user-attachments/assets/6b1fe239-f00a-4a3b-a174-af7dc2d47362)

*Observation:*  
The wireless network was configured using WPA2-PSK with a weak password structure.

*Risk:*  
Weak passwords increase exposure to dictionary-based attacks or brute-force attempts by attackers within wireless range.

*Severity:* Medium  

---

### 2. WPS Enabled

![WPS Screenshot](images/wps-enabled.png)

*Observation:*  
Wi-Fi Protected Setup (WPS) was enabled on the router.

*Risk:*  
WPS can introduce additional attack surface and may allow unauthorized access under certain conditions.

*Severity:* Medium  

---

## Risk Impact

If exploited, the identified weaknesses could potentially allow:

- Unauthorized network access  
- Traffic interception  
- Lateral movement within the local network  
- Access to connected devices  

While no exploitation was performed beyond validation in the controlled lab, the configuration presented unnecessary risk exposure.

---

## Mitigation Implemented

The following security improvements were applied:

- Upgraded encryption configuration (WPA3 where supported)  
- Implemented a 16+ character randomly generated password  
- Disabled WPS  
- Updated router firmware to latest version  
- Created a segmented guest network  
- Reviewed and hardened router administrative settings  

---

## Post-Mitigation Validation

![Config After](images/config-after.png)

After implementing security controls:

- Strong encryption confirmed  
- Secure password policy enforced  
- WPS disabled  
- Firmware updated  

The overall attack surface was significantly reduced.

---

## Lessons Learned

This project reinforced the importance of:

- Strong password policies  
- Proper wireless encryption standards  
- Regular firmware updates  
- Disabling unnecessary services  
- Conducting periodic security assessments  

Wireless networks remain a common entry point for attackers, and proactive security configuration is essential in reducing risk exposure.

---

## Skills Demonstrated

- Wireless Security Fundamentals  
- Risk Assessment  
- Security Hardening  
- Technical Documentation  
- Analytical Thinking  
- Defensive Security Mindset  

---

## Future Improvements

- Implement centralized logging for wireless events  
- Deploy network monitoring tools  
- Simulate detection scenarios in a SOC lab environment  
- Expand assessment to include internal network segmentation testing  

---

## Author

Efrén Navarro  
Aspiring Cybersecurity Analyst and Penetration Tester
