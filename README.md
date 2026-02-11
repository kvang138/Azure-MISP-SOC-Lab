# Sharpening Modern Threat Detection and Response with Microsoft Sentinel Powered by MISP Threat Intelligence

## 📖Introduction
Ever wondered, while reviewing Microsoft Sentinel logs, whether a suspicious IP address is truly malicious? This hands-on, cloud-native Security Operations Center (SOC) lab demonstrates how to build an advanced, cutting-edge threat detection and response (TDR) capabilities using Microsoft Sentinel enhanced with MISP (Malware Information Sharing Platform) threat intelligence. By integrating Microsoft Sentinel with rich, community-driven indicators of compromise (IoCs)—such as malicious IPs, command-and-control (C2) server locations, domains, URLs, file hashes, and registry keys, etc. — you gain the ability to:

 - Quickly determine if an observed IP belongs to known adversary infrastructure.
 - Identify whether users have accessed malicious sites or resources.
 - Enrich alerts with contextual threat intelligence.
 - Shift from reactive incident response to proactive threat hunting and prevention.

The result: stop attacks and threats dead in their tracks before they can cause damage.

## 🔑🔤🛠️Key Components and Technologies
- MISP instance running as a Docker container on a Linux VM (the open-source threat intelligence platform.)
- Docker
- Azure Functions (for automated indicator ingestion and processing)
- Python (core scripting language for integration logic, utilizing PyMISP)
- MISP2Sentinel data connector
- KuduLite (for troubleshooting Azure Functions and deployment)
- App Registration
- Azure Key Vault (secure storage of API keys, credentials, and secrets)
- Log Analytics workspace
- Microsoft Sentinel

## 📸Screenshots
Azure Function App for the MISP to Sentinel Integration.
![Azure Function App for the MISP to Sentinel Integration.](https://github.com/kvang138/Azure-MISP-SOC-Lab/blob/main/Screenshots/Azure-MISP-SOC-Lab%201.png)

KuduLite for troubleshooting Azure Function App deployment.
![KuduLite for troubleshooting Azure Function App deployment.](https://github.com/kvang138/Azure-MISP-SOC-Lab/blob/main/Screenshots/Azure-MISP-SOC-Lab%202.png)

Azure Function App processing and uploading IoCs (Indicator of Compromise) to Microsoft Sentinel.
![Azure Function App processing and uploading IoCs (Indicator of Compromise) to Microsoft Sentinel.](https://github.com/kvang138/Azure-MISP-SOC-Lab/blob/main/Screenshots/Azure-MISP-SOC-Lab%203.png)

Searching for IPv4 and IPv6 malicious IPs with a confidence score of a least 50%.
![Searching for IPv4 and IPv6 malicious IPs with a confidence score of a least 50%.](https://github.com/kvang138/Azure-MISP-SOC-Lab/blob/main/Screenshots/Azure-MISP-SOC-Lab%204.png)

One of the malicious IPv4 addresses identified in the MISP threat feed.
![One of the malicious IPv4 addresses identified in the MISP threat feed.](https://github.com/kvang138/Azure-MISP-SOC-Lab/blob/main/Screenshots/Azure-MISP-SOC-Lab%205.png)

Examining the Security Event log for evidence of malicious IP addresses communicating with the honeypot.
![Examining the Security Event log for evidence of malicious IP addresses communicating with the honeypot.](https://github.com/kvang138/Azure-MISP-SOC-Lab/blob/main/Screenshots/Azure-MISP-SOC-Lab%206.png)

Examining the Application Gateway WAF firewall log for evidence of malicious IP addresses interacting with the WAF or targeting the vulnerable web application.
![Examining the Application Gateway WAF firewall log for evidence of malicious IP addresses interacting with the WAF or targeting the vulnerable web application.](https://github.com/kvang138/Azure-MISP-SOC-Lab/blob/main/Screenshots/Azure-MISP-SOC-Lab%207.png)

Examining the Application Gateway WAF firewall log for evidence of malicious IP addresses communicating with the cloud environment.
![Examining the Application Gateway WAF firewall log for evidence of malicious IP addresses communicating with the cloud environment.](https://github.com/kvang138/Azure-MISP-SOC-Lab/blob/main/Screenshots/Azure-MISP-SOC-Lab%208.png)

## 💡Conclusion
Microsoft Sentinel, when augmented with MISP threat intelligence, it transcends traditional SIEM functionality. It becomes a powerful proactive defense tool by enriching logs, generating high-fidelity alerts on genuine threats, and empowering cybersecurity analysts to detect adversaries lurking in the environment before they escalate. This integration transforms threat hunting from reactive to proactive. By automating the flow of fresh and actionable IoCs into Sentinel, security teams can identify compromised assets faster, reduce dwell time, and respond more effectively all within a scalable cloud-native architecture. This lab showcases a practical, real-world use case used by many SOCs to close intelligence gaps and improve organization's resilience and security posture.
