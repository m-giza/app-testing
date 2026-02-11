# CL-Reg-001: User Registration Feature Checklist

**Application:** Buggy Cars Rating  
**URL:** https://buggy.justtestit.org/  
**Tested on:** 2026-02-09  
**Tester:** Marsel Giza  
**Reference TCs:** TC-Reg-001, TC-Reg-002, TC-Reg-003  

---

##  1. UI & Basic Navigation

| # | Checkpoint | Result | Notes |
|---|------------|--------|-------|
| 1.1 | Homepage loads without errors | ✅ | |
| 1.2 | "Register" button visible (top-right) | ✅ | |
| 1.3 | Registration form opens on click | ✅ | All fields visible |

---

##  2. Positive Registration Flow

| # | Checkpoint | Result | Notes |
|---|------------|--------|-------|
| 2.1 | Login field accepts input | ✅ | `JHwell@32` |
| 2.2 | First Name field accepts input | ✅ | `Jonathan` |
| 2.3 | Last Name field accepts input | ✅ | `Hwell` |
| 2.4 | Password field masks input | ✅ | •••••••• |
| 2.5 | Registration succeeds with valid password | ✅ | `Jnth@n!23` → green "Registration is successful" |
| 2.6 | User persists after page refresh (F5) | ✅ | "User already exists" on re-attempt |

---

##  3. Password Validation (Negative Cases)

| # | Checkpoint | Result | Notes |
|---|------------|--------|-------|
| 3.1 | Weak password (<6 chars) rejected | ✅ | `jnth` → red error |
| 3.2 | Password without special character rejected | ✅ | (tested via TC-Reg-001 logic) |
| 3.3 | Password without uppercase rejected | ✅ | (tested via TC-Reg-001 logic) |
| 3.4 | Mismatched passwords rejected | ✅ | `jOnthn` vs `Jnth@n!23` → "Passwords do not match" |

---

##  4. UX Observation

| # | Checkpoint | Result | Notes |
|---|------------|--------|-------|
| 4.1 | Form remains visible after successful registration | ⚠️ | **Potential UX issue** - user might expect redirect |
