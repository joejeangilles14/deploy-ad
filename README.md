<p align="center">
<img src="https://github.com/user-attachments/assets/994e5afb-bec5-4370-8cdd-aa1da7c30dcb" />
</p>

<h1>Deploying Active Directory</h1>
This tutorial explores deploying an Active Directory environment, from creation and management to deactivation and removal.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Micorsoft Remote Desktop
- Powershell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10</b> (21H2)

<h2>High-Level Deployment and Steps</h2>

- Install Active Directory 
- Create a Domain Admin user within the domain
- Join Client-1 to your domain (mydomain.com)
- Setup Remote Desktop for non-administrative users on Client-1
- Create users and attempt to log into client-1 with one of the users
<h2>Lifecycle Stages</h2>

<p>
<img src="https://github.com/user-attachments/assets/3d52dcb0-c3f1-4b1c-9c9a-ed4631b8c2a0" />
<img src="https://github.com/user-attachments/assets/afb4ab1d-367f-41a4-ae8f-eb31f3a8ff0b" />
</p>
<p>
Select both virtual machines, click on the three dots and start them both. Login to both and start the lab in DC-1.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/70378bcf-4102-454e-9fd2-18706ed0c3f8" />
<img src="https://github.com/user-attachments/assets/ad0f2b82-c2aa-4dee-a9cc-db3d1e9304ae" />
</p>
<p>
In Server Manager click on Add Roles and Features. Click on Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/9e5a6162-3f06-47b3-817e-deed991ef5da" />
</p>
<p>
Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/49ee9fc7-bc5c-43be-bc04-6d02f88ddf11" />
</p>
<p>
There should be only one server to select. Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/de6fb95b-bff4-4598-9922-6e985c74b11d" />
<img src="https://github.com/user-attachments/assets/76d1c5f1-aec0-4e47-b313-9aa7bd07f828" />
</p>
<p>
Select Active Directory Domain Services and click Add Features.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/16a5e523-2569-4894-878c-7ebdfd3944b5" />
</p>
<p>
Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/9e7c03d3-bc9f-4909-ae45-93367734b3a5" />
</p>
<p>
Leave as is and click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/c91d15cd-99fc-47d8-85fc-7340b2f15ad8" />
</p>
<p>
Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/f49efa88-a712-4e5a-97de-3880d69f5259" />
</p>
<p>
Check the "Restart the destination server automatically if required" box and select Yes.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/7de1594b-66b2-4139-aa9f-76bf924833ac" />
</p>
<p>
Select Install.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/2cf0fca0-0eaa-48d3-b8f8-deab600ff514" />
</p>
<p>
Once the installation is complete select Close.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/69ef1234-34d8-418e-8877-5c983be85f69" />
</p>
<p>
Now that Active Directory is installed, it's time to make the server a domain. Go back to Server Manager and click on the notification flag on the top right.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/e691059c-acf7-4319-8b8e-f00fb21ec902" />
</p>
<p>
Click on "Promote this server to a domain controller".
</p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/eec30dd6-d82a-4b0f-9451-59b73bc25454" />
</p>
<p>
Select "Add a new forest" and make mydomain.com as the root domain name. Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/09465212-ad5e-4ac2-a7db-b80c0e6801cb" />
</p>
<p>
Left checked boxes as is and created a password (in this case, I used Password1 for the sake of the lab). Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/eefb7a7b-0d5e-44c6-a56b-e4d3b86d4ba8" />
</p>
<p>
Uncheck "Create DNS Delegation" and click Next.
</p>
<br />
