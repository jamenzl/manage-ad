<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Group Policy and Managing Accounts</h1>
This tutorial outlines the implementation and deployment of on-premises Active Directory with regards to Group Policy and Account Management within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Dealing with Account Lockouts
- Enabling and Disabling Accounts
- Observing Logs

<h2>Deployment and Configuration Steps</h2>

Log into Client-1 as mydomain.com\jane_admin

</p>
<br />
<p>
<img src="https://i.imgur.com/2sK8dDs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open system properties

Click "Remote Desktop"
</p>
<br />
Allow "domain users" access to remote desktop
<p>
<img src="https://i.imgur.com/06XvI62.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can now log into Client-1 as a normal, non-administrative user now

Normally you'd want to do this with Group Policy that allows you to change MANY systems at once

Log into DC-1 as jane_admin

Open PowerShell_ise AS AN ADMINISTRATOR
</p>
<br />
<p>
<img src="https://i.imgur.com/WSWNf74.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a new File and paste the contents of the script into it

Run thescript and observe the accounts being created
</p>
<br />
<p>
<img src="https://i.imgur.com/7noHouD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When finished, open ADUC and observe the accounts in the appropriate OU (_EMPLOYEES)
</p>
<br />
<p>
<img src="https://i.imgur.com/IgMn51F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Attempt to log into Client-1 with one of the accounts (take note of the password in the script)
</p>
<br />
<p>
<img src="https://i.imgur.com/cVR4q4Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
