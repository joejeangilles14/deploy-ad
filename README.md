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
<img src="https://github.com/user-attachments/assets/bf580b7c-686d-4554-845d-d3e6c59df414" />
</p>
<p>
Be sure that "Create DNS Delegation" is unchecked and click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/7617a7af-d4dc-4c61-8775-b1a1e2a6945b" />
</p>
<p>
Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/4d238bc6-c437-4138-83a6-d39c1ecb2eca" />
</p>
<p>
Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/4ff8bc83-4cb4-41d5-9485-4b07269d52d3" />
</p>
<p>
Click Next.
</p>
<br />

p>
<img src="https://github.com/user-attachments/assets/fb20ca28-53e8-49a2-89ee-90ae21d46d9c" />
</p>
<p>
Click Install.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/1d471b66-ce4f-484b-9f70-9c947bd36c6e" />
</p>
<p>
The server will close itself. Once closed, wait a few minutes to log back into DC-1.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/933c62e6-086d-4efc-a31f-55b699044cfd" />
</p>
<p>
Log back in using mydomain.com\labuser as the username to access the remote server as a domain.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/985625d5-4e43-4250-922b-3afc9120f917" />
</p>
<p>
Click on the Start menu and select Active Directory Users and Computers under Windows Administrative Tools.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/212c6c36-278d-44c8-a2f0-f8ec11da4d4a" />
</p>
<p>
Right-click on mydomain.com, hover over new and select Organizational Unit.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/8042c2cc-44ff-4f98-93b5-57b5b7fc81e3" />
</p>
<p>
Name the OU "_EMPLOYEES" and click OK.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/8d07466e-a7e2-4c01-874c-2a7eb6bc2c59" />
</p>
<p>
Once the "_EMPLOYEES" organization unit has been created, go back to mydomain.com, hover over New, and select Organiztional Unit.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/198f11f9-38f8-43b9-9101-74acb0508d93" />
</p>
<p>
Name the OU "_ADMINS" and click OK.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/fc22475b-cae4-4931-903a-470c2cc29b92" />
</p>
<p>
Both organizaional units are now created.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/da51ee29-1ebf-4f9b-b782-5ad8f742b1d1" />
</p>
<p>
Right-click on mydomain.com and select Refresh.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/348893d0-761e-4996-84f5-fb6d90865df8" />
</p>
<p>
In the _ADMINS organizational unit right-click, hover over New, and select User.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/1ec7b7ef-4aa5-4f55-ae78-3b7af8cda690" />
</p>
<p>
Create a new user as Jane Smith and select Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/364b1b48-8a6f-430c-8c1d-7fa17885933f" />
</p>
<p>
Created a password and check "Password never expires" and used password Cyberlab123! for the sake of the lab. Click Next.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/9f04623e-d539-4905-a218-ada558e29004" />
</p>
<p>
Select Finish.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/3cf7e19a-b61e-445c-a5b9-ad7e9ec2321e" />
</p>
<p>
 In _ADMIN, right-click on the new user and select Properties.
</p>
<br />
