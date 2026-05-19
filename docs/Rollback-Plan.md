# Conditional Access Rollback Plan

## Purpose

This rollback plan documents what to do if a Conditional Access policy causes unexpected access issues. The goal is to restore access quickly while keeping a record of what happened.

## When to Use This Rollback Plan

Use this plan if:

- Users are unexpectedly blocked from signing in
- Administrators are unable to access required portals
- MFA prompts are failing
- A business-critical application becomes unavailable
- A Conditional Access policy impacts more users than expected
- Report-only testing shows unexpected results before enforcement

## Rollback Preparation

Before enabling Conditional Access policies, the following should be completed:

1. Create and document break-glass accounts.
2. Confirm break-glass accounts can sign in.
3. Start policies in report-only mode when possible.
4. Test with a small pilot group first.
5. Document policy settings before enforcement.
6. Notify support teams before major policy changes.

## Rollback Steps

1. Sign in with a break-glass administrator account if normal admin access is blocked.
2. Open the Microsoft Entra admin center.
3. Go to Conditional Access policies.
4. Identify the policy causing the issue.
5. Change the policy from **On** to **Report-only** or **Off**.
6. Save the policy change.
7. Confirm affected users can sign in again.
8. Review sign-in logs to confirm the policy impact.
9. Document the issue and action taken.
10. Adjust the policy before testing again.

## Policy Rollback Table

| Issue | Likely Cause | Rollback Action |
|---|---|---|
| Admins cannot sign in | Admin MFA or device policy misconfiguration | Use break-glass account and disable policy |
| Users blocked unexpectedly | Policy targeted too many users | Move policy to report-only mode |
| App access blocked | Incorrect app targeting | Remove app from policy scope |
| MFA prompts failing | MFA registration or method issue | Temporarily disable policy or exclude pilot group |
| Contractors blocked | Group targeting issue | Review contractor group assignment |

## Post-Rollback Review

After access is restored, complete these steps:

1. Review the Conditional Access policy configuration.
2. Review sign-in logs.
3. Confirm affected users and groups.
4. Identify what caused the issue.
5. Update the policy matrix.
6. Retest in report-only mode.
7. Document lessons learned.

## Documentation Notes

Every rollback should be documented with:

- Date and time
- Policy name
- Affected users or groups
- Issue description
- Action taken
- Final outcome
- Person who completed the rollback

## Summary

A rollback plan helps reduce risk when deploying Conditional Access. Policies should be tested carefully, started in report-only mode when possible, and supported by documented break-glass access.
