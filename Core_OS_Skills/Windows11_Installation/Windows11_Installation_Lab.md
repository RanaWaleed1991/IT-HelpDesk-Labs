# Windows 11 Installation & Configuration Lab

## Overview
This lab demonstrates a clean installation and configuration of Windows 11 in a VMware Workstation Pro environment. 
It reflects a real-world IT Service Desk scenario where a new user device is provisioned, updated, and configured with 
the necessary drivers and user accounts.

## Steps and Screenshots

### 1. Creating a New Virtual Machine

I began by creating a new VM in VMware Workstation Pro and selected the Windows 11 ISO image.

![VMware New VM Wizard ISO Selected](./screenshots/VMware_New_VM_Wizard_ISO_Selected.png)

### 2. Starting Windows Setup

When the VM booted, I proceeded with the installation and selected the language and regional preferences.  

![Windows Setup Language](./screenshots/Windows_Setup_Language.png)

### 3. Choosing Installation Option

I chose to install Windows 11 as a new installation.  

![Windows Setup Option Install Windows 11](./screenshots/Windows_Setup_Option_Install_Windows11.png)

### 4. Selecting Windows 11 Edition

I selected **Windows 11 Pro** from the available images to match enterprise environments.  

![Windows Setup Image Selection Windows 11 Pro](./screenshots/Windows_Setup_Image_Selection_Windows11_Pro.png)

### 5. Installation in Progress

The setup began installing Windows 11 files and features.  

![Installing Windows 11 Screen](./screenshots/Installing_Windows11_Screen.png)

### 6. Naming the Device

After installation, I named the device. The device name can later be changed to simulate a corporate naming convention.

![Windows11 VM Is Given Name To The Device](./screenshots/Windows11-VM_Is_Given_Name_To_The_Device.png)

### 7. Windows Updates

I launched **Windows Update** and allowed the system to download the latest patches. 

![Windows Update In Progress](./screenshots/Windows_Update_In_Progress_Window.png)  

![Windows Update Completed Restart In Progress](./screenshots/Windows_Update_Completed_Restart_In_Progress_Window.png)

### 8. User Account Setup

I created a local user account and configured login with a PIN.  

![User Account Created Login Page Pin Required](./screenshots/User_Account_Created_Login_Page.png)

### 9. First Login to Windows 11

The system loaded to the Windows 11 desktop after initial configuration.  

![Windows 11 Desktop](./screenshots/Windows11_Desktop.png)

### 10. Post-Installation Updates

I checked for updates again to ensure the system was up-to-date.  

![Check for Windows Update](./screenshots/Check_for_Windows_Update.png)  

![Windows Are Up to Date](./screenshots/Windows_Are_Upto_Date.png)

### 11. Creating an Additional Standard User

To follow security best practices, I added another standard user account in addition to the administrator.

![Another User Account Created](./screenshots/Another_User_Account_Created_In_Addition_To_Admin.png)

## Conclusion


This lab successfully demonstrates the end-to-end process of deploying a new Windows 11 workstation: 
- Performing a clean installation
- Applying updates
- Configuring user accounts
- Ensuring the system is ready for use in a professional environment. 

This mirrors real-world IT administration tasks when preparing machines for end-users.
