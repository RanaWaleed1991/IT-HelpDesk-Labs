# Deleted Project File — Backup & Recovery with File History

**[View Full Lab Documentation](lab03_Backup_Recovery_Using_File_History.md)**

## Purpose
This lab works a backup request and the data-loss incident that follows it on Windows 10: a dedicated backup disk is provisioned, File History is enabled, and when the user deletes a project document it is restored from that afternoon's saved version.

---

## Scenario
A manager asks for a workstation to be backed up. Later the same day the user deletes Project_Plan.docx from Documents. Because File History was already running, the file is recovered from the 2:25 PM version in six minutes.

---

## Prerequisites
- Windows 10 VM in VMware Workstation Pro
- A second virtual disk to use as the backup drive (E:)
- Local administrator rights

---

## Lab Tasks
1. **Provision a backup disk** and format it in Disk Management.
2. **Turn on File History** targeting the backup disk.
3. **Confirm the user's file** exists and is protected.
4. **Reproduce the data loss** by deleting the file.
5. **Restore the file** from File History to its original location.

---

## Screenshots Included
5 screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation.

---

## Lab Outcomes
- Set up File History on a dedicated backup disk.
- Recovered a deleted user document from a point-in-time version.
- Documented the incident timeline from backup to restore.

---

## Skills Demonstrated
`Backup & Recovery` · `File History` · `Disk Management` · `Data Loss Incident Handling`
