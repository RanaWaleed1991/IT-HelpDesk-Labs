# 🧪 Windows Administration Lab: Local Group Policy for Security

## Overview
This lab demonstrates how to **secure a Windows 10 endpoint using Local Group Policy** by enforcing password complexity requirements and disabling USB storage devices. These are essential steps in hardening a system to prevent weak credentials and unauthorized data access.

---

## Steps and Screenshots

### Step 1: Access the Local Group Policy Editor
1. Open **Local Group Policy Editor (*gpedit.msc*)**
2. This will be used to manage security settings.

---

### Step 2: Enforce Password Complexity

1. Navigate to:  
**Computer Configuration → Windows Settings → Security Settings → Account Policies → Password Policy**

2. Enable **Password must meet complexity requirements**.  

![Password Complexity Enabled](./screenshots/Password_Complexity_Requirements_Enabled.PNG)  

3. I have set **Minimum Password Length** to **8 characters**.  

![Minimum Password Length](./screenshots/Minimum_Password_Length_8_Characters.PNG) 

4. Password Policy changed.

![Password Policy Confirmation](./screenshots/Password_Policy_Window_Confirming_Changes.PNG)

---

### Step 3: Disable USB Storage Devices

1. Navigate to:  
**Computer Configuration → Administrative Templates → System → Removable Storage Access**

2. External storage policy is implemented by enabling **All Removable Storage classes: Deny all access**.  

![USB Storage Denied Policy](./screenshots/All_Removable_Storage_Classes_Enabled.PNG)

3. Policy window confirming that the policy has been configured .

![USB Policy Confirmation](./screenshots/Policy_Window_Confirming_USB_Storage_Denied.PNG)

---

### Step 4: Verify the Policy

1. Policies are applied immediately by running **gpupdate/force** in **Command Prompt**

![Policy Updated](./screenshots/Policy_Updated_Successfully.PNG) 

2. I tested **Password policy** by setting a weak password and it failed. 

![Password Failed](./screenshots/Password_Failed_Because_Of_Complexity_Policy.PNG) 

3. Lastly, I tested **Removable Storage Policy** by plugging a USB drive. Access was denied.

![USB Access Denied](./screenshots/USB_Access_Denied.PNG)

---

## Conclusion
This lab successfully demonstrated **Windows Group Policy Implementation**. I:

- Enforced **Password Complexity** and minimum length requirements for stronger authentication.  
- Disabled **USB storage devices** to prevent unauthorized data access.  
- Verified applied policies to ensure endpoint security hardening is effective.  
