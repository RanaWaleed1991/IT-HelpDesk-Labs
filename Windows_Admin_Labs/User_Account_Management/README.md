# Joiner, Leaver & Password Reset — Local Account Administration

**[View Full Lab Documentation](lab01_User_Account_Management.md)**

## Purpose
This lab handles three everyday account requests on a stand-alone Windows 10 PC: creating a new starter's account with remote access, resetting a manager's forgotten password, and removing a retired user's account — each verified, and each with its side effects understood before confirming.

---

## Scenario
A small office shares a non-domain Windows 10 PC. A new starter (RanaW) needs an account and remote access, a manager (StephM) is locked out, and a retiree's account (OG) must be removed.

---

## Prerequisites
- Windows 10 VM (VMware Workstation Pro)
- Local administrator rights
- Command Prompt

---

## Lab Tasks
1. **Create a new user** (RanaW) with a forced password change at next logon.
2. **Add the user to Remote Desktop Users** — remote access without admin rights.
3. **Reset a password** (StephM) and understand the encrypted-data warning.
4. **Capture the account list** with `net user` before removing anything.
5. **Delete a leaver's account** (OG) and understand the SID warning.
6. **Verify** the final account list with `net user`.

---

## Screenshots Included
8 screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation.

---

## Lab Outcomes
- Worked a full joiner / password reset / leaver cycle on local accounts.
- Granted remote access through group membership, not admin rights.
- Verified every change from the command line.

---

## Skills Demonstrated
`Local User Management` · `Password Resets` · `Group Membership` · `Joiner / Mover / Leaver` · `Least Privilege` · `net user`
