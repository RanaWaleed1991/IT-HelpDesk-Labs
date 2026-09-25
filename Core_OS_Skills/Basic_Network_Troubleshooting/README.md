# Lab 01 — No Internet Access: DNS vs Default Gateway

**[View Full Lab Documentation](lab01_Network_Troubleshooting.md)**

## Purpose
This lab works two "the internet is down" tickets on one Windows 10 workstation — one caused by a bad DNS server, one by a missing default gateway — and shows how layered command-line testing proves which layer failed before anything is changed.

---

## Scenario
A user reports that websites won't load. The same complaint is reproduced twice with two different root causes. Each is diagnosed with `ping`, `nslookup` and `tracert` against a saved baseline, fixed, and verified.

---

## Prerequisites
- VMware Workstation Pro
- Windows 10 virtual machine with internet access
- Command Prompt (Administrator for adapter changes)

---

## Lab Tasks
1. **Capture a known-good baseline** with `ipconfig /all`, a bottom-up ping sequence, `tracert` and `nslookup`.
2. **Ticket 1 — reproduce** an invalid DNS server and flush the DNS cache.
3. **Diagnose** — prove internet is reachable by IP but not by name.
4. **Resolve and verify** by restoring a valid DNS server.
5. **Ticket 2 — reproduce** a missing default gateway.
6. **Diagnose** — prove that even IP traffic fails with "General failure", so DNS is not the cause.
7. **Resolve and verify** by restoring the gateway and tracing the route out.

---

## Screenshots Included
11 screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation. Raw baseline command output is in the [`Outputs`](Outputs) folder.

---

## Learning Outcomes
- A repeatable, bottom-up connectivity test sequence.
- Telling DNS faults from routing faults with one test: pinging a public IP.
- Reading Windows network errors precisely ("timed out" vs "General failure" vs "code 1231").
- Using a baseline as evidence that a fix actually restored normal service.

---

## Skills Demonstrated
`Network Troubleshooting` · `TCP/IP` · `DNS` · `Default Gateway` · `ipconfig · ping · tracert · nslookup` · `Root Cause Analysis`
