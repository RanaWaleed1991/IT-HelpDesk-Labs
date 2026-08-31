# User Locked Out — MFA Recovery, Temporary Access Pass & Conditional Access Hardening

**Ticket Subject:** User Locked Out — MFA Recovery After Device Change
**Category:** Identity & Access Management / Security
**Priority:** P2 — User Blocked
**Environment:** Microsoft Entra ID / Microsoft 365 (ResolvePoint IT tenant)

---

## Problem Statement
James Whitfield (Marketing Coordinator) replaced his phone over the weekend and traded in his old device, leaving him locked out of Microsoft 365 because his MFA approvals were routing to the old, inaccessible phone. The task is to recover his access without a full password reset by issuing a Temporary Access Pass, guide him through re-registering MFA on his new device, and then — as a follow-on management request — mature the tenant's security posture by migrating from Security Defaults to a targeted Conditional Access policy.

---

## Tools Used
- **Microsoft Entra ID** (authentication methods, Temporary Access Pass, Conditional Access, Security Defaults)
- **Microsoft Authenticator** (user-side MFA re-registration)
- **Microsoft 365 User Portal** (verification)
- **Web browser** (host machine + private/incognito window for user-side testing)

---

## Technical Steps

### 1. Capture the Baseline (Security Defaults ON)
Before making any changes, documented the tenant's starting security posture. Navigated to **Overview → Properties → Security defaults** and confirmed the tenant was protected by Security Defaults — the baseline all-or-nothing MFA enforcement mechanism.

**Screenshot:**
![Security Defaults ON Baseline](.screenshots/Security\_Defaults\_showing\_ON\_as\_the\_baseline\_state)

---

### 2. Review the User's Authentication Methods
Diagnosed the lockout by navigating to **Users → All Users → James Whitfield → Authentication methods**. Reviewed the currently registered methods, which pointed to the old (now inaccessible) device — confirming the root cause of the lockout.

**Screenshot:**
![James Whitfield Authentication Methods](screenshots/James-Whitfield_Authentication_Methods.png)

---

### 3. Require MFA Re-registration (Simulate Lost Device)
Cleared the stale authentication state by selecting **Require re-register multifactor authentication**. This forces the user to set up MFA fresh on their new device on next sign-in, without exposing the account or requiring a password reset.

**Screenshot:**
![MFA Re-registration Confirmation](screenshots/MFA_Re-registration_Confirmation.png)

---

### 4. Generate a Temporary Access Pass (TAP)
Issued a **Temporary Access Pass** to James via **Users → James Whitfield → Authentication methods → Add authentication method → Temporary Access Pass**. A TAP is a time-limited passcode that lets a locked-out user sign in *and* register new MFA methods — the correct L2 tool for device-loss recovery, avoiding an unnecessary password reset.

**Screenshot:**
![Temporary Access Pass Generated](screenshots/Temporary_Access_Pass_Generated.png)

---

### 5. Verify Recovery — User-Side Sign-In and Re-Registration
Opened a private browser window, signed in to the Microsoft 365 portal as James, and entered the **Temporary Access Pass** instead of a password/MFA approval. The sign-in succeeded and prompted MFA re-registration.

**Screenshot:**
![James Whitfield Signing In With TAP](screenshots/James-Whitfield_Signing_In_With_TAP.png)

Completed re-registration of the Microsoft Authenticator app, simulating setup on the new phone. The confirmation screen — **"Authenticator Added — This is now your default sign-in method"** — verified the full recovery loop closed successfully.

**Screenshot:**
![MFA Authenticator Re-added Success](screenshots/MFA_Authenticator_Re-added_Success.png)

---

### 6 & 7. Conditional Access Migration — Design & Dependency
The follow-on management task was to migrate the tenant from Security Defaults to a targeted Conditional Access policy requiring MFA. On reaching the Conditional Access policy builder, Entra ID confirmed the key architectural dependency: **Security Defaults must be disabled before a Conditional Access policy can be enabled** — the two enforcement mechanisms cannot run simultaneously.

**Screenshot:**
![Conditional Access Policy Creation with Security Defaults Warning](screenshots/Conditional_Access_Policy_Creation_Security_Defaults_Warning.png)

**Policy Design (as it would be built in production):**

| Setting | Value |
|---|---|
| Name | `CA01 - Require MFA for All Users` |
| Users | Include: All Users — **Exclude: break-glass admin account** |
| Target resources | All cloud apps |
| Grant | Grant access → Require multifactor authentication |
| Enable policy | Report-only first, then On after validation |

> **Environment Note:** The tenant's Microsoft 365 subscription expired before Steps 6–7 could be enforced end-to-end. The Conditional Access policy build is therefore documented as designed rather than saved-and-enforced. The dependency (disable Security Defaults first) and the correct policy structure are demonstrated by the policy-builder screenshot above. In a licensed production environment, this policy would be created in **Report-only** mode, validated against sign-in logs, then switched to **On**.

> **Best Practice — Break-Glass Exclusion:** Any MFA-enforcing Conditional Access policy must exclude a dedicated break-glass admin account, and should always start in Report-only mode. Enabling a misconfigured policy in "On" mode with no exclusion is one of the most common ways administrators lock an entire organisation — including themselves — out of a tenant.

---

## MFA Troubleshooting Decision Tree
A reusable process for handling the highest-volume ticket category at any service desk:

```
MFA ticket received
│
├─ Is the user fully locked out (can't sign in at all)?
│   └─ YES → Generate Temporary Access Pass → user signs in → re-registers MFA
│
├─ Can they sign in but MFA is failing?
│   ├─ New device?          → Re-register Authenticator on new device
│   ├─ Not receiving prompts? → Verify method; switch to phone/SMS temporarily
│   └─ Stale/old method?     → Admin requires re-registration → user re-registers
│
└─ Confirm old/stale methods removed → verify sign-in → close ticket
```

---

## Key Takeaways
- **Temporary Access Pass beats a password reset for device loss.** A TAP recovers a locked-out user *and* lets them register new MFA, without weakening the account. Reaching for a password reset on every MFA lockout is a junior habit; TAP is the correct L2 tool.
- **Security Defaults and Conditional Access are a trade-off, not a stack.** Security Defaults is a free, all-or-nothing switch for small orgs; Conditional Access is granular and license-gated (Entra ID P1). You cannot run both — migrating from one to the other is a real decision every maturing organisation makes.
- **Break-glass exclusions are non-negotiable.** The fastest way to cause a tenant-wide outage is enabling an MFA policy with no admin exception. Report-only mode plus a break-glass exclusion is the safe migration pattern.
- **Document the process, not just the fix.** A written troubleshooting decision tree turns "I reset his MFA" into "I follow a repeatable diagnostic process" — which is what distinguishes L2-level operational thinking.

---

## Skills Demonstrated
`Microsoft Entra ID` · `Multi-Factor Authentication (MFA)` · `Temporary Access Pass (TAP)` · `MFA Recovery & Troubleshooting` · `Conditional Access (design)` · `Security Defaults Migration` · `Least-Privilege / Break-Glass Design`
