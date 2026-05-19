# Conditional Access Policy Matrix

## Purpose

This document outlines a basic Microsoft Entra ID Conditional Access security baseline. The goal is to improve identity security while reducing the risk of accidentally locking out users or administrators.

## Policy Matrix

| Policy Name | Target Users | Target Apps | Control | Mode |
|---|---|---|---|---|
| Require MFA for Administrators | Admin users | All cloud apps | Require MFA | Report-only |
| Require MFA for All Users | All standard users | All cloud apps | Require MFA | Report-only |
| Block Legacy Authentication | All users | All cloud apps | Block access | Report-only |
| Require MFA for Sensitive Groups | Finance, HR, IT Admins, Contractors | Selected apps | Require MFA | Report-only |
| Break-Glass Exclusion | Break-glass accounts | All cloud apps | Excluded from selected policies | Documented exception |

## Policy 1: Require MFA for Administrators

### Purpose

Administrator accounts have elevated permissions and should require stronger authentication.

### Target Users

- Global Administrators
- User Administrators
- Groups Administrators
- Security Administrators
- Privileged Role Administrators

### Control

Require multi-factor authentication.

### Testing Approach

Start in report-only mode and review sign-in logs before enforcement.

---

## Policy 2: Require MFA for All Users

### Purpose

All users should use MFA to reduce the risk of account compromise.

### Target Users

- Standard employees
- Contractors
- Department users

### Control

Require multi-factor authentication.

### Testing Approach

Start with a test group before expanding to all users.

---

## Policy 3: Block Legacy Authentication

### Purpose

Legacy authentication methods can bypass modern security controls and should be blocked.

### Target Users

All users, excluding emergency accounts if needed.

### Control

Block access.

### Testing Approach

Use report-only mode first and review sign-in logs for impact.

---

## Policy 4: Require MFA for Sensitive Groups

### Purpose

Sensitive departments should have stronger access controls.

### Target Groups

- SG-Finance-Employees
- SG-HR-Employees
- SG-IT-Admins
- SG-Contractors

### Control

Require MFA.

### Testing Approach

Test with one group before applying broadly.

---

## Policy 5: Break-Glass Account Exclusion

### Purpose

Break-glass accounts help prevent total administrative lockout.

### Target Accounts

- Emergency admin account 1
- Emergency admin account 2

### Control

Excluded from selected Conditional Access policies.

### Notes

Break-glass accounts should not be used for daily administration. They should be monitored and protected with strong passwords.
