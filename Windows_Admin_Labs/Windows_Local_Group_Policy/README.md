# Endpoint Hardening with Local Group Policy

**[View Full Lab Documentation](lab02_Local_Group_Policy.md)**

## Purpose
This lab hardens a stand-alone Windows 10 workstation with Local Group Policy: password complexity and an 8-character minimum are enforced, all USB storage is blocked, and each control is proven by testing it as a user — a weak password is rejected and a USB drive is denied.

---

## Scenario
A security review found that users on a non-domain workstation can set weak passwords and copy data to USB drives. Both risks must be closed and verified, without a domain to push policy from.

---

## Prerequisites
- Windows 10 virtual machine (VMware Workstation Pro), Pro edition or higher (gpedit.msc)
- Local administrator rights
- A USB drive for testing

---

## Lab Tasks
1. **Enable password complexity** requirements.
2. **Set the minimum password length** to 8 characters.
3. **Review the full password policy** and note remaining gaps.
4. **Deny all removable storage** access.
5. **Confirm** the removable storage setting.
6. **Apply** with `gpupdate /force`.
7. **Test** — attempt a weak password.
8. **Test** — attempt to open a USB drive.

---

## Screenshots Included
8 screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation.

---

## Lab Outcomes
- Enforced password complexity and minimum length on a stand-alone PC.
- Blocked USB storage without blocking other USB devices.
- Verified both controls from the user's side, and documented follow-up recommendations.

---

## Skills Demonstrated
`Local Group Policy` · `Password Policy` · `Removable Storage Control` · `Endpoint Hardening` · `gpupdate`
