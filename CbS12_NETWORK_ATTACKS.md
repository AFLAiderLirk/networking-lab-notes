# CbS12 — Network attacks: educational lab summary

**Context:** independent summary of cybersecurity coursework at School 21. Five task files were committed and pushed to the private GitLab `develop` branch (last observed commit: `2b7c4ac`). This is **not** an official assessment or a claim that the project has passed peer review.

## Objective

Learn to map security incidents to MITRE ATT&CK, identify configuration weaknesses, observe HTTP traffic in an isolated proxy setup, investigate a packet capture, and use search-engine reconnaissance responsibly.

## Work performed

| Area | Technologies | What was done | Validation / limitations |
| --- | --- | --- | --- |
| Threat classification | MITRE ATT&CK | Mapped eight incident scenarios to tactics and techniques | Written mapping submitted; independent grading not confirmed |
| MongoDB security checks | Python, PyMongo, TCP sockets, ThreadPoolExecutor | Built a scanner for private or loopback networks that tests whether unauthenticated clients can list databases | Syntax and local execution passed; positive detection against an intentionally unsecured MongoDB instance **not yet tested** |
| HTTP proxy inspection | Python, mitmproxy, curl | Built an addon that logs HTTP form submission metadata, including methods, URLs without query values, and field names | Local GET, POST form-encoded, and multipart tests returned HTTP 200 and were logged; field values and passwords are not collected |
| Network forensics | Wireshark/tshark, DNS, Python | Investigated a supplied PCAP, detected unusual dnscat-style DNS traffic, reconstructed a session, and identified evidence of DNS tunneling | Packet inspection and decoded command-session output were reviewed; challenge flag deliberately excluded from public documentation |
| Exposure research | FOFA, nginx, CVE references | Recorded a search query and example result for a legacy nginx version associated with CVE-2017-7529 | Search result does not prove the device is vulnerable; no exploitation conducted |

## Key concepts learned

- Difference between a MITRE **tactic** (attacker objective) and **technique** (method)
- Authentication checks versus simple open-port checks
- Proxy-based inspection of HTTP request metadata in a local test environment
- DNS tunneling indicators: unusually long hex-like subdomains, repeated requests, and command output encoded in DNS labels
- IDS/IPS controls and the role of DNS monitoring in detecting suspicious traffic
- Limits of passive version-based vulnerability identification

## Environment

Kali Linux, Git/GitLab, Python 3, PyMongo, mitmproxy / mitmdump, curl, Wireshark / tshark, VirtualBox-based lab.

## Publication and ethics

This document is an **independent portfolio explanation**, not a mirror of School 21 source materials. Private GitLab contents, original assignment text, challenge flags, raw captures, scripts submitted for school evaluation, credentials, server IPs, tokens, and personal data are intentionally omitted. The lab work does not imply production deployment, commercial pentest experience, or authorization to probe third-party systems.
