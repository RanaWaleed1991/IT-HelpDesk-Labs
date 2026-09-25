# MFA Recovery, Temporary Access Pass & Conditional Access

**[View Full Lab Documentation](MFA_TAP_Conditional_Access.md)**

## Purpose
This lab demonstrates end-to-end MFA lockout recovery in Microsoft Entra ID — diagnosing a locked-out user, issuing a Temporary Access Pass, re-registering MFA on a new device, and planning the tenant's move from Security Defaults to a targeted Conditional Access policy.

---

## Scenario
James Whitfield (Marketing Coordinator) replaced his phone and is locked out of Microsoft 365 because MFA approvals route to his old, traded-in device. The task is to recover his access without a password reset, then harden the tenant with Conditional Access.

---

## Prerequisites
- Microsoft 365 tenant with Entra ID P1 (ResolvePoint IT)
- Global Admin or Authentication Administrator account
- Microsoft Entra ID access
- Microsoft Authenticator app for user-side re-registration
- Host browser + private/incognito window for verification

---

## Lab Tasks
1. **Capture the baseline** — confirm Security Defaults is ON.
2. **Review authentication methods** to diagnose the lockout.
3. **Require MFA re-registration** to clear the stale device.
4. **Generate a Temporary Access Pass (TAP)** for recovery.
5. **Verify recovery** — user signs in with TAP and re-registers MFA.
6. **Design a Conditional Access policy** requiring MFA (Security Defaults dependency documented).
7. **Document the MFA troubleshooting decision tree.**

---

## Screenshots Included
6 screenshots covering Tasks 1–5 in the [`screenshots`](screenshots) folder — each is embedded at the matching step of the lab documentation.

---

## Learning Outcomes
- MFA lockout diagnosis and recovery without a password reset.
- Temporary Access Pass as the correct tool for device-loss scenarios.
- The Security Defaults vs Conditional Access trade-off and migration path.
- Break-glass exclusions and Report-only mode as safe rollout practices.
- A documented, repeatable MFA troubleshooting process.

---

## Environment Note
The tenant's Microsoft 365 subscription expired before the Conditional Access policy could be enforced end-to-end. The policy is documented as designed (Step 6), including the Security Defaults dependency — reflecting how real-world work blocked by an environment constraint is handled professionally: scope what was done, document what remains.

---

## Skills Demonstrated
`Microsoft Entra ID` · `MFA` · `Temporary Access Pass` · `MFA Recovery` · `Conditional Access (design)` · `Security Defaults Migration` · `Break-Glass Design`
