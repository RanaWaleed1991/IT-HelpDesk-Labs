# Active Directory Lab Documentation - Part 1

## Overview
In this lab, I demonstrate my ability to set up and configure Windows Server 2022 in a VMware environment.  
The initial steps involve preparing the virtual machine, installing the operating system, and getting the server ready for Active Directory Domain Services.  
This documentation is structured to help recruiters, hiring managers, and technical reviewers clearly see my process and technical skills.

## Steps and Screenshots

### Step 1: Creating the Virtual Machine
I began by creating a new virtual machine in VMware Pro and selecting the Windows Server 2022 ISO for installation.  
![Step1](/screenshots/New_Virtual_Machine_Wizard_Server_EVAL_iso_Selected.PNG)

### Step 2: Configuring Virtual Machine Settings
Before installation, I ensured the virtual machine was configured with sufficient resources (CPU, RAM, and storage).  
![Step2](/screenshots/Virtual_Machine_Settings_Window.PNG)

### Step 3: Starting the Windows Server Installation
With the VM prepared, I initiated the Windows Server setup by selecting the 'Install Now' option.  
![Step3](/screenshots/Microsoft_Operating_System_Setup_Install_Now.PNG)

### Step 4: Selecting the Edition
I chose the **Standard Evaluation with Desktop Experience** to provide a familiar GUI interface.  
![Step4](/screenshots/Standard_Evaluation_Operating_System_Desktop_Experience_Selected.PNG)

### Step 5: Installation Progress
The operating system installation was carried out successfully as shown below.  
![Step5](/screenshots/Installing_Microsoft_Server_Operating_System_Page.png)

### Step 6: First Login as Administrator
Once the OS was installed, I logged in as the default Administrator to start post-installation tasks.  
![Step6](/screenshots/Administrator_Login_Page_After_Installation.PNG)

### Step 7: Server Manager Dashboard
After login, the Server Manager automatically launched, providing a central interface to manage roles and features.  
![Step7](/screenshots/Server_Manager_Dashboard.png)

### Step 8: Renaming the Server
To follow best practices, I renamed the server to **Rana-DC01**, which represents my lab’s Domain Controller.  
![Step8](/screenshots/VM_Renamed_To_Rana-DC01_From_Server_Manager.PNG)

### Step 9: Configuring DNS
I configured the server’s IP address to also act as its DNS, which is essential for Active Directory environments.  
![Step9](/screenshots/IP_Address_Of_The_Server_is_Used_To_Set_The_DNS_Address.PNG)

### Step 10: Starting Role-Based Installation
Next, I initiated the **Role-based or feature-based installation** process to prepare for AD DS.  
![Step10](/screenshots/Adding_Roles_And_Features_By_Selecting_Roles_Based_Installation.PNG)

### Step 11: Selecting the Target Server
From the server pool, I selected **Rana-DC01** to install the roles.  
![Step11](/screenshots/For_Server_Selection_Rana-DC01_Is_Selected.PNG)

## Conclusion
At this stage, the server has been set up and prepared for Active Directory installation.  
This demonstrates my ability to configure a base Windows Server 2022 environment, a skill directly applicable in enterprise IT environments.
