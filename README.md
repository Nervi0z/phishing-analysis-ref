# phishing-analysis-ref

A curated list of tools, platforms, and resources for detecting, analyzing, and investigating phishing.

Covers threat intelligence feeds, URL/file scanners, email analysis, sandboxes, simulation frameworks, and OSINT utilities. Maintained as a living reference for SOC analysts, incident responders, and security researchers.

> Some tools in the offensive/simulation section are intended for authorized testing only. Using them against systems you don't own or without explicit permission is illegal.

---

## Contents

- [Threat Intelligence & Data Sources](#threat-intelligence--data-sources)
- [Analysis Tools](#analysis-tools)
- [Prevention & Detection](#prevention--detection)
- [Simulation & Awareness Training](#simulation--awareness-training)
- [Supporting Tools](#supporting-tools)
- [Learning Resources](#learning-resources)
- [Contributing](#contributing)

---

## Glossary

| Term | Meaning |
|------|---------|
| IOC | Indicator of Compromise (URL, file hash, IP, etc.) |
| Sandbox | Isolated environment for safely executing suspicious files or URLs |
| MITM | Man-in-the-Middle attack |
| OSINT | Open Source Intelligence |
| FOSS | Free and Open Source Software |
| Gateway | A filtering control point, in this context for email traffic |

---

## Threat Intelligence & Data Sources

### Phishing Feeds & Databases

| Tool | Description | Model | Link |
|------|-------------|-------|------|
| **PhishTank** | Collaborative database of verified phishing URLs | Free/API | [phishtank.com](https://www.phishtank.com/) |
| **OpenPhish** | Real-time phishing URL feed, high quality | Commercial/API | [openphish.com](https://openphish.com/) |
| **CheckPhish** | AI-based phishing detection with API access | Freemium/API | [checkphish.ai](https://checkphish.ai/) |
| **MISP Project** | FOSS platform for correlating and sharing IOCs including phishing indicators | FOSS | [misp-project.org](https://www.misp-project.org/) |
| **PhishStats** | Statistics and data on phishing campaigns | Free/API | [phishstats.info](https://phishstats.info/) |

### IP & Domain Reputation

| Tool | Description | Model | Link |
|------|-------------|-------|------|
| **AbuseIPDB** | Collaborative database of IPs associated with malicious activity | Freemium/API | [abuseipdb.com](https://www.abuseipdb.com/) |
| **VirusTotal** | Checks IPs and domains against multiple engines and datasets | Freemium/API | [virustotal.com](https://www.virustotal.com/) |
| **Cisco Talos Reputation** | IP/domain reputation lookup from Cisco Talos | Free | [talosintelligence.com](https://talosintelligence.com/reputation_center) |
| **URLVoid** | Scans URLs and domains across multiple reputation services | Freemium/API | [urlvoid.com](https://www.urlvoid.com/) |
| **IBM X-Force** | Threat intelligence portal with IP/URL/vulnerability reputation | Freemium/API | [exchange.xforce.ibmcloud.com](https://exchange.xforce.ibmcloud.com/) |

---

## Analysis Tools

### URL & File Scanners

| Tool | Description | Model | Link |
|------|-------------|-------|------|
| **VirusTotal** | De facto standard for scanning URLs and files against multiple AV engines | Freemium/API | [virustotal.com](https://www.virustotal.com/) |
| **URLScan.io** | Scans URLs and returns detailed info on page content and loaded resources | Freemium/API | [urlscan.io](https://urlscan.io/) |
| **Any.Run** | Interactive online sandbox, good for quick URL/file triage | Freemium | [any.run](https://any.run/) |
| **Hybrid Analysis** | Free malware analysis service combining sandbox and static analysis | Free | [hybrid-analysis.com](https://www.hybrid-analysis.com/) |
| **ScanURL** | Independent web service for scanning URLs | Free | [scanurl.net](https://scanurl.net/) |

### Email Analysis (Headers, Content, Attachments)

| Tool | Description | Model | Link |
|------|-------------|-------|------|
| **MxToolbox Header Analyzer** | Straightforward online parser for email headers | Free | [mxtoolbox.com/EmailHeaders.aspx](https://mxtoolbox.com/EmailHeaders.aspx) |
| **Google Messageheader** | Header analyzer from Google's G Suite Toolbox | Free | [toolbox.googleapps.com](https://toolbox.googleapps.com/apps/messageheader/) |
| **PhishTool** | Integrated email analysis and IOC extraction | Commercial | [phishtool.com](https://phishtool.com/) |
| **ThePhish** | FOSS automated EML analysis framework using TheHive/Cortex/MISP | FOSS | [GitHub](https://github.com/emalderson/ThePhish) |

### Sandboxes

| Tool | Description | Model | Link |
|------|-------------|-------|------|
| **Any.Run** | Interactive cloud sandbox, good for visual triage | Freemium | [any.run](https://any.run/) |
| **Cuckoo Sandbox** | Standard FOSS sandbox for automated malware analysis, self-hosted | FOSS | [cuckoosandbox.org](https://cuckoosandbox.org/) |
| **Hybrid Analysis** | CrowdStrike's free online sandbox | Free | [hybrid-analysis.com](https://www.hybrid-analysis.com/) |
| **Joe Sandbox Cloud** | Commercial sandbox with detailed behavioral analysis | Commercial | [joesandbox.com](https://www.joesandbox.com/) |
| **Triage** | Malware analysis and sandbox platform | Commercial | [tria.ge](https://tria.ge/) |

---

## Prevention & Detection

### Email Security Gateways

Enterprise solutions, mostly commercial:

- **Proofpoint Email Protection** — advanced threat protection, widely deployed
- **Mimecast Email Security** — cloud-based with sandboxing, URL/attachment protection, DMARC
- **Barracuda Email Protection** — full suite including gateway, DMARC, and IR
- **Microsoft Defender for Office 365** — integrated into M365
- **Google Workspace Security** — integrated in Gmail/Workspace including sandbox
- **Cofense** — focused on phishing reported by users, detection and response
- **Avanan (Check Point)** — cloud-native API-based security for O365/Gmail

### Browser Protection

| Tool | Description | Model |
|------|-------------|-------|
| **Microsoft SmartScreen** | Built into Edge and Windows, blocks malicious sites and downloads | Built-in |
| **Google Safe Browsing** | Underlying technology in Chrome, Firefox, and Safari | Built-in/API |
| **Netcraft Extension** | Browser extension for phishing site detection | Free |
| **uBlock Origin** | Blocks known malicious domains via filter lists | FOSS |

---

## Simulation & Awareness Training

### Awareness Platforms

Commercial platforms for training end users:

- **KnowBe4** — phishing simulation and security awareness training
- **Cofense PhishMe** — simulation with integrated user reporting
- **Proofpoint Security Awareness Training** — training modules and simulation
- **Microsoft Attack Simulation Training** — within Microsoft 365 Defender
- **GoPhish** — FOSS framework usable for internal training (requires manual setup)

### Phishing Simulation Frameworks

> Intended for authorized penetration testing and internal simulations only.

| Tool | Description | Model | Link |
|------|-------------|-------|------|
| **GoPhish** | FOSS standard for creating and managing phishing simulation campaigns | FOSS | [getgophish.com](https://getgophish.com/) |
| **SET (Social-Engineer Toolkit)** | Classic Python framework for social engineering attacks | FOSS | [GitHub](https://github.com/trustedsec/social-engineer-toolkit) |
| **Evilginx2/3** | Advanced MITM framework for capturing credentials and session tokens (2FA bypass) | FOSS | [GitHub](https://github.com/kgretzky/evilginx2) |
| **King Phisher** | FOSS campaign framework with server management | FOSS | [GitHub](https://github.com/rsmusllp/king-phisher) |
| **CredSniper** | Tool for building credential-harvesting login pages | FOSS | [GitHub](https://github.com/ustayready/CredSniper) |

---

## Supporting Tools

### OSINT

| Tool | Description | Model | Link |
|------|-------------|-------|------|
| **Maltego** | Graph-based platform for relationship analysis and OSINT | Freemium/Commercial | [maltego.com](https://www.maltego.com/) |
| **SpiderFoot** | OSINT automation tool, self-hosted or cloud | FOSS/Commercial | [spiderfoot.net](https://www.spiderfoot.net/) |
| **theHarvester** | Collects emails, subdomains, and hosts from public sources | FOSS | [GitHub](https://github.com/laramies/theHarvester) |
| **Recon-ng** | Modular OSINT framework in Python | FOSS | [GitHub](https://github.com/lanmaster53/recon-ng) |

### General Security Frameworks

| Tool | Description | Model | Link |
|------|-------------|-------|------|
| **Metasploit Framework** | Exploit development and execution platform | FOSS/Commercial | [metasploit.com](https://www.metasploit.com/) |
| **BeEF** | Browser exploitation framework, useful for analyzing phishing kits | FOSS | [beefproject.com](https://beefproject.com/) |

---

## Learning Resources

### Workflow Examples

**Quick URL triage:**
`Suspicious URL → URLScan.io or VirusTotal → Review results and categorize`

**Phishing email analysis:**
`Get EML → Parse headers (MxToolbox) → Extract IOCs (URLs, IPs, hashes) → Check IOCs (VirusTotal, AbuseIPDB, PhishTank) → Analyze attachments/URLs in sandbox (Any.Run, Hybrid Analysis)`

**Campaign investigation:**
`Identify pattern (subject, sender, phishing kit) → Search threat intel (MISP, PhishStats) → OSINT on infrastructure (Maltego, Recon-ng)`

### References

- [APWG Phishing Activity Trends Reports](https://apwg.org/trendsreports/) — quarterly phishing trend data
- [MITRE ATT&CK — Phishing (T1566)](https://attack.mitre.org/techniques/T1566/) — technical breakdown of the tactic
- [Phishing.org](https://www.phishing.org/) — general phishing reference

### Related Lists

- [awesome-incident-response](https://github.com/meirwah/awesome-incident-response)
- [awesome-threat-intelligence](https://github.com/hslatman/awesome-threat-intelligence)
- [awesome-osint](https://github.com/jivoi/awesome-osint)
- [awesome-soc](https://github.com/cyb3rxp/awesome-soc)

---

## Contributing

Before submitting, check that the tool isn't already listed and that it's directly relevant to phishing analysis, detection, or prevention. Provide a working link, a clear description, and the licensing model. Follow the table format used in existing sections.

Quality over quantity — well-maintained and widely used tools are preferred.

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full process.

---

License: [CC0 1.0 Universal](LICENSE)
