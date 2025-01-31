<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles and Departments within osTicket
- Configure Teams and Agents
- Configure Users and Service Level Agreement
- Configure Help Topics

<h2>Configuration Steps</h2>
<h3>Configuring Roles and Departments</h3>
<p>
We will be beginning this portion of the lab by logging into the admin portal. By using this link: 'http://localhost/osTicket/scp/login.php' it will take you to the login for admin work. Once you are logged in you will be sent to the tickets section. Now this ticketing section is known as the 'agent portal', the 'admin panel' which is where we are going to be doing our configurations is a seperate section. If you click on the Admin Panel button, you will be redirected to a different page.

![image](https://github.com/user-attachments/assets/ab79fa8d-a49a-43db-a6a2-1eed2956253b)
![image](https://github.com/user-attachments/assets/4827eb1e-6654-404a-a9a4-f05be6ccbcdb)

Now, from the Admin Panel we will be going to Agents->Roles. This will show us all the roles, and what permissions these certain roles will have. Feel free to go through each role and see what permissions they have.

![image](https://github.com/user-attachments/assets/d99053d0-1296-4e9c-aef6-3fd1caf72956)

From here, we will be making our own role. Click on 'Add new role' and name it 'Supreme Admin'. We will be checking all the permissions in all 3 categories.
![image](https://github.com/user-attachments/assets/d868c0eb-561f-42e4-a00c-0f65616f0a4d)
![image](https://github.com/user-attachments/assets/de730057-961d-4823-8d8e-7010443be09a)
![image](https://github.com/user-attachments/assets/3e724d16-ae61-44d8-8464-7823ec4240b2)
![image](https://github.com/user-attachments/assets/b1e0910b-c6f3-4fb4-93bd-350cef3559f3)

Once that is done, go ahead and save any changes done. Now we will be configuring Departments. In order to get here we will go to Agents->Departments. You should initially only see 2 Departments made.

![image](https://github.com/user-attachments/assets/3893688b-39f4-499c-8534-181e9113cf10)

From the Departments section, we will be adding new departments. So, click on 'Add New Department' and name it 'System Administrators'. Make sure for the 'Parent:' section that it says 'Top Level Department'. We can leave any other settings set to their defaults.

![image](https://github.com/user-attachments/assets/1b70f330-887a-412f-a284-bf8e42f900f4)

Press Create Department, and we have successfully configured Roles and Departments within osTicket.
</p>

<h3>Configuring Teams and Agents</h3>

<p>
Now, we will be making our way to the Teams portion. In order to get there we will click on Agents->Teams. You should see one team already premade: 'Level 1 Support'. We are going to create a new team, named 'Online Banking'. From the teams page, click on 'Add New Team', and enter the name of the team. Once the name is entered, we will simply press 'Create Team'. 

![image](https://github.com/user-attachments/assets/310affa4-3a36-40a6-8375-70a0a80a83d2)
![image](https://github.com/user-attachments/assets/20cf712d-07b5-4211-a089-8c3be0c1d47d)

Our next step, will be to allow end users to create tickets without needing an account. In order to set this up we will navigate to the settings menu within our Admin Panel. We will go to: Settings->Users. On this page we will look for: 'Registration Required'. The setting should be under the category 'Authentication Settings'. Make sure that the box in this area is unchecked. If it is not, please uncheck it and save changes.

![image](https://github.com/user-attachments/assets/736ad038-05eb-45ee-9658-e65b517019d1)

We will now, go ahead and add agents to our helpdesk. Go ahead and click on 'Agents' within the Admin Portal. You should be redirected to a screen with only the default agent made. 

![image](https://github.com/user-attachments/assets/fb8a1201-b57e-4aec-9cd4-8a0b40d34e67)

From this page, click on 'Add New Agent'; now make sure to give the agent a name, email, and Username.

![image](https://github.com/user-attachments/assets/9cc49811-6294-4f9a-b0e5-186a1e88fa95)

Now we will make our way to the 'Access" tab. From here we will add the user to the 'System Administrators' Department and also giving them the 'Supreme Admin' role. Then Navigate to the Teams tab, and add the agent to the 'Online Banking' team. Once everything is set, go ahead and create the user. 

![image](https://github.com/user-attachments/assets/4b0ec11a-d3e6-49a5-ae58-1f0a8a7437ea)
![image](https://github.com/user-attachments/assets/4addab05-cf30-428e-be3e-38373187d5e7)

If we go back to the 'Agents' tab, we will see the new agent we have created. Now we will be repeating the process, and create another agent. Make sure to add this second agent to the 'support' department, and only give the agent 'view only' role. Now we should have 3 users within the Agents tab.

![image](https://github.com/user-attachments/assets/bb331848-f987-427d-866c-2ef222eca19a)
![image](https://github.com/user-attachments/assets/f13ed653-a896-49fe-bc1b-1f382d2c563f)

We will go through, and give both the agents a password. Click on the agents name, and then click on 'set password'. Make sure to uncheck 'Send the agent a password reset email', and from here we will set the passwords for the agent. We will also uncheck the box: 'Require password change at next login'. Click 'update' once the passwords are set. Make sure to repeat this for both agents. 

![image](https://github.com/user-attachments/assets/34fa6f40-4ad4-465f-8ee0-7901cc1dd802)

We have successfuly added and configured both teams and agents. Now we will be moving on to the next step.
</p>
<br />

<h3>Configuring Users and SLA (Service Level Agreement)</h3>

<p>
To begin this portion of the lab, we will be going back to the 'Agent Panel'. Once we are at the panel, we will be going to the 'Users' tab and then we will be adding users.

![image](https://github.com/user-attachments/assets/6126b148-c6a6-4349-acf5-df23d48b170e)

Go ahead and click on 'add user' and we will fill in the information needed to create our user. Fill in the Name and email portion of the 'create new user' section. Once the user is created, you will be redirected to the user profile.

![image](https://github.com/user-attachments/assets/4db572ad-f4d9-4fb0-98bd-2eff06b46fb3)

We are now going to be configuring the SLA, in order to do this we need to go back to the 'Admin Panel'. Once you are in the Admin Panel, we will be navigating to: Manage->SLA.

![image](https://github.com/user-attachments/assets/cf131dff-68f8-4304-9af8-e0f780a827b6)

On this page we will have the default SLA, we will now be creating 3 new SLA's on the basis of severity. We will be naming them, 'Sev-A, Sev-B, Sev-C'. Sev-A being the most important, and Sev-C being the least. Click on 'Add New SLA Plan' and from here we will create the following SLAs.

Sev-A

![image](https://github.com/user-attachments/assets/31500ac0-27ea-46cb-9932-88a74aa231ff)

Sev-B

![image](https://github.com/user-attachments/assets/1db7d528-06ae-4943-8ee2-234995c9509d)

Sev-C

![image](https://github.com/user-attachments/assets/38a53a79-e64a-4df5-b3c2-a629ab09adc9)

Once you have made all 3 SLAs they should be displayed in the SLA section.

![image](https://github.com/user-attachments/assets/04a465ee-430f-43e7-9462-c8a1acdb9071)

We will now be going to the next portion of the lab, congratulations we have successfully Configured Users and SLA.
</p>

<h3>Configuring Help Topics</h3>

<p>
From the Admin Panel, we will go to Manage->Help Topics. 

![image](https://github.com/user-attachments/assets/297598b7-64af-4768-b747-0d785dbf9f57)

Once you are here, click on 'Add New Help Topic'. We will be creating the following Help Topics: 'Business Critical Outage, Personal Computer Issues, Equipment Request, Password Reset, and Other'. Make sure to also include each topic with its respective Parent Topic. Once all topics have been added, the 'Help Topics' page should look like the following image.

![image](https://github.com/user-attachments/assets/5781cb52-1e2d-40ef-a12f-f7726f889042)

This concludes our second portion of the lab, we have configured osTicket post installation for our needs and any common issues that may arise within helpdesk.

</p>
<br />
