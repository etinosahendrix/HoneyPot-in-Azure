# Azure Sentinel: Real-Time Threat Detection + SOC + Honeynet
<br>

<img src="https://github.com/bayulus/azure-honeynet-livetraffic/blob/main/images/soc.png?raw=true" >

<p> This project covers the end-to-end setup of Azure Sentinel, a Security Information and Event Management (SIEM) solution. It includes connecting it to a live virtual machine acting as a honeypot to observe and analyze RDP brute force attacks worldwide. The custom PowerShell script enhances the analysis by looking up attackers' geolocation information and visualizing it on the Azure Sentinel Map.</p>

💻 **Languages and Tools Used For This Project:** 🛠️

![Static Badge](https://img.shields.io/badge/Azure%20Sentinel-blue?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/SQL-blue?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/Microsoft%20PowerShell-blue?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/Log%20Analytics%20Workspace-blue?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/VIRTUAL%20MACHINE-blue?style=for-the-badge)

🚨 Project Recap: Building an RDP Brute-Force Detection and Visualization System with Azure Sentinel

Here’s a high-level breakdown of the steps I followed to design and implement this cybersecurity monitoring solution:

🔹 Step 1:
Provisioned an Azure Sentinel workspace to collect, monitor, and analyze security-related data across the environment.

🔹 Step 2:
Deployed a Windows virtual machine as a honeypot, deliberately exposing RDP to simulate a vulnerable entry point and attract potential attackers.

🔹 Step 3:
Configured data connectors in Sentinel to ingest logs from the honeypot VM, and integrated additional sources for a more holistic threat picture.

🔹 Step 4:
Defined analytic detection rules in Sentinel to flag unusual login behavior, focusing on patterns consistent with RDP brute-force attacks. Alerts were configured to trigger upon rule matches.

🔹 Step 5:
Developed a custom PowerShell enrichment script that utilized the ipgeolocation.io API to fetch attacker location data based on IP addresses, including country, city, and coordinates.

🔹 Step 6:
Ingested the enriched geolocation data back into Sentinel and configured the map visualization tool to visually display attacker origins in real-time.

🔹 Step 7:
Established an incident response process, outlining remediation steps and escalation paths based on the severity and context of the detected threats.
