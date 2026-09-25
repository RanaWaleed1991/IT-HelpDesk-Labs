# IT Help Desk Portfolio

Hi, I'm Rana. I have a Master's in Information Technology and I'm working my way back into IT, aiming for a help desk or IT support role. I don't have recent on-the-job experience yet, so I built this portfolio to show how I actually work: 13 hands-on labs covering Windows, Microsoft 365, Entra ID, Active Directory and service desk tools.

Every lab is written up like a real support ticket. There's a user with a problem, the steps I took to find the cause, the fix, and proof that it worked. Each step has a screenshot from when I did it.

---

## If You Only Have Five Minutes

These four labs give the best picture of how I approach a ticket:

| Lab | What it shows |
|---|---|
| [User Locked Out: MFA Recovery with a Temporary Access Pass](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Microsoft_365_Labs/MFA_TAP_Conditional_Access/MFA_TAP_Conditional_Access.md) | Getting a locked-out user back in after a phone change without resetting their password, then planning a move from Security Defaults to Conditional Access. |
| [INC0010001: VPN Drops After 5 Seconds](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Help_Desk_Operations/ServiceNow_Ticket_Workflow/ServiceNow_Ticket_Workflow_Lab.md) | One ServiceNow incident from start to finish: triage, correcting the priority, internal notes vs customer updates, escalating to Tier 2, and resolving once the user confirms. |
| [No Internet Access: DNS or Default Gateway?](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Core_OS_Skills/Basic_Network_Troubleshooting/lab01_Network_Troubleshooting.md) | Two faults that look the same to a user. I use ping, nslookup and tracert to prove which one is broken before changing anything. |
| [Slow Startup: Boot Time Cut by 48%](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Core_OS_Skills/PC_Performance_Troubleshooting_LocalHost/lab02_PC_Performance_Troubleshooting.md) | Done on a real laptop. Boot time went from 178 to 93 seconds and idle disk use from 65% to 3%, measured before and after with Event Viewer. |

---

## All Labs

### Microsoft 365 and Entra ID
- [New Hire Provisioning: Entra ID Onboarding with RBAC and SSPR](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Microsoft_365_Labs/Entra_ID_User_Lifecycle_%26_RBAC/Entra_ID_User_Lifecycle_RBAC.md)
- [User Locked Out: MFA Recovery, Temporary Access Pass and Conditional Access](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Microsoft_365_Labs/MFA_TAP_Conditional_Access/MFA_TAP_Conditional_Access.md)
- [Sales New Starter: Microsoft 365 Account, MFA, Teams and Mailbox Check](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Microsoft_365_Labs/User_Account_Creation_and_Management_in_Microsoft_365/M365_User_Creation_and_Verification.md)
- [Outlook Not Set Up: Microsoft 365 Apps and a Mail Flow Test](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Microsoft_365_Labs/Microsoft_365_Email_Setup/Microsoft_365_Email_Setup.md)

### Help Desk Operations
- [INC0010001: VPN Drops After 5 Seconds, Full Incident Lifecycle in ServiceNow](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Help_Desk_Operations/ServiceNow_Ticket_Workflow/ServiceNow_Ticket_Workflow_Lab.md)
- [My Documents Won't Print: Remote Fix with Quick Assist](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Help_Desk_Operations/Remote_Support_Tool/Quick_Assist_Printer_Lab.md)

### Active Directory
- [New Domain Build, Part 1: Building and Preparing the Domain Controller](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Active_Directory/AD%20Installation%20and%20Functionality/Lab_Documentation_Part1.md)
- [New Domain Build, Part 2: AD DS, First User, Security Group and a Read-Only File Share](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Active_Directory/AD%20Installation%20and%20Functionality/Lab_Documentation_Part2.md)
- [Staff Changing System Settings: Control Panel Restriction and Screen Lock GPOs](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Active_Directory/Active_Directy_GPO_Lab/Active_Directory_GPO_Lab.md)

### Windows Troubleshooting
- [No Internet Access: DNS vs Default Gateway Failures](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Core_OS_Skills/Basic_Network_Troubleshooting/lab01_Network_Troubleshooting.md)
- [Slow Startup: Cutting Boot Time 48% by Removing Startup Programs](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Core_OS_Skills/PC_Performance_Troubleshooting_LocalHost/lab02_PC_Performance_Troubleshooting.md)
- [Print Jobs Stuck in the Queue: Event Logs and Print Spooler Recovery](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Core_OS_Skills/Printer_Troubleshooting/lab03_Printer_Troubleshooting.md)

### Windows Administration
- [New Starter Workstation: Windows 11 Pro Build, Updates and a Standard User Account](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Core_OS_Skills/Windows11_Installation/Windows11_Installation_Lab.md)
- [Joiner, Leaver and Password Reset: Local Account Administration](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Windows_Admin_Labs/User_Account_Management/lab01_User_Account_Management.md)
- [Endpoint Hardening: Password Complexity and USB Storage Blocking](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Windows_Admin_Labs/Windows_Local_Group_Policy/lab02_Local_Group_Policy.md)
- [Deleted Project File: File History Backup and Restore](https://github.com/RanaWaleed1991/IT-HelpDesk-Labs/blob/main/Windows_Admin_Labs/File_Recovery_And_Backup/lab03_Backup_Recovery_Using_File_History.md)

---

## Skills

- **Operating systems:** Windows 10, Windows 11, Windows Server 2022
- **Identity and access:** Active Directory, Entra ID, Microsoft 365 admin, local accounts, RBAC, least privilege, SSPR, MFA, Temporary Access Pass, Conditional Access
- **Troubleshooting:** networking (DNS, gateway, ping, tracert, nslookup), slow PCs, printers and the print spooler, Event Viewer
- **Administration:** Group Policy (domain and local), security groups, NTFS permissions, file shares, File History backups, Windows Update
- **Service desk:** ServiceNow incident management, ticket triage and escalation, Quick Assist remote support, writing clear updates for users

---

## How I Write Each Lab

I try to document a lab the way I'd want a ticket handed over to me:

1. **The ticket:** who reported what, how urgent it is, and the exact environment.
2. **The problem:** what's wrong and what "fixed" means for the user.
3. **The steps:** what I checked, what I found and what I changed, with a screenshot for each step.
4. **The proof:** a summary of the evidence that the problem is actually solved.
5. **What I learned:** the reasoning behind the steps, and what I'd do differently in a real company.

## About the Lab Environments

I did these labs in my own home lab (VMware virtual machines, Microsoft 365 trial tenants and a ServiceNow developer instance). The Group Policy lab used TryHackMe's Active Directory environment. The tickets are realistic scenarios built around that hands-on work. Where I broke something on purpose to recreate a problem, the lab says so. The slow startup lab was done on my own laptop.

---

## What I'm Looking For

I'm looking for an IT Help Desk or IT Support role where I can help people with their problems, keep learning, and grow into more advanced systems work. If you think I'd be a good fit for your team, I'd love to hear from you.

## Contact

- **Email:** ranawaleedbinzia@gmail.com
- **GitHub:** [RanaWaleed1991](https://github.com/RanaWaleed1991)
