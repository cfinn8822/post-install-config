# post-install-config
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>Post-Install Configuration Objectives</h2>

- Create and Configure Roles
- Create and Configure Departments & Teams
- Create and Configure Agents (worker) & Users (customers)
- Configure (SLA) Service Learning Agreements
- Configure Help Desk Topics

<h2>Configuration Steps</h2>

1)Prerequisites and Installation

 - This demonstration assumes a Virtual Machine is established with the prerequisite files installed for working OS Ticket.

 2)On the web browser,go to your Help Desk Login Page http://localhost/osTicket/scp/login.php. And sign into your help desk.

<img src="https://i.imgur.com/mZpjphU.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

 3)Once login you are on the Agent Panel.Click on the"Admin Panel"at the top-right of page.

 <img src="https://i.imgur.com/tyjoyW4.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

 4)Click on the"Agents"tab->"Roles"->"Add new role".

 
<img src="https://i.imgur.com/STO36vY.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

 - Roles are permissions granted to the Agents per Department that they have access to.
 *In the Definition tab, type any Role name of your choice (this example uses Supreme Admin).
 
  - Then click on the permissions tab.
 
<img src="https://i.imgur.com/EnHGkk9.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

5) This role will we be given all permissions.Check all boxes under Tickets,Tasks and Knowledgebase.

 - Once done,click Add Role.
 
<img src="https://i.imgur.com/QkVRhRX.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

- Now we've created a Supreme Admin role with all permissions granted. Next, we'll create a Department.

6)Still in the Agents tab, click on the Department category.

 - Click Add Department.


<img src="https://i.imgur.com/dCAnXPQ.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

7)Create a Department name of your choice( for this example i am using System Administrators ).Skip everything else for the time being.


<img src="https://i.imgur.com/DYLYvLB.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

8)Now we move on to making Teams."Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter."

- Still in the Agents tab, click on the "Teams" category.


<img src="https://i.imgur.com/YlqUi2d.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

9) Create a Team name of your choice( for this example i am using Level 2 Support)

 - Click create Team.

<img src="https://i.imgur.com/Ac0EbWS.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

10)Currently in the Agent tab,click"Agents" category.

<img src="https://i.imgur.com/LFCST9K.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

11)Create the required credentials for the workers.

 - First name(for this example jane)
 - Last name (for this example doe)
 - Email address(for this example jane.doe@osticket.com)
 - Username(for this example jane.doe)

12)Click "Set Password", and a window prompt will appear.

 - Uncheck "Send the agent a password reset email".
 - Create a password for this user.
 - Uncheck "Require password change at next login".
 - Click "Set".

<img src="https://i.imgur.com/0O5zPFg.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

13)Click on the"Access" tab

 - Assign this user the Department that we created (this example uses System Administrators).
 - Assign this user the Role that we created (this example uses Supreme Admin).
 - Under Extended Access, assign this user the "Support"
 - Assign this user the "Supreme Admin" role.
 - Click Create

 
<img src="https://i.imgur.com/3mQuPkF.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

14)Click on the"Teams" tab

 - Assign this user the Team that we created (this example uses Level II Support)
 - Once done, click "Create"


<img src="https://i.imgur.com/n6rY5X1.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

15)Create another Agent following the steps, however assign it to a different Role and Department.

 - This example creates Agent "John Doe" | Department: "Level I Support" | Role: "View only | Extended Access: Support".


<img src="https://i.imgur.com/gmWITrd.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

16)Agent Panel Creating Users

 - Click on "Agent Panel" on the top-right of the page.

<img src="https://i.imgur.com/ApLT5LP.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

 - Click on the "Users" tab.
 - Click on "Add User".
 - Create an Email Address and Full Name for this user( this example uses karen@osticket.com / Karen Karen ).
 - Click "Add User".

<img src="https://i.imgur.com/PtJfzjT.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/5ZXl6oc.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

17)Create another user of your choice (this example uses ken@osticket.com / Ken Ken)

<img src="https://i.imgur.com/pBotAdb.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

18)Admin Panel - Configuring SLA

 - "SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed."
 - Return to the "Admin Panel".
 - Navigate to "Manage" tab > "SLA".
 - Click "Add New SLA Plan".

<img src="https://i.imgur.com/yI2vENX.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

19)Create the following plans:

 - SEV-A
   - Grace Period: 1 hour (Amount, in hours, before tickets with this SLA will become overdue if not closed in allotted time.)
   - Schedule: 24/7 (Accounted for all days of the week, even on non-business days)

 - Sev-B
   - Grace Period: 4 hours
   - Schedule: 24/7
  
 - Sev-C
   - Grace Period: 8 hours
   - Schedule: Monday - Friday 8am - 5pm with U.S. Holidays
  
<img src="https://i.imgur.com/z3GT3tW.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/tvJT9Xm.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

20)Configure Help Topics
 - Help Topics will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket.
 - Currently in the Admin Pangel, navigate to "Manage" tab > "Help Topics".
 - Click "Add New Help Topic".

<img src="https://i.imgur.com/MjPsvvw.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
 
21)Create Help Topics with the following names:
 - Business Critical Outage
 - Personal Computer Issues
 - Equipment Request
 - Password Reset

- "Internal Notes" can be written down for personal use, but not necessary.
 - After that, click "Add Topic".

<img src="https://i.imgur.com/chmCHaA.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/aOkRyta.png.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

COMPLETE!!!



