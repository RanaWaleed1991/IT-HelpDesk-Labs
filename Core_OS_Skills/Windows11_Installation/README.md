# Windows 11 Workstation Build for a New Starter

**[View Full Lab Documentation](Windows11_Installation_Lab.md)**

## Purpose
This lab builds a new-starter workstation from scratch: a clean Windows 11 Pro install in VMware Workstation Pro, a device name that follows naming rules, full patching verified twice, PIN sign-in, and a standard (non-admin) account for day-to-day use.

---

## Scenario
A new employee starts next week and needs a workstation. The machine must be clean, on the business edition of Windows, fully patched, and set up so the user does not work as an administrator.

---

## Prerequisites
- VMware Workstation Pro installed on the host
- Windows 11 ISO image (Win11_24H2_English_x64.iso)
- VM resources: 4 GB RAM, 2 CPU cores, 64 GB disk (Windows 11 minimums)

---

## Lab Tasks
1. **Create the VM** and attach the Windows 11 ISO.
2. **Set language and region**, choose a clean install, select **Windows 11 Pro**.
3. **Install** Windows.
4. **Name the device** following naming rules.
5. **Patch** with Windows Update and restart.
6. **Configure PIN sign-in** and complete first sign-in.
7. **Re-check updates** until the machine reports it is up to date.
8. **Create a standard user account** for daily use.

---

## Screenshots Included
13 screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation.

---

## Learning Outcomes
- End-to-end manual Windows 11 deployment.
- Why Pro (not Home) is required for business devices.
- Patching as part of provisioning, verified rather than assumed.
- Least privilege on the endpoint: standard users for daily work.

---

## Skills Demonstrated
`Windows 11 Deployment` · `VMware Workstation` · `Windows Update` · `Local Accounts` · `Least Privilege` · `Workstation Provisioning`
