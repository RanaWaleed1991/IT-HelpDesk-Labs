# Lab 02 — Slow Startup: Boot Time and Disk Usage Troubleshooting

**[View Full Lab Documentation](lab02_PC_Performance_Troubleshooting.md)**

## Purpose
This lab troubleshoots a real, slow-starting Windows laptop using only built-in tools. Boot duration was measured with Event ID 100, high-impact startup programs were disabled, and the result was verified: boot time fell from 178 to 93 seconds and idle disk usage from 65% to 3%.

---

## Scenario
A user complains that their laptop takes minutes to start and the disk is constantly busy. The task is to measure the problem, find the cause, apply the least disruptive fix and prove the improvement with before-and-after data.

---

## Prerequisites
- A Windows PC with administrator access (this lab used a physical laptop, not a VM)
- Task Manager and Event Viewer (built-in)
- Snipping Tool for evidence capture

---

## Lab Tasks
1. **Measure idle resource usage** in Task Manager.
2. **Review startup programs** and their startup impact.
3. **Record boot duration** from Event Viewer (Diagnostics-Performance, Event ID 100).
4. **Disable unneeded startup programs** (iTunesHelper, Skype).
5. **Re-measure resource usage** after a reboot.
6. **Re-measure boot duration** and compare.

---

## Screenshots Included
6 before-and-after screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation.

---

## Lab Outcomes
- Boot time reduced from **177,860 ms → 92,627 ms** (48% faster).
- Idle disk usage reduced from **65% → 3%**.
- A repeatable method: measure, change one thing, re-measure.

---

## Skills Demonstrated
`Performance Troubleshooting` · `Task Manager` · `Startup Optimisation` · `Event Viewer` · `Before/After Measurement`
