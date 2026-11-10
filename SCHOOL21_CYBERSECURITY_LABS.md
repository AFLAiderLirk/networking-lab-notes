# School 21 · Cybersecurity practice (public portfolio summary)

**Project work in private GitLab repositories; public summaries only.**

I study cybersecurity at School 21 alongside Information Security at Novgorod State University. My assessed School 21 projects are stored in private repositories. This document explains the **practical work I performed**, the tools involved, and the limits of the evidence, without publishing school solutions, original task text, flags, captures, credentials, keys, or exported firewall configurations.

School 21 has **accepted** my completed coursework in enterprise infrastructure planning, network attack analysis, threat detection, and protected network design (**completion and acceptance reported by me**). Other secure-communications exercises below are described as practice, without an unverified claim of acceptance.

## Enterprise infrastructure and network architecture

- Designed educational small-organization LAN topologies, separating employee endpoints, internal services, and public-facing resources into security zones, including a DMZ.
- Worked with asset inventory, IPv4 subnetting, operating systems and services, account and access boundaries, and Active Directory concepts.
- Selected security controls using least privilege, defense in depth, the CIA triad, firewalls, VPNs, and endpoint/network protections.
- Prepared topology diagrams and structured inventories, including remote-access design considerations.

**Tools and concepts:** diagrams.net, TCP/IP, network segmentation, DMZ, asset inventory, firewall and VPN architecture.

## Network attack investigation and security assessment

- Mapped simulated incidents to MITRE ATT&CK tactics and techniques.
- Developed a Python/PyMongo lab scanner to identify MongoDB servers that permit unauthenticated database enumeration on authorized networks. The positive-detection scenario was not independently verified against an intentionally exposed database.
- Built a mitmproxy addon to observe HTTP form-submission **metadata** in a local lab, avoiding capture of submitted field values and passwords. Tested common request methods and form encodings.
- Analyzed PCAP traffic to recognize dnscat-style DNS tunneling and reconstruct evidence from an encoded session.
- Used FOFA and CVE advisories for version-based exposure research, without treating search results as proof of exploitation or actively exploiting third-party services.

**Tools and concepts:** Kali Linux, Python, PyMongo, mitmproxy, Wireshark, tshark, tcpdump, MITRE ATT&CK, DNS, HTTP, PCAP analysis, FOFA and CVE research.

## Detection engineering and behavioral signals

- Inspected three binary samples and authored **YARA** signatures combining plaintext and hexadecimal indicators, including a file-size condition. Checked each rule against all three samples to avoid false matches within the supplied set.
- Investigated a supplied network capture and developed **Suricata** rules for four distinct suspicious patterns: C2-like TCP handshake, suspicious HTTP request, ICMP tunnel marker, and malicious-looking DNS query. Verified the rules through offline PCAP replay and alerts.
- Wrote a Python keyboard-dynamics exercise using **pynput** and **statistics**: capture intervals between successive keystrokes during two manual entries of the same phrase and compare mean timing deviations against a threshold.
- Kept the work limited to isolated educational samples; these are lab detectors, not production-hardened security controls.

**Tools and concepts:** YARA, Suricata, tshark, PCAP, packet signatures, DNS/HTTP/ICMP indicators, Python, pynput, statistical comparison.

## Secure network design, VPNs, and firewall policy

- Deployed two **pfSense CE 2.6.0** virtual firewalls in VirtualBox with separate LAN subnets and a shared isolated WAN segment.
- Configured a site-to-site **IPsec/IKEv2** VPN with Phase 1 and Phase 2 settings. Verified an established IKE security association and installed Child SA on both peers.
- Created pfSense filtering rules for VPN-side traffic and lab restrictions: block RDP (TCP 3389), block SSH (TCP 22), and permit SMTP (TCP 25) only during a scheduled window, with a deny rule outside that window.
- Prepared equivalent **iptables** rules as a text-based educational exercise; the rules were not deployed to a production firewall.
- Documented interface addressing, virtualization, and troubleshooting of NAT versus isolated virtual networks.

**Tools and concepts:** pfSense, VirtualBox, IPsec/IKEv2, ESP, PSK, LAN/WAN, host-only and internal networks, firewall rule ordering, schedules, iptables.

## Secure communications and network protocol labs

- Configured **nginx HTTPS/TLS** and inspected handshake traffic in Wireshark/tshark.
- Practiced **OpenVPN**, Easy-RSA CA/certificate setup, TUN interfaces, and packet capture with tcpdump.
- Worked with isolated **CryptoPro NGate / CSP 5.0 / GOST TLS** educational scenarios.
- Used **GNS3 and Cisco IOS** in networking exercises involving IPv4 addressing, ARP, DHCP, DNS, NTP, SSH, VLAN, OSPF, EtherChannel, HSRP, and traffic inspection.

These scenarios demonstrate learning and configuration practice; acceptance of every individual exercise is not asserted.

## How I work

- Build isolated lab environments; avoid probing systems without authorization.
- Document assumptions, verify configurations and observable results, and distinguish tested behavior from planned behavior.
- Use Git/GitLab to manage educational submissions and GitHub to share **independent descriptions**, not private coursework.

## Scope and publication boundaries

This is a self-authored high-level portfolio narrative. The original School 21 repositories, assignments, code submitted for grading, raw packet captures, network exports, credentials, VPN secrets, flags, and internal infrastructure details remain private. These are educational exercises, **not paid employment, security certifications, penetration tests of third-party systems, or production deployments**.
