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
  - Log into DC-1 and install the "Active Directory Domain Services" role<br />
      ![image](https://github.com/user-attachments/assets/4a7f23e6-e740-44f2-a5c1-9c3a71d6fdba)
  - Promote DC-1 to a domain controller, creating a new forest (e.g., mydomain.com)<br />
      ![image](https://github.com/user-attachments/assets/b5eb907f-09f4-4632-b05e-227013cf8ab2)
<br />
<br />

2. Create OUs and Users:
  - In Active Directory Users and Computers (ADUC), create the "_EMPLOYEES" and "_ADMINS" OUs<br />
      ![image](https://github.com/user-attachments/assets/bf979b7e-bad7-4427-97ac-eebbe49868aa)
  - Add a new user, "jane_admin"<br />
      ![image](https://github.com/user-attachments/assets/50fc1adf-d70d-4205-8f13-662e35d36752)
  - Assign them to the "Domain Admins" group<br />
      ![image](https://github.com/user-attachments/assets/d4acb8b4-0c52-42d7-8d37-7cef1bdd32e0)
<br />
<br />

3. Join Client-1 to the Domain:
  - Restart Client-1 and join it to the domain (mydomain.com)<br />
      ![image](https://github.com/user-attachments/assets/0087ece3-efbe-408e-b9ed-047b9c991a3f)
  - Verify that Client-1 appears in ADUC and move it to the "_CLIENTS" OU<br />
      ![image](https://github.com/user-attachments/assets/6cd9dead-472b-4bd0-8cfc-48393cea782f)
  - Create a new OU named "_CLIENTS" and drag Client-1 into there<br />
      ![image](https://github.com/user-attachments/assets/ff68ebd3-9d2e-4da7-b197-6f06eebd7f41)
<br />
<br />
