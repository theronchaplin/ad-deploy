<img src=https://github.com/user-attachments/assets/b0b2b2d4-c2ed-47b6-b59c-9da1d87514c6>
<br />
<br />

<h1>Deploying Active Directory</h1>

This phase focuses on installing Active Directory Domain Services, configuring a new forest, creating organizational units (OUs), and adding users. The goal is to establish a functioning Active Directory environment, including domain join for client machines.<br />
<br />
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Services
- PowerShell
<br />
<br />

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)
<br />
<br />

<h2>Walkthrough Steps</h2>

1. Install AD Domain Services:
  - Log into DC-1 and install the "Active Directory Domain Services" role
  - Promote DC-1 to a domain controller, creating a new forest (e.g., mydomain.com)
<br />
<br />

2. Create OUs and Users:
  - In Active Directory Users and Computers (ADUC), create the "_EMPLOYEES" and "_ADMINS" OUs
  - Add a new user, "jane_admin," and assign them to the "Domain Admins" group
<br />
<br />

3. Join Client-1 to the Domain:
  - Restart Client-1 and join it to the domain (mydomain.com)
  - Verify that Client-1 appears in ADUC and move it to the "_CLIENTS" OU
<br />
<br />
