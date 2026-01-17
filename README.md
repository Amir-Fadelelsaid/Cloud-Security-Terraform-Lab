# Cloud-Security-Terraform-Lab
Infrastructure-as-Code project deploying an Azure SOC environment using Terraform, including Log Analytics Workspace, Microsoft Sentinel, and secure storage resources.
![image](https://raw.githubusercontent.com/Amir-Fadelelsaid/Cloud-Security-Terraform-Lab/301896a2575c22d6fe20234ac2818d5484fce514/rg-cloud-soc-lab-resourcegroup.png)
**Figure 1 – Azure SOC Infrastructure Verification**

This screenshot confirms the successful deployment of the Azure SOC core components created using Terraform:
- Resource Group: `rg-cloud-soc-lab`
- Log Analytics Workspace: `law-cloud-soc`
- Microsoft Sentinel enabled (`SecurityInsights`)
- Storage Account: `cloudsocstorage*`


![image](https://github.com/Amir-Fadelelsaid/Cloud-Security-Terraform-Lab/blob/122772c8e0315225b9659720a9ec9e283e677e29/Law-Cloud-Soc-Overview.png)
## Log Analytics Workspace Deployment

This screenshot verifies that the Log Analytics Workspace (`law-cloud-soc`) was successfully created via Terraform and is active.  
It serves as the central data ingestion and analytics platform for the SOC, storing security telemetry that Microsoft Sentinel relies on.

![image](https://github.com/Amir-Fadelelsaid/Cloud-Security-Terraform-Lab/blob/fe6e07751f9c2168d2b3fce02f1566345ae6b8cc/sentinel-enabled.png)
## Microsoft Sentinel Enabled



This screenshot confirms that Microsoft Sentinel has been successfully enabled and is actively running on the Log Analytics Workspace (law-cloud-soc).  
Although no incidents are currently present, this is expected in a newly deployed SOC environment before data connectors and log sources are configured.

![image](https://github.com/Amir-Fadelelsaid/Cloud-Security-Terraform-Lab/blob/c5480358503593d1d9650b7088aa9b75abad2bac/Microsoft%20Sentinel%20%E2%80%93%20Data%20Connectors%20Configured.png)
## Data Connectors Connected

This screenshot shows the Microsoft Sentinel Data Connectors page with multiple Microsoft security services successfully connected, including Defender for Endpoint, Defender for Identity, Defender for Cloud Apps, Microsoft Entra ID Protection, and Microsoft Defender XDR. These connectors enable centralized ingestion of security telemetry into Sentinel, forming the foundation for threat detection, investigation, and SOC operations.

![image](https://github.com/Amir-Fadelelsaid/Cloud-Security-Terraform-Lab/blob/48b981a42aed15818a38b2b18af47c3f653e1fa0/Microsoft%20Entra%20ID.png)
## Installed Microsoft Entra ID
This screenshot confirms that the Microsoft Entra ID solution has been successfully installed from the Microsoft Sentinel Content Hub.

Rather than using legacy “Data Connectors,” modern Sentinel deployments ingest identity telemetry through the Microsoft Defender XDR platform.  
Microsoft Entra ID logs and security signals flow as:

Microsoft Entra ID → Microsoft Defender → Microsoft Sentinel

The installed Entra ID solution enables:

- Ingestion of sign-in logs and audit logs  
- Detection of risky users and risky sign-ins  
- Identity-based threat analytics and correlation  
- Built-in workbooks for identity visibility  
- Automated response via playbooks  
- Alignment with Microsoft’s current SIEM/XDR architecture  

This confirms the SOC is configured using Microsoft’s modern identity security pipeline and is capable of monitoring:

- Privileged account misuse  
- Suspicious authentication activity  
- Cloud identity compromise attempts  
- Lateral movement indicators tied to identity  

Even if the Data Connectors page shows “0,” this is expected behavior when using Defender-based ingestion. The Content Hub installation is the authoritative proof that Entra ID integration is active and operational.

![image](https://github.com/Amir-Fadelelsaid/Cloud-Security-Terraform-Lab/blob/a2d6e45bafee0ff7a8b407b7b212cfebcf3563ea/Sentinel%20Analytics%20rules%20engine%20verification.png)
## Sentinel Analytics Rules Engine Verification

This screenshot verifies that the Microsoft Sentinel Analytics Rules engine is deployed and operational.  
Analytics rules form the detection core of the SOC by analyzing security telemetry and generating alerts.

Although no rules are currently configured, this is expected in a newly deployed environment and confirms readiness for:
- Threat detection logic
- Alert generation
- Correlation rules
- SOC operational workflows

![image](https://github.com/Amir-Fadelelsaid/Cloud-Security-Terraform-Lab/blob/0b8bf92fbfa18623d3f826915c2351db4e924c16/Sentinel%20Workbooks%20Visualization%20layer.png)
## Microsoft Sentinel Workbooks (Visualization Layer)

This screenshot verifies that Microsoft Sentinel Workbooks are available and operational within the SOC environment.

Workbooks provide interactive dashboards and visual analytics for:
- Security events
- Incident trends
- Threat hunting results
- Data connector health
- SOC performance metrics

Although no custom workbooks are currently deployed, this confirms the environment is fully prepared for SOC visualization and monitoring once data ingestion increases.

![image](https://github.com/Amir-Fadelelsaid/Cloud-Security-Terraform-Lab/blob/0cadd59b0affb090576b3efc2953f54e89e54e05/Sentinel%20Automation%20And%20SOAR%20Readiness%20Verification.png)
## Microsoft Sentinel Automation (SOAR Readiness)

This screenshot verifies that Microsoft Sentinel Automation is enabled and accessible.

Automation rules and playbooks provide Security Orchestration, Automation, and Response (SOAR) capabilities, allowing:
- Automatic incident handling
- Triggered remediation workflows
- Integration with Azure Logic Apps
- Incident suppression and enrichment
- Playbook-based response actions

Although no automation rules or playbooks are currently configured, this confirms the SOC environment is fully prepared for automated incident response once detection rules and operational workflows are deployed.

