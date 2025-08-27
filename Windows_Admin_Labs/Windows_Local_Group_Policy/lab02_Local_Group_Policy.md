# 🧪 Windows Administration Lab: Local Group Policy for Security

## Overview
This lab demonstrates how to **secure a Windows 10 endpoint using Local Group Policy** by enforcing password complexity requirements and disabling USB storage devices. These are essential steps in hardening a system to prevent weak credentials and unauthorized data access.

---

## Steps and Screenshots

### Step 1: Access the Local Group Policy Editor
1. Press `Win + R`, type `gpedit.msc`, and press **Enter**.  
2. This opens the **Local Group Policy Editor** where security settings can be managed.

---

### Step 2: Enforce Password Complexity
1. Navigate to:  
Computer Configuration → Windows Settings → Security Settings → Account Policies → Password Policy

2. Enable **Password must meet complexity requirements**.  
3. Set **Minimum Password Length** to **8 characters**.  
4. Apply changes.

**Screenshots:**  
![Password Complexity Enabled](../screenshots/Password_Complexity_Requirements_Enabled.PNG)  
![Minimum Password Length](../screenshots/Minimum_Password_Length_8_Characters.PNG)  
![Password Policy Confirmation](../screenshots/Password_Policy_Window_Confirming_Changes.PNG)

---

### Step 3: Disable USB Storage Devices
1. Navigate to:  
Computer Configuration → Administrative Templates → System → Removable Storage Access

2. Enable **All Removable Storage classes: Deny all access**.  
3. Apply changes.

**Screenshots:**  
![USB Storage Denied Policy](../screenshots/All_Removable_Storage_Classes_Enabled.PNG)  
![USB Policy Confirmation](../screenshots/Policy_Window_Confirming_USB_Storage_Denied.PNG)

---

### Step 4: Verify the Policy
1. Run the following in **Command Prompt** to apply policies immediately:  
gpupdate /force

2. Test **password policy**: Try setting a weak password → it should fail.  
3. Test **USB policy**: Insert a USB drive → access should be denied.

**Screenshots:**  
![Policy Updated](../screenshots/Policy_Updated_Successfully.PNG)  
![Password Failed](../screenshots/Password_Failed_Because_Of_Complexity_Policy.PNG)  
![USB Access Denied](../screenshots/USB_Access_Denied.PNG)

---

## Conclusion
This lab successfully demonstrated how to:  
- Enforce **password complexity** and minimum length requirements for stronger authentication.  
- Disable **USB storage devices** to prevent unauthorized data access.  
- Verify applied policies to ensure endpoint security hardening is effective.  

Configuring **local security policies** is a critical skill for Help Desk and Junior SysAdmin roles.

