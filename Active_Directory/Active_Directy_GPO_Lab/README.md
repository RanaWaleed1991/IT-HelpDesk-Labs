# Active Directory GPO Lab — Control Panel Restriction & Screen Lock

**[View Full Lab Documentation](Active_Directory_GPO_Lab.md)**

## Purpose
This lab uses Active Directory Group Policy to stop staff in Management, Marketing and Sales from changing system settings through Control Panel, and to lock every computer in the domain after 5 minutes of inactivity — then proves both by signing in as a Marketing user.

---

## Scenario
Staff keep changing settings they shouldn't, and computers are being left unlocked. Two GPOs are built, each scoped to the right part of the domain (IT deliberately excluded from the restriction), and tested over Remote Desktop as the domain user Mark.

---

## Prerequisites
- An Active Directory domain with OUs (this lab used TryHackMe's "Active Directory Basics" environment, domain thm.local)
- Group Policy Management Console access
- A domain user in a target OU for testing, and Remote Desktop access

---

## Lab Tasks
1. **Create** the Restrict Control Panel Access GPO.
2. **Configure** Prohibit access to Control Panel and PC settings.
3. **Link** it to the Management, Marketing and Sales OUs only.
4. **Create** the Auto Lock Screen GPO and link it to the domain root.
5. **Set** the machine inactivity limit to 300 seconds.
6. **Test** both policies by signing in as a Marketing user over RDP.

---

## Screenshots Included
13 screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation.

---

## Learning Outcomes
- Creating, editing and linking GPOs with GPMC.
- Scoping policies to OUs, and the difference between user and computer settings.
- Testing Group Policy as a user it is meant to target.

---

## Skills Demonstrated
`Active Directory` · `Group Policy` · `OU Scoping` · `Endpoint Security` · `Remote Desktop` · `Policy Testing`
