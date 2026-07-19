Ticket #502: MFA Recovery, Temporary Access Pass & Conditional Access
Purpose
This lab demonstrates end-to-end MFA lockout recovery in Microsoft Entra ID — diagnosing a locked-out user, issuing a Temporary Access Pass, re-registering MFA on a new device, and migrating the tenant's security posture from Security Defaults toward a targeted Conditional Access policy.
View Full Lab Documentation
---
Scenario
James Whitfield (Marketing Coordinator) replaced his phone and is locked out of Microsoft 365 because MFA approvals route to his old, traded-in device. The task is to recover his access without a password reset, then harden the tenant with Conditional Access.
---
Prerequisites
Microsoft 365 tenant with Entra ID P1 (ResolvePoint IT)
Global Admin or Authentication Administrator account
Microsoft Entra ID access
Microsoft Authenticator app for user-side re-registration
Host browser + private/incognito window for verification
---
Lab Tasks
Capture the baseline — confirm Security Defaults is ON.
Review authentication methods to diagnose the lockout.
Require MFA re-registration to clear the stale device.
Generate a Temporary Access Pass (TAP) for recovery.
Verify recovery — user signs in with TAP and re-registers MFA.
Design a Conditional Access policy requiring MFA (Security Defaults dependency documented).
Document the MFA troubleshooting decision tree.
---
Screenshots Included
All screenshots are located in the `/screenshots` folder.
---
Learning Outcomes
MFA lockout diagnosis and recovery without a password reset.
Temporary Access Pass as the correct tool for device-loss scenarios.
The Security Defaults vs Conditional Access trade-off and migration path.
Break-glass exclusions and Report-only mode as safe rollout practices.
A documented, repeatable MFA troubleshooting process.
---
Environment Note
The tenant's Microsoft 365 subscription expired before the Conditional Access policy could be enforced end-to-end. The policy is documented as designed, with the Security Defaults dependency demonstrated via the policy-builder screenshot — reflecting how real-world work blocked by environment constraints is handled professionally.
---
Skills Demonstrated
`Microsoft Entra ID` · `MFA` · `Temporary Access Pass` · `MFA Recovery` · `Conditional Access (design)` · `Security Defaults Migration` · `Break-Glass Design`
