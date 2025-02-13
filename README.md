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

Get logged into DC-1

Pick a random user account you previously created

Attempt to login with it 10 times with a bad password

</p>
<br />
<p>
<img src="https://i.imgur.com/bDGR1pQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
We must configure group policy to lockout the account after five (5) attempts

</p>
<br />
<p>
<img src="https://i.imgur.com/SnVX2bP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/OHiLu0E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After group polivy has been configured, attmept to log into DC-1 six (6) times with a bad password

You should get a pop up window telling you your account has been locked out

</p>
<br />
<p>
<img src="https://i.imgur.com/yTv9XvD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Observe that the account has been locked out within Active Directory

Unlock the account

Reset the password

Attempt to log in with it
</p>
<br />
<p>
<img src="https://i.imgur.com/f4hVGbY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/MQyEK9e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/JSlwKou.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Disable the same account in Active Directory
</p>
<br />
<p>
<img src="https://i.imgur.com/F4OrwWF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Attempt to login with it, observe the error message
</p>
<br />
<p>
<img src="https://i.imgur.com/01sdZo9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Re-enable the account and attempt to login with it
</p>
<br />
<p>
<img src="https://i.imgur.com/4EkEEkS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/JSlwKou.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Observe the logs (event viewer) in the Domain Controller
</p>
<br />
<p>
<img src="https://i.imgur.com/64h9XjW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Observe the logs (event viewer as ADMIN (use jane_admin)) on the client machine (client-1)
</p>
<br />
<p>
<img src="https://i.imgur.com/BdDy65r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
