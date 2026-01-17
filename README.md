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
