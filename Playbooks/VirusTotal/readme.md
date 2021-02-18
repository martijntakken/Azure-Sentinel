# VirusTotal Logic Apps connector

![VirusTotal](./VirusTotal.png)<br>
## Table of Contents

1. [Overview](#overview)
1. [Actions supported by VirusTotal custom connector](#actions)
1. [Deployment](#deployment)
1. [Authentication](#Authentication)

<a name="overview"></a>

## Overview
General info about this product and the core values of this integration. <br>


<a name="actions"></a>

## Actions supported by VirusTotal custom connector

| Action | Description |
| --------- | -------------- |
| **Analyze a URL** | Action used to analyze a Url. Returns an id that can be used for the 'Get URL report' action. |
| **Get URL report** | ID Action used to Retrieve information about a URL. Uses the ID from the 'Analyze a URL' action as input |
| **Get a IP report** | Action used to retrieve information about an IP address |
| **Retrieve information about a file or URL analysis** | Action used to retrieve information about a file or URL analysis |
| **Get file report** | Action used to retrieve information about a file. Uses a SHA-256, SHA-1 or MD5 for identifying the file |
| **Upload and analyze a file** | Action used to upload and analyze a file. The total payload size can not exceed 32MB. |
| **Get Domain report** | Action used to retrieve information about an Internet domain |


<a name="deployment"></a>

## Deployment instructions 

Prior using this custom connector, it should be deployed in the Resource Group where the playbooks that will include it are located.
<br>
1. Deploy the Custom Connector by clicking on "Deploy to Azure" button. This will take you to deplyoing an ARM Template wizard.
2. Fill in the required paramteres:
    * Connector name: Please enter the custom connector(ex: VirusTotal)


<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FConnector%2FAzureDeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmartijntakken%2FAzure-Sentinel%2Ffeature%2Fvirustotal%2FPlaybooks%2FVirusTotal%2FConnector%2FAzureDeploy.json" target="_blank">
   <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>    
</a>


<a name="authentication"></a>

## Authentication
This connector supports the following authentication types:
* API Key Authentication