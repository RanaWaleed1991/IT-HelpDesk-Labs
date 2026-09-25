# How I Built My Lab Environment

This page explains what I ran these labs on. Everything below comes from what is visible in the lab screenshots, so you can check it against them. At the end there's a short list of what you'd need if you want to build something similar yourself.

**[Back to the portfolio](README.md)**

---

## The Big Picture

My lab has four parts:

1. **Virtual machines on my own PC**, run in VMware Workstation Pro 17
2. **Two Microsoft 365 tenants** for the cloud and identity labs
3. **A ServiceNow developer instance** for the ticketing lab
4. **TryHackMe's Active Directory environment** for the Group Policy lab

One lab (slow startup) was done on a real laptop instead of a VM.

```
 My Windows PC
 │
 ├── VMware Workstation Pro 17
 │     ├── Rana.Windows10          Windows 10 "end user" PC      (DESKTOP-9OPLHE7)
 │     ├── Rana.Windows11          Windows 11 Pro workstation    (Windows11-VM)
 │     └── Rana.Windows_Server_2022   Domain controller          (RANA-DC01, lab.local)
 │
 └── Web browser
       ├── Microsoft 365 tenant: VirtualLabs1991.onmicrosoft.com   (Business Standard trial)
       ├── Microsoft 365 tenant: ResolvePointIT.onmicrosoft.com    (Business Premium)
       ├── ServiceNow Personal Developer Instance
       └── TryHackMe "Active Directory Basics" (domain thm.local)

 Separate physical laptop     →  slow startup lab
```

---

## 1. Virtual Machines (VMware Workstation Pro 17)

### Windows 10 VM: the "user's PC"

This is the machine I used most. It plays the part of an ordinary user's computer.

| Detail | Value |
|---|---|
| VM name | Rana.Windows10 |
| Computer name | DESKTOP-9OPLHE7 |
| Windows version | Windows 10, build 19045.6093 |
| Network adapter | Intel 82574L (Ethernet0) |
| IP address | 192.168.40.134, from DHCP server 192.168.40.254 |
| Default gateway | 192.168.40.2 |
| Local account | USER |
| Extra disk | A second virtual disk, about 10 GB, formatted as **BackupDisk (E:)** for the File History lab |
| Extra software | Microsoft 365 apps (Outlook, Word, Excel and others), PDF Architect 9, PDFCreator |

