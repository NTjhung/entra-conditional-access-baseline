# Conditional Access Testing Results

## Purpose

This document records testing results for the Microsoft Entra Conditional Access baseline lab. The goal is to test policies safely before enforcement and document the expected outcome, actual outcome, and any needed changes.

## Testing Approach

All Conditional Access policies should be tested before enforcement. In this lab, policies are planned and tested using report-only mode when possible.

## Test Accounts and Groups

| Test Item | Purpose |
|---|---|
| Standard test user | Validate normal user MFA behavior |
| Admin test user | Validate administrator MFA behavior |
| Finance test user | Validate sensitive group policy behavior |
| Contractor test user | Validate contractor access behavior |
| Break-glass account | Validate emergency account exclusion |

## Test Case 1: Require MFA for Administrators

| Field | Result |
|---|---|
| Policy Name | Require MFA for Administrators |
| Target | Admin users |
| Expected Result | Admin users should be required to complete MFA |
| Actual Result | Pending testing |
| Status | Not Started |
| Notes | Policy should start in report-only mode before enforcement |

## Test Case 2: Require MFA for All Users

| Field | Result |
|---|---|
| Policy Name | Require MFA for All Users |
| Target | Standard users |
| Expected Result | Users should be required to complete MFA |
| Actual Result | Pending testing |
| Status | Not Started |
| Notes | Test with a small pilot group before applying to all users |

## Test Case 3: Block Legacy Authentication

| Field | Result |
|---|---|
| Policy Name | Block Legacy Authentication |
| Target | All users |
| Expected Result | Legacy authentication should be blocked |
| Actual Result | Pending testing |
| Status | Not Started |
| Notes | Review sign-in logs before enforcing |

## Test Case 4: Require MFA for Sensitive Groups

| Field | Result |
|---|---|
| Policy Name | Require MFA for Sensitive Groups |
| Target | Finance, HR, IT Admins, Contractors |
| Expected Result | Sensitive groups should require MFA |
| Actual Result | Pending testing |
| Status | Not Started |
| Notes | Start with one group before expanding |

## Test Case 5: Break-Glass Account Exclusion

| Field | Result |
|---|---|
| Policy Name | Break-Glass Account Exclusion |
| Target | Emergency administrator accounts |
| Expected Result | Break-glass accounts should be excluded from selected policies |
| Actual Result | Pending testing |
| Status | Not Started |
| Notes | Break-glass activity should be monitored |

## Evidence to Collect

The following screenshots should be collected for the portfolio:

- Conditional Access policy list
- Policy configuration screen
- Report-only mode setting
- Break-glass exclusion setting
- Sign-in log showing Conditional Access result
- Testing result notes

## Final Summary

Testing has not been completed yet. This document will be updated after the policies are created and tested in Microsoft Entra ID.
