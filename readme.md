# (CURRENTLY IN PROGRESS) Building a SOC + Honeynet in Azure (Live Traffic) 
![68747470733a2f2f692e696d6775722e636f6d2f5a5778653033652e6a7067](https://github.com/TerikaJ/Soc-Honeynet/assets/136477450/bc037cb5-677a-41b6-9389-724559b80b06)


## 🛡️ Introduction 🛡️
In this project, I constructed a mini honeynet in Azure, integrating log sources from various resources into a Log Analytics workspace. This data was utilized by Microsoft Sentinel to build attack maps, trigger alerts, and create incidents. I measured security metrics in the initial, unsecured environment for 24 hours, then applied security controls to harden the environment, followed by another 24-hour measurement period. The results of these metrics, which are detailed below, demonstrate the impact of the applied security controls:

**The metrics we will show are:**
- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)

## Architecture Before Hardening / Security Controls
![Architecture Diagram](https://i.imgur.com/aBDwnKb.jpg)

## Architecture After Hardening / Security Controls
![Architecture Diagram](https://i.imgur.com/YQNa9Pp.jpg)

**The architecture of the mini honeynet in Azure consists of the following components:**
- Virtual Network (VNet)
- Network Security Group (NSG)
- Virtual Machines (2 windows, 1 linux)
- Log Analytics Workspace
- Azure Key Vault
- Azure Storage Account
- Microsoft Sentinel

**Technologies, Azure Components, and Regulations Employed**
- Azure Virtual Network (VNet)
- Azure Network Security Groups (NSG)
- Virtual Machines (2 Windows VMs, 1 Linux VM)
- Log Analytics Workspace with Kusto Query Language (KQL) Queries
- Azure Key Vault for Secure Secrets Management
- Azure Storage Account for Data Storage
- Microsoft Sentinel for Security Information and Event Management (SIEM)
- Microsoft Defender for Cloud to Protect Cloud Resources
- Windows Remote Desktop for Remote Access
- Command Line Interface (CLI) for System Management
- PowerShell for Automation and Configuration Management
- [NIST SP 800-53 Revision 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) for Security Controls
- [NIST SP 800-61 Revision 2](https://www.nist.gov/privacy-framework/nist-sp-800-61) for Incident Handling Guidance
