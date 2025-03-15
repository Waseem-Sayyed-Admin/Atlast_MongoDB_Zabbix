# MongoDB Atlas API for Zabbix

## Overview
This repository contains a template for Zabbix that allows monitoring of MongoDB Atlas metrics through the MongoDB Atlas API. The template was developed to facilitate the integration between Zabbix and MongoDB Atlas. It offers automated collection of important metrics and allows automatic discovery of nodes and metrics, making it easier to configure and manage monitoring in Zabbix. The main features include:

- Cluster Status: Checks the overall health of MongoDB Atlas clusters.
- Performance Metrics: Monitors CPU, memory, and disk IO usage of each cluster.
- Database Metrics: Monitors read and write performance, latency, and connection utilization.
- Operations and Query Monitoring: Monitors the number of operations performed and the query execution time.

## Requirements
- Zabbix Server: Version 5.x or higher.
- MongoDB Atlas: Active account and access to the MongoDB Atlas API.
- API Key: Credentials to access the MongoDB Atlas API (with permissions to read metrics).
## How to Use
### MongoDB Atlas API Configuration:

- Create an API Key in MongoDB Atlas with the necessary permissions to access your cluster's metrics.
- Importing in Zabbix:

- Import the template into your Zabbix server.
- Configure a Host in Zabbix for MongoDB Atlas, using the API credentials and the MongoDB Atlas URL.

After configuration, the metrics will be available in Zabbix for analysis and real-time alerts.

Customization
This template can be easily extended or modified to meet specific MongoDB Atlas monitoring needs. The keys and triggers can be adjusted to collect additional information or to configure custom alerts.

How to get your organizationID in MongoDB Atlas
- organizationID -> {$KEY_CLUSTER}

![Org_key](https://github.com/user-attachments/assets/ed501e43-76a8-46fe-ad42-4d84ad59eb8c)

How to get API KEY MongoDB Atlas
- Public Key -> {$USER_KEY}
- Private Key -> {$PASS_KEY}

![User_pass_KEY](https://github.com/user-attachments/assets/cee62bf8-8674-4181-b8c9-8bef25d77fe2)


The information should be passed in MACROS below:

![MACROS_Template](https://github.com/user-attachments/assets/80d4577e-a333-4274-9322-87405092183f)

#### Troubleshoot:
If Discovery Not work then clone the host prototypes
![image](https://github.com/user-attachments/assets/fcb318ec-7935-4b54-81ed-8b7cb412745f) 
Disable orignal host prototypes 
![image](https://github.com/user-attachments/assets/6528ae07-1482-4604-ac54-3d8fe58ffeea)
Add macro on clone host prototypes 
![image](https://github.com/user-attachments/assets/6ac48fe5-00e3-4e28-bd75-caaf36e11e4f)
Check All host you can find discovery node of mongodb
