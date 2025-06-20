<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services


<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/user-attachments/assets/86ca7a7a-c8dc-4fef-b780-091c046537ff)
![image](https://github.com/user-attachments/assets/2dc6edf7-3cab-4c1b-a75e-06d85b046cc7)
![image](https://github.com/user-attachments/assets/2c179053-6c9d-4ee6-9d33-31c98c896da2)
<p>I open Group Policy Management in Windows Server to create password rules on lockouts and timeouts. I set the accounts to lock out after 5 fail attempts.</p>

![image](https://github.com/user-attachments/assets/18760da2-542f-4e91-a723-03580b3ae799)
<p> This gave a overview of the password policy or rules set in place for my domain.</p>

![image](https://github.com/user-attachments/assets/4dcf4991-283f-4742-b66b-13bcbc16212f)
<p>I looked up a fake user to see how AD work.</p>

![image](https://github.com/user-attachments/assets/240f67dc-b605-47a6-a451-4b3e2f538960)
<p>I double right click on the user name to disable their account. Like in a scenario if they were leaving the organization or if someone had got into their account.</p>

![image](https://github.com/user-attachments/assets/8ad35e0d-2ded-4986-b815-12e7f2de08b4)
<p>Then I reactive the account by double right clicking on the account.</p>

![image](https://github.com/user-attachments/assets/40d72610-1a58-42ef-92e1-2bdeff364f9b)
<p> I went into the properties of the user account to see how password setting can be implement on individual account.</p>

![image](https://github.com/user-attachments/assets/0e8375d5-45ef-4bf3-8d04-a88292c5e545)
<p> I try to reset the user password and unlock it. Also, have an understanding of how this works in the real world when someone calls the help desk.</p>

<p>
  
<h2>File Sharing</h2>  
  
![image](https://github.com/user-attachments/assets/0558302f-27d3-41dd-a373-8611efae98f5)
<p>I create a new OU name Group within that I create accountants as group.</p>

![image](https://github.com/user-attachments/assets/6ecacc34-359b-4a39-9106-8be4d628ad91)
![image](https://github.com/user-attachments/assets/ddaa8198-51b2-442a-be66-e368f74a45aa)
![image](https://github.com/user-attachments/assets/1bba4e50-e8bc-4ee4-86f2-9298434c91a3)
<p>I create files to share in AD and set permission for certain individuals for no access, only read, and read and write.</p>


![image](https://github.com/user-attachments/assets/d0bd7c22-92c9-4747-ac10-50b63081f0e2)
![image](https://github.com/user-attachments/assets/a1126f25-6019-4f35-9b44-fe74a7151462)
<p>I login as one of my fake user to see if I can see the share folders and I am able to. The only folder I no access to is the accounting folder since the Accountants only have permission to read/write in that folder.</p>

![image](https://github.com/user-attachments/assets/27441854-07b9-4eb2-99bf-0fe89e8be74f)
<p> Now back in AD, I put my user in the accountants group to have access to the folder.</p>

![image](https://github.com/user-attachments/assets/66862282-f02c-4587-bc00-d1663422f565)
<p>Back in the VM, now I am able to open the folder.</p>
