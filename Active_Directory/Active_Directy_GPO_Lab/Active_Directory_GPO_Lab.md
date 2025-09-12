# Active Directory GPO Lab

## Overview  
In this lab, I practiced Group Policy Object (GPO) management within Active Directory.  
The tasks focused on restricting Control Panel access for users and configuring an auto-lock screen policy.  
This helped me understand how GPOs are created, edited, linked to Organizational Units (OUs), and tested using domain users.  

## Steps and Screenshots  

### Task 1: Restricting Control Panel Access  

- I created a new GPO named **Restrict Control Panel Access**. 

![Creating New GPO](./screenshots/Creating_New_GPO_Named_Restrict_Control_Panel_Access.PNG)  

- Edited the GPO to configure **Prohibit access to Control Panel and PC settings**. 

![Editing Restrict Control Panel Access](./screenshots/Editing_Restrict_Control_Panel_Access_GPO.PNG)  

- Verified the setting before applying – it was initially not configured.  

![Not Configured](./screenshots/Control_Panel_Window_Showing_Prohibit_Access_to_Control_Panel_Not_Configured.PNG)  

- Enabled the restriction policy.  

![Enabled Restriction](./screenshots/Prohibit_Access_to_Control_Panel_And_PC_Settings_Is_Enabled.PNG)  

- Linked the GPO to **Management, Marketing, and Sales OUs**. 

![Linked GPO](./screenshots/Restrict_Control_Panel_Access_GPO_Linked_To_Management_Marketing_And_Sales_OUs.PNG)  

### Task 2: Configuring Auto-Lock Screen Policy 

- Created a new GPO named **Auto Lock Screen**. 

![New Auto Lock Screen](./screenshots/Creating_New_GPO_Named_Auto_Lock_Screen.PNG)  

- Linked it to the **Root Domain**.  

![Linked Auto Lock](./screenshots/Auto_Lock_Screen_Linked_To_The_Root_Domain.PNG)  

- Configured the **Machine Inactivity Limit** to 300 seconds (5 minutes). 

![Set Inactivity Limit](./screenshots/Security_Options_Showing_Machine_Inactivity_Limit_Is_Set_To_300Seconds.PNG)  

### Task 3: Testing the Policies  

- Used the domain user **Mark** in the **Marketing OU** for testing.

![Marketing OU User](./screenshots/Marketing_OU_Showing_User_Mark.PNG)  

- Verified domain login via **RDP** using Mark’s credentials.  

![RDP Login](./screenshots/Sigining_In_To_Domain_Via_RDP_Using_Mark_Credentials.PNG)  

- Attempted to open Control Panel – restriction worked as expected. 

![Restriction Applied](./screenshots/Tried_Opening_Control_Panel_Restrictions_Error_Message_Received_Because_of_GPO.PNG)  

- Waited for 5 minutes – user session logged out automatically.  

![Auto Logout](./screenshots/Mark_Login_Screen_Verifying_It_Got_Logged_Out_After_5_Minutes.PNG)  

## Conclusion  

This lab demonstrated how to create and manage Group Policy Objects in Active Directory.  
I successfully implemented policies to restrict Control Panel access and enforce auto-lock after inactivity.  
By linking these policies to OUs and testing with a domain user, I gained hands-on experience in applying security and productivity-related policies within an AD environment.  
