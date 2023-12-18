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

- Configure Roles
- Configure Departments
- Configure Teams
- Allow anyone to create a ticket
- Configure Agents
- Configure Users
- Configure SLA
- Configure Helper Topic

<h2>Configuration Steps</h2>

<h4> 1. Configure Roles </h4>

- Roles are permissions granted to Agents per Department that they have access to. Each Role has a set of permissions that can be checked/unchecked for agents given that Role in association with a Department they have access to. An unlimited number of roles can be created and assigned to Agents with access to various departments.

<h4> </h4>

- Login to osTicket with the Admin user credentials.

![image](https://github.com/oraljr/post-install-config/assets/152557529/322aa1cf-5013-476c-a398-94939365e13b)

- Click on Admin Panel (Note: The Agent Panel option becomes available in the upper right hand corner where Admin is located and the two become interchangeable).
    - Select Agents -> Roles.
    - Click "Add New Role".
          
![image](https://github.com/oraljr/post-install-config/assets/152557529/09e857a0-b2e0-42db-8d47-39c2404b8e47)

- Create a Supreme Admin Role.  

SUPREME ADMIN PHOTO

- Click on the Permissions tab and enable all Permissions for Tickets, Tasks and Knowledgebase, once complete select Add Role.
  
SS: Permissions for Tickets, Tasks and Knowledgebase,

<h4>2. Configure Departments</h4>

- In the Admin Panel, Select Agents -> Departments.
  - Create new Department.  

SS DEPT ADD NEW DEPT

  - Create System Administrator Department.
        
      <img width="50%" hieght ="50%"  align = "top" alt="Sys Admin Dpt created" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/a5b8865a-73c8-4559-ae91-5a88973e7b26">


----------------------------------------------------------------------------------------------------------------------------------------

<h4>3. Configure Teams</h4>
   
- In the Admin Panel, select Agents -> Teams.
    - Create New Teams.

        <img width="50%" hieght ="50%" alt="Add Teams" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/9bc80ffd-45a4-44a3-837b-220c97883f09">
        
    - Create Team called Level II Support.
      
       <img width="50%" hieght ="50%" alt="Level II Support creation Plus add member" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/c5232f89-6b79-4c05-b322-e6d01b0e4ec4">

    - Add a member to that team by selecting the member tab, and selecting an agent.

        <img width="50%" hieght ="50%" alt="add member to teams" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/2056fc9d-7f2e-403c-a0e0-2b0e37903ab0">

----------------------------------------------------------------------------------------------------------------------------------------------

<h4> 4. Make Sure That Anyone Can Register </h4>

   - In the Admin Panel.
   - In Settings -> Users -> User Settings.
       - Verify that in the registration required section, the box is NOT checked.
          
          <img width="50%" hieght ="50%" alt="Make sure anyone can register" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/6d4923bc-c83a-4eac-925c-45b5c01b725f">


---------------------------------------------------------------------------------------------------------------------------------------------------

<h4>5. Configure Agents </h4>

   - In Admin Panel, select the Agents -> Agents.
   - Select Add New Agent, give your agent a name and an email address.
   - Select set password.

      <img width="50%" hieght ="50%" alt="Set Password for New Agent" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/8881d1be-c444-4e67-9e9d-a42279c3dbc6">


   - Type in a password that you can remember, and click Set.
     
      <img width="50%" hieght ="50%" alt="New Agent 2" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/e9e43040-bff3-4a7e-9bfa-790a2b685ced">
      
   - Select the Access tab, assign your new agent to the System Administrator Department, and give them full access. Give this Agent extended access to the Support department. Once completed select Create.
  
     <img width="50%" hieght ="50%" alt="new agent 3" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/4db08ac2-d5b8-4135-823d-ff7ff504d807">
  
     
 -------------------------------------------------------------------------------------------------------------------------------------------------------------------

<h4>6. Configure Users</h4> 

- Navigate to the Agents Panel.

  <img width="50%" hieght ="50%" alt="Create User" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/31bbe2e8-328b-43c0-90f0-e9d5ae1a4efa">

    - Select Users, then User Directory.
    - Select Create a New User.
   
      <img width="50%" hieght ="50%" alt="new user 2" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/97c62ce5-0159-493c-bc01-49119924f43d">
   
    - Create an email address for the user and their full name.
    - Select "Add User".
      
        <img width="50%" hieght ="50%" alt="new user 3" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/4bd907d7-8851-401e-95db-9cec4176f8d3">

      ---------------------------------------------------------------------------------------------------------------------------------------------------

<h4>7. Configure SLA (Service Level Agreements) </h4>

- Navigate to the Admin Panel.
- Select the Manage tab then SLA.
- Select "Add New SLA"

    <img width="50%" hieght ="50%" alt="Add SLA" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/62a2e423-4e16-49bb-8982-f93a0b3386b8">
    
- In this example, we are going to create an SLA titled SEV-A with a Grace period of 1 hour on a 24/7 schedule
     
    <img width="50%" hieght ="50%" alt="add sla 2" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/6c95474c-77e2-47d4-8b74-c844b3b0019a">

- You can create more SLA's in the form of the following grace periods and schedules.
  -  Sev-B (4 hours, 24/7).
  -  Sev-C (8 hours, Business Hours).
          
   ----------------------------------------------------------------------------------------------------------------------------------------------------------

<h4> 8. Configure Help Topics </h4>

- Navigate to the Admin Panel, select the Manage tab, then Help Topics.
- Select "Add New Help Topic".

    <img width="50%" hieght ="50%" alt="Add Help Topics" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/b4d0dd33-e444-4f71-a85e-0b0105e614c5">

- Add a Help Topic titled Business Critical Outage, select Add Topic when completed.

    <img width="50%" hieght ="50%" alt="add help topics 2" src="https://github.com/s-evelyn/osTicket-PostInstallConfig/assets/53543374/65eb8b98-d8bd-4b36-a5c9-b691267ef5d2">

- Continue to add the following Help Topics:
    - Personal Computer Issues
    - Equipment Request
    - Password Reset

</p>

<br />

-----------------------------------------------------------------------------------------------------------------------------------------------
