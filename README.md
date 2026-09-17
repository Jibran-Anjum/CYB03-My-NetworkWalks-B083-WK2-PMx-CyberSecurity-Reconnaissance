<div align="center">

# Network Footprinting & Passive OSINT Collection Labs

</div>

<p align="center">
    <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
    <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
    <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
    <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
    <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
    <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
    <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
    <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
    <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
    <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
    <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
    <img src="https://img.shields.io/badge/Waqas%20Karim%20CCIE-C00000?style=flat-square" />
</p>

---


Welcome to the **Network Footprinting & Passive OSINT Collection** repository. This repository serves as a centralized documentation hub for hands-on cybersecurity labs focused on the reconnaissance phase of security testing. 

The primary objective of these reports is to demonstrate how publicly accessible information can be systematically gathered, analyzed, and structured using industry-standard CLI tools and specialized search engine operators—all without directly engaging in intrusive exploitation.

---

## 🛠️ Overview of Included Reports

This repository is organized into distinct project modules focusing on two primary reconnaissance methodology branches: **Active Infrastructure Enumeration** and **Passive Search Engine Intelligence (OSINT)**.

### 📌 Project Module 1: Active Infrastructure Reconnaissance
* **Core Objective:** Conduct non-intrusive domain and infrastructure analysis on target domains to build a complete target profile.
* **Key Methodology & Tools:**
  * **Domain Ownership:** `whois` queries to evaluate domain registration, registrar data, and administrative contacts.
  * **Technology Fingerprinting:** `whatweb` for detecting CMS frameworks (WordPress), JavaScript libraries, and client-side plugins.
  * **DNS Resolution & Record Enumeration:** `nslookup` and `dnsrecon` for mapping IP addresses, SOA, NS, MX, TXT (SPF), and SRV autodiscover records.
  * **HTTP Header Security Analysis:** `curl -I` for inspecting cookie flags (`HttpOnly`, `Secure`), cache configurations, and server software signatures.
  * **WAF Detection:** `wafw00f` to identify active Web Application Firewalls (e.g., ModSecurity).

### 📌 Project Modules 2 & 5: Open-Source Intelligence (OSINT) & Google Dorking
* **Core Objective:** Leverage Google Hacking Database (GHDB) techniques to perform zero-contact intelligence gathering.
* **Key Methodology & Tools:**
  * Application of advanced search operators (`intitle:`, `inurl:`, `site:`, `intext:`, `filetype:`) to identify exposed web interfaces and public endpoints.
  * Direct indexing techniques (`intitle:"Index of"`) for discovering open directory trees and downloadable public documentation (e.g., academic resources, research papers, and technical PDFs).
  * Evaluation of unintended public exposure patterns across live web applications and public hardware interfaces.

---

## 🚀 Key Takeaways & Defense Considerations

Each report concludes with practical defensive remediations designed to minimize an organization's attack surface:
* **WHOIS Privacy:** Masking administrative and technical contact data via registrar privacy services.
* **Server Header Sanitization:** Obscuring sensitive software versions (`Server`, `X-Powered-By`) to mitigate automated fingerprinting.
* **Directory Browsing Controls:** Explicitly disabling `Indexes` in web server configs (`Apache`, `Nginx`) to prevent path traversal and file enumeration.
* **Proper WAF Deployment:** Implementing web application firewall policies to filter probes and suspicious request signatures.
