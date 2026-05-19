# Entra Conditional Access Security Baseline

## Project Overview

This project demonstrates a Microsoft Entra ID Conditional Access security baseline. The lab focuses on MFA, admin protection, legacy authentication blocking, break-glass account planning, report-only testing, and rollback documentation.

## Business Problem

Organizations need to protect user identities without accidentally locking out users or administrators. Conditional Access policies help enforce security controls such as MFA and app access restrictions, but they must be planned, tested, and documented carefully.

## Tools Used

- Microsoft Entra ID
- Conditional Access
- MFA
- Sign-in logs
- Report-only mode
- Break-glass account planning
- GitHub documentation
- Markdown

## What This Project Demonstrates

- Conditional Access planning
- MFA enforcement strategy
- Admin account protection
- Break-glass account exclusions
- Legacy authentication blocking
- Report-only testing
- Rollback planning
- IAM security documentation

## Planned Policies

### Policy 1: Require MFA for Administrators

This policy requires MFA for privileged/admin users.

### Policy 2: Require MFA for All Users

This policy requires MFA for standard users accessing cloud applications.

### Policy 3: Block Legacy Authentication

This policy blocks older authentication methods that do not support modern security controls.

### Policy 4: Require Stronger Controls for Sensitive Groups

This policy applies stricter access requirements to sensitive groups such as Finance, HR, IT Admins, and Contractors.

### Policy 5: Break-Glass Account Exclusion

This policy documents emergency admin account exclusions to reduce the risk of total tenant lockout.

## Project Files

- docs/
- screenshots/

## Documentation Created

- Conditional Access Policy Matrix
- Break-Glass Account Plan
- Rollback Plan
- Testing Results

## Key IAM Concepts Demonstrated

### Conditional Access

Conditional Access helps control access based on users, groups, applications, risk, device state, and other conditions.

### MFA

Multi-factor authentication adds another layer of protection beyond a username and password.

### Break-Glass Accounts

Break-glass accounts are emergency administrator accounts used when normal admin access is unavailable.

### Report-Only Testing

Report-only mode allows policies to be tested before enforcing them, reducing the chance of accidentally blocking users.

### Rollback Planning

Rollback documentation explains how to quickly disable or adjust a policy if it causes unexpected access problems.

## Resume Bullet

- Designed a Microsoft Entra Conditional Access security baseline with MFA enforcement, admin protection, legacy authentication blocking, break-glass exclusions, report-only testing, and rollback documentation.

## Status

In progress. This project will be updated with policy documentation, screenshots, testing notes, and final results.