**Used in:** Network Troubleshooting, Printer Troubleshooting, Local Account Management, Local Group Policy, File History, Microsoft 365 Email Setup, Microsoft 365 User Creation (the admin work was done in this VM's browser; the checks signed in as Test User were done in a browser on my PC), and as the user's side of the Quick Assist lab.

### Windows 11 VM: the new workstation

| Detail | Value |
|---|---|
| VM name | Rana.Windows11 |
| Install media | Win11_24H2_English_x64.iso |
| Edition | Windows 11 Pro |
| Device name | Windows11-VM |
| Accounts | My Microsoft account as the main account, plus a local standard account called **Test User** |

**Used in:** Windows 11 Installation, and as the technician's PC in the Quick Assist lab.

### Windows Server 2022 VM: the domain controller

| Detail | Value |
|---|---|
| VM name | Rana.Windows_Server_2022 |
| Edition | Windows Server 2022 Standard Evaluation (Desktop Experience), build 20348 |
| Hardware | 2 CPU cores, 2048 MB RAM, 60 GB disk |
| Network | VMware NAT adapter |
| Server name | RANA-DC01 |
| IP address | 192.168.239.129 (static), gateway 192.168.239.2 |
| DNS | 192.168.239.129 (itself), with 8.8.8.8 as the alternate |
| Domain | lab.local (NetBIOS name LAB) |
| Roles | Active Directory Domain Services, DNS, File and Storage Services |

**Used in:** New Domain Build, Parts 1 and 2.

**Worth knowing:** the screenshots show the Windows 10 VM on the 192.168.40.x network and the server on 192.168.239.x. No lab in this repo joins a client PC to lab.local. The file share was checked from the server itself. Joining a client and testing as a domain user is the next step I've listed in that lab.

The Windows 10 VM was not activated (the "Activate Windows" watermark is visible in its screenshots), and the server runs on an evaluation licence ("Windows License valid for 175 days" on its desktop). Neither affects anything these labs do.

---

## 2. Microsoft 365 Tenants

I used two separate tenants.

### VirtualLabs1991.onmicrosoft.com

| Detail | Value |
|---|---|
| Subscription | Microsoft 365 Business Standard (trial) |
| Admin account | RanaWaleedZia@VirtualLabs1991.onmicrosoft.com |
| Managed from | A browser inside the Windows 10 VM |
| Test account | Test User (Test_User@VirtualLabs1991.onmicrosoft.com) |

**Used in:** Microsoft 365 Email Setup, and Microsoft 365 User Creation (MFA, Teams, admin roles).

### ResolvePointIT.onmicrosoft.com ("ResolvePoint IT")

| Detail | Value |
|---|---|
| Subscription | Microsoft 365 Business Premium, 25 licences |
| Tenant location | Australia |
| Admin account | Rana Waleed Bin Zia |
| Managed from | A web browser on my PC, with a private window to sign in as the test user |
| Test accounts | James Whitfield (Marketing Coordinator) and Ronaldo |

Business Premium includes **Microsoft Entra ID P1**, which is what allows Conditional Access. The subscription expired before I could switch the Conditional Access policy on, so that part is documented as a design in the MFA lab.

**Used in:** Entra ID User Lifecycle and RBAC, and MFA Recovery with a Temporary Access Pass.

---

## 3. ServiceNow Personal Developer Instance

A free developer instance from ServiceNow, where I had the admin role.

| Detail | Value |
|---|---|
| Users I created | K Mbappe (the caller), Vini jr (Tier 1), Arda Guler (Tier 2) |
| Groups I created | Service_Desk, Network_Support |
| How I played each role | ServiceNow's "impersonate user" feature |

**Used in:** ServiceNow Ticket Workflow (INC0010001).

---

## 4. TryHackMe Active Directory Environment

For the domain Group Policy lab I used TryHackMe's **Active Directory Basics** room, opened in the browser.

| Detail | Value |
|---|---|
| Domain | thm.local |
| Domain controller address | 10.201.51.169 |
| Existing OUs | IT, Management, Marketing, Sales and others |
| Test user | Mark (Marketing OU) |

**Used in:** Active Directory GPO lab.

---

## 5. Physical Laptop

The slow startup lab was done on a real laptop (computer name "dell"), not a VM, so the boot times and disk usage in that lab are real measurements.

---

## Which Lab Used What

| Lab | Environment |
|---|---|
| No Internet Access: DNS vs Default Gateway | Windows 10 VM |
| Slow Startup | Physical laptop |
| Print Jobs Stuck in the Queue | Windows 10 VM |
| New Starter Workstation (Windows 11) | Windows 11 VM |
| Joiner, Leaver and Password Reset | Windows 10 VM |
| Endpoint Hardening (Local Group Policy) | Windows 10 VM |
| Deleted Project File (File History) | Windows 10 VM with a second virtual disk |
| Outlook Not Set Up | Windows 10 VM + VirtualLabs1991 tenant |
| Sales New Starter (Microsoft 365) | Windows 10 VM + VirtualLabs1991 tenant |
| New Hire Provisioning (Entra ID) | Browser + ResolvePoint IT tenant |
| User Locked Out (MFA and TAP) | Browser + ResolvePoint IT tenant |
| My Documents Won't Print (Quick Assist) | Windows 11 VM (technician) and Windows 10 VM (user) |
| INC0010001 (ServiceNow) | ServiceNow developer instance |
| New Domain Build, Parts 1 and 2 | Windows Server 2022 VM |
| Staff Changing System Settings (GPO) | TryHackMe Active Directory Basics |

---

## Want to Build Something Similar?

You don't need anything expensive. This is roughly what you'd need to recreate these labs:

- **A PC with enough RAM** to run two or three VMs at once
- **VMware Workstation Pro** (free for personal use) or another hypervisor such as Hyper-V or VirtualBox
- **Windows 10 or 11 and Windows Server 2022 ISOs.** Microsoft's Evaluation Center offers free time-limited evaluation versions of Windows Server.
- **A Microsoft 365 trial** for the Microsoft 365 and Entra ID labs. You'll need Entra ID P1 (included in Business Premium) for Conditional Access.
- **A ServiceNow Personal Developer Instance**, free from the ServiceNow Developer site
- **A TryHackMe account** for the ready-made Active Directory environment

A few tips from building mine:

- Give each VM a clear name so screenshots make sense later (for example Rana.Windows10).
- Give a domain controller a static IP and point its DNS at itself before you install Active Directory.
- Trial tenants expire. Plan the labs you want to do before you start the trial, and take your screenshots as you go.
