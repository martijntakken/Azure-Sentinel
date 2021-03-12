# VirusTotal - Sentinel Playbooks

![VirusTotal](../../Images/VirusTotal.png)<br>
## Table of Contents

1. [Summary](#overview)
1. [Prerequisites](prerequisites)
1. [Deployment](#deployment)
1. [postdeployment](postdeployment)
1. [Authentication](#Authentication)
1. [References](#references)

<a name="summary"></a>

## Summary

This folder contains 4 playbooks: 
* Domain Report: Scan one or more domains using VirusTotal
* File Report: Scan one or more files using VirusTotal
* IP Report: Scan one or more IP addresses using VirusTotal
* Url Report: Scan one or more Urls using VirusTotal

![Playbook](../../Images/Playbook%20Sentinel.png)

All the playbooks are used to respond to an incident in Azure Sentinel and use VirusTotal to scan a domain, file IP address or url. The results of the scan are snown in the related Azure Sentinel Incident. 

<a name="Prerequisites"></a>

## Prerequisites

1. Playbook templates leverage the VirusTotal API for enrichment. To use the VirusTotal capabilities, first generate a Virus Total API key. Refer this link: [how to generate the API Key](https://developers.virustotal.com/v3.0/reference#getting-started)
1. The VirusTotal connector must be deployed in the same resource group as the playbooks

<a name="deployment"></a>

## Deployment instructions 

You can choose to deploy one ore more playbooks.

1. Deploy a playbook by clicking on "Deploy to Azure" button. This will take you to deplyoing an ARM Template wizard.
2. Fill in the required parameters:
    * Resource group
    * Region
    * Playbook name

### Domain Report:

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FPlaybooks%2FSentinel%2FDomain%20Report%20Sentinel.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTota%2FPlaybooks%2FSentinel%2FDomain%20Report%20Sentinel.json" target="_blank">
   <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>    
</a>

### File Report:

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FPlaybooks%2FSentinel%2FFile%20Report%20Sentinel.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FPlaybooks%2FSentinel%2FFile%20Report%20Sentinel.json" target="_blank">
   <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>    
</a>

### IP Report:

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FPlaybooks%2FSentinel%2FIP%20Report%20Sentinel.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FPlaybooks%2FSentinel%2FIP%20Report%20Sentinel.json" target="_blank">
   <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>    
</a>

### Url Report:

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FPlaybooks%2FSentinel%2FUrl%20Report%20Sentinel.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FPlaybooks%2FSentinel%2FUrl%20Report%20Sentinel.json" target="_blank">
   <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>    
</a>

<a name="postdeployment"></a>

## Post-Deployment instructions 
### a. Authorize connections
Once the deployment is completed, you will need to authorize each connection. There are connection for Azure Sentinel and VirusTotal. For each connection complete the following steps:
 1. Click edit API connection
 1. Fill in the necessary information
 1. Click Authorize
 1. Sign in
 1. Click Save


### b. Configurations in Azure Sentinel
For Azure Sentinel some additional configuration is needed:
1. Enable Azure Sentinel Analytics rules that create alerts and incidents which includes the relevant entities.
1. Configure automation rule(s) to trigger the playbooks.


<a name="references"></a>

## Learn more
* <a href="https://developers.virustotal.com/v3.0/reference" target="_blank">Virus Total API</a>