# Lab 01 – Local User Account Management in Windows 10

## Overview
This lab demonstrates how to perform common user account management tasks in Windows 10:
- Create and delete local user accounts
- Reset user passwords
- Add users to local groups
- Verify changes using Command Prompt

These are typical real-world tasks performed by Help Desk and Junior System Administrators.

---

## Steps & Screenshots

### 1. Create a New Local User Account
- Open **Local Users and Groups (lusrmgr.msc)** → **Users → New User…**  
- Created user: **RanaW**  
- Assigned initial password.  
 
![New User Account](./screenshots/New_User_Account_Setup.PNG)  
![RanaW Account Created](./screenshots/RanaW_Account_Created.PNG)  

---

### 2. Add User to Local Group
- Open **RanaW Properties → Member Of tab**.  
- Added user to **Remote Desktop Users** group.  
 
![Added To Group](./screenshots/RanaW_Added_To_Local_Group.PNG)  
![Group Membership](./screenshots/RanaW_Group_Membership.PNG)  

---

### 3. Reset a User Password
- Right-clicked user **StephM** → **Set Password** → entered new password.  
 
![Password Reset Confirmation](./screenshots/StephM_Password_Reset_Confirmation.PNG)  

---

### 4. Delete an Old User Account
- Right-clicked **OG** account → **Delete** → Confirmed deletion.  
 
![User Deletion Confirmation](./screenshots/Confirmation_Of_User_Deletion.PNG)  

---

### 5. Verify Using Command Prompt
- Ran `net user` before and after deletion to verify user list.  

![Users List Before](./screenshots/Users_List.PNG)  
![Updated Users List](./screenshots/Updated_Users_List.PNG)  

---

## Conclusion
This lab successfully demonstrated how to:  
✔ Create a new user account  
✔ Reset a user password  
✔ Add a user to local groups  
✔ Delete an obsolete account  
✔ Verify changes with Command Prompt  

These are essential skills for IT Support/Help Desk technicians to manage local accounts in a Windows environment.
