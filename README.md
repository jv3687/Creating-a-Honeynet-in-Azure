<h1>Azure Honeynet: Cyber threats in Real Time</h1>



<h2>Introduction</h2>
In this project, I simulate a small-scale honeynet that attracts real-world traffic from attackers around the world through Microsoft Azure. The goal throughout this project is to demonstrate best security practices, incident response tactics, and the effects of hardening your environment. We'll accomplish this by intentionally deploying virtual machines that have no safeguard from the public internet to attract attackers into our environment. Then after ingesting some log sources into Log Analytics Workspace, Microsoft Sentinel will come in to create attack maps, alerts, and incidents. In order to showcase metrics before and after hardening the environment based off the incidents generated from the 24 hour capture.
<br />


<h2>Azure Components Used</h2>

- <b>Azure Virtual Network (VNet)</b> 
- <b>Azure Network Security Group (NSG)</b>
- <b>Virtual Machines (2x Windows, 1x Linux)</b>
- <b>Log Analytics Workspace with Kusto Query Language (KQL) Queries</b>
- <b>Azure Key Vault</b>
- <b>Azure Storage Account</b>
- <b>Microsoft Sentinel</b>
- <b>Microsoft Defender for Cloud</b>

<h2>Architecture Before Hardening </h2>

- <b>In the "BEFORE" stage of the project, all resources were initially deployed with the hope that attraction would be gained from the public internet. The Virtual Machines had both their Network Security Groups (NSGs) and built-in firewalls wide open, allowing unrestricted access from any source. Additionally, all other resources, such as storage accounts and databases, were deployed with public endpoints visible to the internet, without utilizing any Private Endpoints for added security. These machines were then left to the public for 24 hours to generate the following attack maps mentioned earler.</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
