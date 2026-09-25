# Lab 03 — Print Jobs Stuck in the Queue

**[View Full Lab Documentation](lab03_Printer_Troubleshooting.md)**

## Purpose
This lab installs a network printer by IP address on Windows 10, then diagnoses and fixes two common printing tickets — jobs held by an offline printer, and a jammed queue caused by the Print Spooler — using the print queue and PrintService event logs (Event IDs 372 and 350).

---

## Scenario
A user needs a network printer added. Afterwards their documents never print, and later the queue jams so badly that jobs cannot be cancelled. Each problem is traced to its cause and resolved without rebooting the PC.

---

## Prerequisites
- Windows 10 virtual machine (VMware Workstation Pro)
- Local administrator rights
- No physical printer needed — a placeholder TCP/IP address (192.168.1.50) is used

---

## Lab Tasks
1. **Add a printer** using a TCP/IP address.
2. **Select a driver** (Generic / Text Only).
3. **Confirm the installation** in Devices and Printers.
4. **Diagnose held jobs** — printer in offline mode.
5. **Confirm with Event Viewer** — PrintService Admin log, Event ID 372.
6. **Reproduce a jammed queue** by stopping the Print Spooler.
7. **Read the spooler error** — Event ID 350.
8. **Restart the Print Spooler** and confirm the queue clears.

---

## Screenshots Included
8 screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation.

---

## Lab Outcomes
- Installed a TCP/IP printer and set it as default.
- Identified an offline printer from the queue window and Event ID 372.
- Identified a failed spooler from "Error processing command" and Event ID 350.
- Cleared a jammed queue by restarting the Print Spooler, with no reboot.

---

## Skills Demonstrated
`Printer Installation` · `Print Queue Management` · `Event Viewer` · `Print Spooler` · `Windows Services`
