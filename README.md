# Cybersecurity & Networking Labs

**Linux · Network security · Threat detection · VPN / firewalls · Traffic analysis · GNS3**

This repository is my **public, independently written portfolio overview** of practical networking and cybersecurity exercises. It goes well beyond GNS3: I have worked with Linux services, protected communications, attack investigation, IDS signatures, behavioral analysis, pfSense and IPsec.

## School 21 cybersecurity projects

**The original School 21 projects and submissions are stored in private GitLab repositories.** I do **not** publish the original assignments or solutions here. Several completed projects — covering infrastructure design, investigation of network attacks, threat detection and protected network design — have been **accepted by School 21** (status confirmed by me).

[**Read the complete public overview of what I worked on →**](SCHOOL21_CYBERSECURITY_LABS.md)

| Area | Practical work and tools |
| --- | --- |
| **Secure network design** | Small-enterprise LAN architecture, security zones and DMZ, asset inventory, access restrictions, defense in depth |
| **Network attack analysis** | MITRE ATT&CK mapping, Python/PyMongo checks, mitmproxy HTTP-form metadata, DNS-tunneling PCAP investigation, FOFA/CVE research |
| **Threat detection** | YARA binary signatures, Suricata rules and offline PCAP alerts, Python keyboard-timing comparison with pynput/statistics |
| **VPN and firewall administration** | Two pfSense virtual machines, site-to-site IPsec/IKEv2 tunnel, Phase 1/Phase 2 checks, LAN/IPsec rules, RDP/SSH restrictions, scheduled SMTP, iptables rules |
| **Protected communication channels** | nginx HTTPS/TLS, certificate infrastructure, OpenVPN/Easy-RSA, TUN interfaces, CryptoPro NGate/CSP and GOST TLS exercises |
| **Network engineering fundamentals** | GNS3/Cisco IOS, IPv4, VLAN, OSPF, HSRP, EtherChannel, routing, ARP, DHCP, DNS, NTP, SSH, Wireshark/tshark/tcpdump |

## Selected outcomes

- Created YARA rules designed to distinguish three supplied binary samples; validated all nine rule-to-file combinations.
- Developed four Suricata indicators for suspicious TCP, HTTP, ICMP and DNS patterns; tested them against a provided PCAP.
- Built a basic keyboard-dynamics program to compare inter-keystroke timing between two manual entries.
- Established an **IPsec VPN between two pfSense instances** and verified the IKE SA and Child SA status.
- Applied and documented firewall policy for RDP, SSH and SMTP access during a defined time window.
- Investigated traffic patterns consistent with DNS tunneling and reconstructed evidence from a lab capture.

These are **educational lab results**, not claims of production readiness or commercial experience.

## Repository scope

- This repo is a **portfolio description**, not a public mirror of school materials.
- It contains no private source submissions, challenge flags, credentials, VPN keys, network captures or exported configuration files.
- Original technical work is maintained in **private School 21 GitLab repositories**; the public narrative is intentionally high level.
- Acceptance of completed School 21 project work is reported by the author; no external grading certificate is reproduced here.

## Other public work

- [Webots Mower — C++ robotics prototype](https://github.com/AFLAiderLirk/webots-mower)
- [AiderKits — Java / Paper plugin](https://github.com/AFLAiderLirk/aiderkits)
- [AFLQuestBoard — Java / Paper plugin](https://github.com/AFLAiderLirk/AFLQuestBoard)
- [Cryptography learning notes](https://github.com/AFLAiderLirk/cryptography-learning-notes)
- [GitHub profile and résumés](https://github.com/AFLAiderLirk)
