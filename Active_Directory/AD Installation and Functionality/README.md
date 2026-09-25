# New Domain Build — Domain Controller, First User & RBAC File Share

**[View Full Lab Documentation — Part 1: Build and Prepare the Server](Lab_Documentation_Part1.md)**

**[View Full Lab Documentation — Part 2: Active Directory, Users, Groups and Shares](Lab_Documentation_Part2.md)**

## Purpose
This lab builds a Windows Server 2022 domain controller from scratch for a small office with no central user management, then onboards the first domain user into a security group and publishes a team file share that only that group can read.

---

## Scenario
A small office runs on stand-alone PCs with separate local accounts and uncontrolled shared files. IT is asked to introduce central management: build RANA-DC01, create the lab.local domain, onboard Kylian Mbappe into the Forward team, and give the team read-only access to a shared folder.

---

## Prerequisites
- VMware Workstation Pro
- Windows Server 2022 evaluation ISO
- Basic understanding of Active Directory, DNS and NTFS permissions

---

## Lab Tasks
**Part 1 — Build and prepare the server**
1. Create and size the VM; install Windows Server 2022 Standard (Desktop Experience).
2. Rename the server to RANA-DC01.
3. Configure a static IP with DNS pointing at the server itself.
4. Start Add Roles and Features targeting RANA-DC01.

**Part 2 — Put the domain to work**
1. Install AD DS and promote the server to the domain controller for lab.local.
2. Create the user Kylian Mbappe.
3. Create the Forward security group and add the user.
4. Share the Forward Data folder and confirm it is published.
5. Grant the Forward group read-only NTFS permissions.

---

## Screenshots Included
22 screenshots in the [`screenshots`](screenshots) folder, embedded step by step across Part 1 and Part 2.

---

## Learning Outcomes
- Preparing a server for Active Directory: naming, static IP and DNS.
- Installing AD DS and promoting a domain controller.
- Managing users and security groups in Active Directory.
- Role-based, least-privilege access to shared data with NTFS permissions.

---

## Skills Demonstrated
`Windows Server 2022` · `Active Directory` · `Domain Controller` · `DNS` · `Security Groups` · `NTFS Permissions` · `RBAC`
