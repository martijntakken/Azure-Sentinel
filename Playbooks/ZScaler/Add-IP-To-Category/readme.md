# ZScaler - Add IP to category

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

This folder contains 1 playbooks: 
* Add IP to category: Add one or more IP addresses to an existing ZScaler category

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
    * Storage account name (newly created storage account, which is used by the playbook)
    * ZScaler Admin Url
    * ZScaler Key
    * ZScaler Username
    * ZScaler Password
    * Category (Name of an existing ZScaler category)

### Add IP to category:

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2FZScaler%2FPlaybooks%2FZScaler%2FAdd-IP-To-Category%2FAzureDeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2FZScaler%2FPlaybooks%2FZScaler%2FAdd-IP-To-Category%2FAzureDeploy.json" target="_blank">
   <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>    
</a>


<a name="postdeployment"></a>

## Post-Deployment instructions 
### a. Authorize connections
Once the deployment is completed, you will need to authorize each connection. There are connection for Azure KeyVault and Azure Sentinel. For each connection complete the following steps:
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
* <a href="https://help.zscaler.com/zia/api" target="_blank">Zscaler API</a>