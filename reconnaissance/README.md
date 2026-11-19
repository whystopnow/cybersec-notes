# Reconnaissance[^1]

### Reconnaissance is divided into two main types:

- **Passive** reconnaissance: Collecting publicly available data (like social media posts, DNS records, or company websites) without directly interacting with the target. 

- **Active** reconnaissance: Directly probing the target’s systems to discover open ports, running services, and software versions. 
While attackers use this phase to build a blueprint for exploitation, security professionals use the same techniques to proactively identify and fix weaknesses in their own defenses.

---

[Initial Enumeration](https://github.com/whystopnow/cybersec-notes/blob/main/reconnaissance/initial-enumeration.md)

[Credential Enumeration](https://github.com/whystopnow/cybersec-notes/blob/main/reconnaissance/credential-enumeration.md)

---

### The most widely used reconnaissance tools

| Tool | Best For |	Type |
|------|----------|------|
| Nmap	| Port scanning, service & OS detection	| Active
| Shodan	| Internet-wide exposed device/service discovery	| Passive
| Censys	| Certificate & host intelligence at scale	| Passive
| Amass	Deep | subdomain & attack-surface mapping	| Passive/Active
| theHarvester	| Email, subdomain & host harvesting from public sources	| Passive
| Recon-ng	| Modular, scriptable recon framework	| Passive/Active
| Maltego	| Visual link analysis & relationship mapping	| Passive
| SpiderFoot	| Automated multi-source OSINT footprinting	| Passive
| Subfinder	| Fast passive subdomain discovery	| Passive
| Masscan	| Internet-scale port scanning (very fast, very noisy)	| Active

[^1]: Cybersecurity reconnaissance is the process of gathering information about a target system, network, or organization to identify vulnerabilities and plan a cyberattack.  It is typically the first phase of an attack, allowing threat actors to understand the target’s infrastructure and security posture before attempting to breach it. 
