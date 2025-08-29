# Windows Administration Lab: Backup & Recovery with File History

## User Overview
This lab demonstrates how to **configure backup storage, enable File History, and restore a deleted file** on a Windows 10 workstation. This is a common real‑world Help Desk task to recover files for end users and ensure data protection.

## Steps and Screenshots

### 1. Create and Attach a Virtual Backup Disk

A virtual disk is added in VMware and then initialized in Windows Disk Management.
![Backup Disk Created](./screenshots/New_Virtual_Disk_BackupDisk_Created.PNG)

### 2. Enable File History with Backup Drive
Navigate to **Control Panel → File History** and backup is enabled using the backup disk (E:).
![File History Enabled](./screenshots/File_History_Enabled_With_BackupDisk(E).PNG)

### 3. Create a Test File in Documents
In the Documents folder, a test file named **Project_Plan.docx** is created.
![Project Plan File](./screenshots/Documents_Folder_With_A_Project_Plan_File.PNG)

### 4. Delete the File to Simulate Data Loss
In order to simulate accidental file deletion by a user, the test file is then deleted
![File Deleted](./screenshots/Project_Plan_File_Got_Deleted.PNG)

### 5. Restore File Using File History
The test file is resoted using **File History → Restore Personal Files** .
![File Restored](./screenshots/Restoring_Deleted_File_Using_File_History.PNG)

## Conclusion
This lab successfully demonstrated **File Recovery and Data Backup**

- New virtual disk was created for Data Backup
- File History was enabled to save files in BackupDisk (E:)
- A file was created in Documents folder, then deleted on purpose and was then restored using Windows built‑in recovery feature

