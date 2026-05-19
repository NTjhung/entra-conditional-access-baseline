# Break-Glass Account Plan

## Purpose

Break-glass accounts are emergency administrator accounts used when normal administrator access is unavailable. These accounts help prevent a full tenant lockout if Conditional Access, MFA, or other identity controls cause unexpected access problems.

## Why Break-Glass Accounts Matter

Conditional Access policies can improve security, but a misconfigured policy could accidentally block administrators. A break-glass account provides a backup way to regain access and fix the issue.

## Lab Break-Glass Accounts

For this lab, the following emergency admin accounts are planned:

| Account | Purpose | Daily Use? |
|---|---|---|
| breakglass01 | Emergency tenant access | No |
| breakglass02 | Backup emergency tenant access | No |

## Break-Glass Account Rules

1. Break-glass accounts should only be used during emergencies.
2. They should not be used for daily administration.
3. They should have strong passwords.
4. They should be cloud-only accounts.
5. They should be excluded from selected Conditional Access policies to prevent total lockout.
6. Sign-in activity should be monitored.
7. Access should be reviewed regularly.
8. Passwords should be stored securely according to company policy.

## Conditional Access Exclusion Plan

Break-glass accounts may be excluded from selected policies, such as:

- Require MFA for all users
- Require compliant device
- Location-based restrictions
- Risk-based sign-in restrictions

These exclusions should be documented and monitored because excluded accounts can create risk if they are compromised.

## Monitoring Plan

Break-glass account activity should be reviewed regularly.

Recommended monitoring items:

- Successful sign-ins
- Failed sign-ins
- Sign-ins from unusual locations
- Password changes
- Role changes
- Conditional Access bypass activity

## Example Emergency Use Case

If a Conditional Access policy accidentally blocks administrators from signing in, an authorized person can use a break-glass account to access the tenant, disable or adjust the policy, and restore normal administrator access.

## Security Notes

Break-glass accounts reduce lockout risk, but they also create security risk if not protected. They should be highly restricted, monitored, and documented.
