# VirusTotal Logic Apps connector

![VirusTotal](./Images/VirusTotal.png)<br>
## Table of Contents

1. [Overview](#overview)
1. [Actions supported by VirusTotal custom connector](#actions)
1. [Prerequisites](prerequisites)
1. [Deployment](#deployment)
1. [postdeployment](postdeployment)
1. [Authentication](#Authentication)
1. [References](#references)

<a name="overview"></a>

## Overview
General info about this product and the core values of this integration. <br>


<a name="actions"></a>

## Actions supported by VirusTotal custom connector

| Action | Description |
| --------- | -------------- |
| **Get URL report** | ID Action used to Retrieve information about a URL. Uses uses a MD5 hash of the URL as input |
| **Get a IP report** | Action used to retrieve information about an IP address. Uses an IP address as input |
| **Get file report** | Action used to retrieve information about a file. Uses a SHA-256, SHA-1 or MD5 for identifying the file |
| **Get Domain report** | Action used to retrieve information about an Internet domain. Usess a domain as input |
| **Analyze a URL** | Action used to analyze a Url. Returns an id that can be used for the 'Get URL report' action. |
| **Upload and analyze a file** | Action used to upload and analyze a file. The total payload size can not exceed 32MB. |
| **Retrieve information about a file or URL analysis** | Action used to retrieve information about a file or URL analysis |

<a name="deployall"></a>

## Deployment Custom Connector 

This package includes:

* Custom connector for VirusTotal
* Twelve playbook templates leverage VirusTotal custom connector

You can choose to deploy the connector and optionally one ore more playbooks, each seperately from it's specific folder. Instructions for deploying the playbooks are located in the playbook folders. 

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FConnector%2FAzureDeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FConnector%2FAzureDeploy.json" target="_blank">
   <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>    
</a>

<a name="prerequisites"></a>

### Prerequisites for using and deploying Custom Connector
1. Playbook templates leverage VirusTotal for enrichment. To use this VirusTotal capabilities,generate a Virus Total API key first. Refer this link [ how to generate the API Key](https://developers.virustotal.com/v3.0/reference#getting-started)

<a name="deployment"></a>
### Deployment instructions 
1. Deploy the Custom Connector and playbooks by clicking on "Deploy to Azure" button. This will take you to deplyoing an ARM Template wizard.
2. Fill in the required parameteres:
    * Name

<a name="references"></a>

## Learn more
* <a href="https://developers.virustotal.com/v3.0/reference" target="_blank">Virus Total API</a>