# TC-Reg-002: Password mismatch validation

| Field | Value |
|-------|-------|
| **Priority** | Medium |
| **Severity** | Minor |
| **Behavior** | Negative |
| **Type** | Functional |
| **Layer** | E2E |
| **Automation** | Manual |

## Description
Verify real-time validation of password confirmation field.

**Password requirements:**
- Minimum length: 6 characters
- At least 1 special character
- At least 1 uppercase letter

## Preconditions
- Network connection available
- User is not registered in the system
- Registration form is open
- Valid login/First Name/Last Name entered

## Steps

| # | Action | Expected Result |
|---|--------|-----------------|
| 1 | Enter valid password: `Jnth@n!23` | Field accepts input, no error |
| 2 | Enter mismatched password in "Confirm Password": `jOnthn` | ❌ Red error message: "Passwords do not match" |
| 3 | Correct "Confirm Password" to match original: `Jnth@n!23` | ✅ Error disappears |

## Postconditions
- Registration form remains visible
- User is **not** registered in the system
