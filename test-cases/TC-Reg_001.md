# TC-Reg-001: Password validation fails with weak password

| Field | Value |
|-------|-------|
| **Priority** | Medium |
| **Severity** | Major |
| **Behavior** | Negative |
| **Type** | Functional |
| **Layer** | E2E |
| **Automation** | Manual |

## Description
Verify that registration is blocked when password does not meet security requirements.

**Password requirements:**
- Minimum length: 6 characters
- At least 1 special character
- At least 1 uppercase letter

## Preconditions
- Network connection available
- User is not registered in the system

## Steps

| # | Action | Expected Result |
|---|--------|-----------------|
| 1 | Open https://buggy.justtestit.org/ | Homepage loads successfully |
| 2 | Click "Register" button (top-right) | Registration form appears |
| 3 | Enter valid data:<br>• Login: `JHwell@32`<br>• First Name: `Jonathan`<br>• Last Name: `Hwell` | Fields accept input |
| 4 | Enter weak password: `jnth` | Field accepts input, no real-time validation error |
| 5 | Enter confirm password: `jnth` | Field accepts input, no error |
| 6 | Click "Register" button | ❌ Red error message appears indicating password requirements not met |

## Postconditions
- User is **not** registered in the system
- Registration form remains visible with entered data
