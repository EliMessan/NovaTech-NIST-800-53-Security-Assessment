# NovaTech Solutions | NIST SP 800-53 Security Assessment

## Project Overview
This project documents a simulated security control assessment of NovaTech Solutions, a fictional organization operating an Ubuntu Server environment. I evaluated 12 selected NIST SP 800-53 security controls through configuration reviews, technical testing, vulnerability assessment, and evidence analysis.

The objective was to identify control implementation gaps, evaluate security risks, and recommend practical remediation actions using a structured assessment methodology.

> **Disclaimer:** NovaTech Solutions is a fictional organization. All testing was performed in an authorized, isolated lab environment. This project does not represent an official NIST certification or authorization to operate.

## Lab Environment and Tools
- Host: Apple MacBook Air (Apple Silicon)
- Virtualization: UTM
- Operating System: Ubuntu Server 26.04 LTS
- Security Framework: NIST SP 800-53
- Tools: Linux CLI, SSH, UFW, Lynis, ClamAV, systemd journal, Linux permissions and account management utilities
- Documentation: Security control assessment tracker, technical evidence, risk documentation, POA&M, and final assessment report

## Security Controls Assessed
| Control | Control Name | Assessment Focus |
|---|---|---|
| AC-2 | Account Management | User accounts, account settings, and privileged access |
| AC-3 | Access Enforcement | File and directory permissions |
| AC-6 | Least Privilege | Administrative permissions and access restrictions |
| AU-2 | Event Logging | System audit and event logging configuration |
| AU-6 | Audit Record Review, Analysis, and Reporting | Review of security-relevant log entries |
| CM-6 | Configuration Settings | Security-relevant system settings |
| CM-7 | Least Functionality | Unnecessary services and exposed functionality |
| SI-2 | Flaw Remediation | Software updates and patch management |
| SI-3 | Malicious Code Protection | ClamAV detection and quarantine testing |
| RA-5 | Vulnerability Monitoring and Scanning | Lynis security assessment and recommendations |
| SC-7 | Boundary Protection | UFW firewall rules and network exposure |
| IA-2 | Identification and Authentication (Organizational Users) | Authentication and SSH configuration |

## Assessment Methodology
1. Defined the Ubuntu Server assessment scope and identified applicable controls.
2. Examined account, access, authentication, logging, service, and firewall configurations.
3. Performed technical tests and captured command output as assessment evidence.
4. Ran Lynis to identify potential hardening opportunities.
5. Tested ClamAV malware detection and quarantine using the harmless EICAR test file.
6. Documented observations, implementation gaps, risk ratings, and remediation recommendations.

## Selected Technical Findings

### Malware Protection — SI-3
ClamAV detected EICAR test files and quarantined them during lab testing. This demonstrates successful detection and quarantine in the tested scenario, but does not establish complete coverage of every malware-protection requirement.

### Vulnerability Assessment — RA-5
A Lynis audit completed 253 tests and produced a hardening index of 67. The resulting recommendations provide a baseline for prioritizing system hardening. The index is a tool-specific indicator, not a formal NIST compliance score.

### Boundary Protection — SC-7
UFW was active with incoming traffic denied by default and outgoing traffic allowed. SSH access on port 22 remained permitted, presenting an opportunity to further restrict management access to trusted sources.

### Authentication — IA-2
The assessment identified password-aging and SSH authentication settings requiring further review or hardening. Technical configuration checks were documented without claiming full compliance with the control.

## Project Deliverables

| Deliverable | Description |
|---|---|
| [Final Security Assessment Report](NovaTech_Final_Security_Assessment_Report.pdf) | Professional assessment report documenting findings, control implementation gaps, risk analysis, and remediation recommendations. |
| [NIST SP 800-53 Assessment Tracker](NovaTech_NIST_800-53_Reviewed.xlsx) | Assessment documentation for 12 security controls, including findings, evidence, implementation status, and risk ratings. |
| [Risk Register](NovaTech_Risk_Register.xlsx) | Documents identified security weaknesses, associated risks, severity levels, and recommended risk treatment. |
| [Plan of Action and Milestones (POA&M)](NovaTech_POAM.xlsx) | Tracks proposed remediation actions, priorities, responsible roles, and target completion dates. |
| [Technical Evidence](04-Technical-Evidence/) | Screenshots and supporting records organized by NIST security control. |

### Risk Management and Remediation Planning

Beyond technical testing, this project demonstrates the security assessment lifecycle. I identified and documented security control weaknesses, evaluated their risk severity, and developed a Risk Register and POA&M to translate findings into prioritized remediation plans. The proposed actions are documented for future implementation and verification.

## Skills Demonstrated
NIST SP 800-53 control assessment, Linux security administration, access control testing, least privilege, security logging, vulnerability assessment, endpoint malware protection, firewall review, evidence collection, risk analysis, remediation planning, and technical reporting.

## Key Takeaway
This project strengthened my ability to approach security from an assessor's perspective: identify the control objective, collect relevant evidence, test the implemented configuration, distinguish verified results from gaps, and translate findings into actionable remediation recommendations.

## Author
Eli Messan | Information Technology Student, Towson University
