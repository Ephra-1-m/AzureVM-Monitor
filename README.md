<h1>RDP Alert Sentinel</h1>


<h2>Description</h2>
This program is configured using Azure, Microsoft Sentinel, and a VM with Log Analytics to monitor RDP login events. It detects and sends notifications for successful RDP logins, enhancing security awareness.
<br />


<h2> Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>KQL</b>

<h2>Environments Used </h2>

- <b>Windows 11 Home</b> (23H2)
- <b>Microsoft Azure</b>
- <b>RDP (Remote Desktop Protocol)</b>


<h2>Configuration and Setup Overview:</h2>

<p align="center">
The virtual machine is connected to Azure Log Analytics for log monitoring and analysis. A public IP address is used for security purposes, and the VM is also connected to the virtual network for proper integration. Additionally, alert rules are configured to monitor specific events, such as successful RDP logins, and trigger notifications when conditions are met.<br/>
<img src="https://imgur.com/sObhR4m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connecting Windows Security Events via Azure Monitoring Agent (AMA) allows security logs from Windows to be sent to Azure Log Analytics. This enables real-time monitoring and analysis, helping detect threats and trigger alerts in Microsoft Sentinel. <br/>
<img src="https://i.imgur.com/UzHjbeu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
A security event rule named Great Success was created to trigger when there was a successful login that wasn’t from the system. Additionally, RDP ports were left open to allow remote access. <br/>
<img src="https://i.imgur.com/fqoI5DV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Signed in to the VM using RDP with the username and password created during the VM setup. After logging in, PowerShell was used to print the private IP address of the VM, which is part of the Azure Virtual Network, showing the IP as 10.0.0.4. <br/>
<img src="https://i.imgur.com/Booem8r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
As you can see, the incident titled Great Success showed up, indicating a successful RDP login. The event includes details such as the time of the login and other relevant information, confirming the triggered alert.  <br/>
<img src="https://i.imgur.com/nFiQX7c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Once you click on the event, you can view information like the date, event severity, event name, and other relevant details related to the RDP login. <br/>
<img src="https://i.imgur.com/u9nuiCP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Total cost for project:  <br/>
<img src="https://i.imgur.com/1XOy4hW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
