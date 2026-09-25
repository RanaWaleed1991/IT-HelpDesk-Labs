# INC0010001 — Full Incident Lifecycle in ServiceNow

**[View Full Lab Documentation](ServiceNow_Ticket_Workflow_Lab.md)**

## Purpose
This lab follows one real ServiceNow incident, INC0010001 (VPN drops after 5 seconds), from submission to resolution: triage and re-prioritisation, Tier 1 investigation, escalation to the network team, internal work notes versus customer updates, and resolution on user confirmation.

---

## Scenario
A remote employee cannot stay connected to the VPN and cannot reach the file server. The ticket is logged through the self-service portal, triaged by the service desk, escalated to Network Support after a certificate mismatch is found, fixed, and resolved once the user confirms.

---

## Prerequisites
- ServiceNow Personal Developer Instance
- Admin role (to create users and groups and to impersonate)
- Basic understanding of ITIL incident management

---

## Lab Tasks
1. **Log the incident** as the end user through the Service Portal.
2. **Assign** to the Service_Desk group and a Tier 1 agent.
3. **Triage** — correct Impact and Urgency, and so the Priority.
4. **Investigate** — record work notes and update the customer.
5. **Escalate** to Network_Support with a clear handover.
6. **Fix and confirm** with the user.
7. **Resolve** with a resolution code and notes.

---

## Screenshots Included
7 screenshots in the [`screenshots`](screenshots) folder, embedded step by step in the lab documentation.

---

## Learning Outcomes
- The full incident lifecycle in ServiceNow, recorded on the ticket.
- How Impact and Urgency set Priority, and why triage corrects it.
- The difference between Work notes (internal) and Additional comments (customer-visible).
- Escalating with evidence and resolving on user confirmation.

---

## Skills Demonstrated
`ServiceNow` · `ITIL Incident Management` · `Triage & Prioritisation` · `Escalation` · `Customer Communication`
