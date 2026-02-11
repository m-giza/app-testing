# CL-Reg-001: User Registration Feature Checklist

**Application:** Buggy Cars Rating  
**URL:** https://buggy.justtestit.org/  
**Tested on:** 2026-02-11  
**Tester:** Marsel Giza  
**Reference TCs:** TC-Reg-001, TC-Reg-002, TC-Reg-003  

---

## 1. UI & Navigation

| # | Checkpoint | Result | Notes |
|---|------------|--------|-------|
| 1.1 | Homepage loads without errors | ✅ | |
| 1.2 | "Register" button visible in top-right navigation | ✅ |  |
| 1.3 | Clicking "Register" opens registration form | ✅ | Form appears without page reload |
| 1.4 | All form fields visible: Login, First Name, Last Name, Password, Confirm Password | ✅ |  |
| 1.5 | "Register" button initially disabled (empty form) | ✅ |  |

---

## 2. Field Validation - Positive Cases

| # | Checkpoint | Result | Notes |
|---|------------|--------|-------|
| 2.1 | Login field accepts min. 3 characters | ✅ | `JHwell@32` accepted |
| 2.2 | First Name field accepts alphabetic input | ✅ | `Jonathan` accepted |
| 2.3 | Last Name field accepts alphabetic input | ✅ | `Hwell` accepted |
| 2.4 | Password field masks input (••••••) | ✅ | Characters hidden on typing |
| 2.5 | Confirm Password field masks input | ✅ | Characters hidden on typing |
| 2.6 | "Register" button becomes active after all fields filled | ✅ | With valid data from TC-Reg-003 |
| 2.7 | Registration succeeds with valid credentials | ✅ | Green message: "Registration is successful" |
| 2.8 | User persists after page refresh (F5) | ✅ | "User already exists" on re-attempt |

---

##  3. Field Validation - Negative Cases (Security)

| # | Checkpoint | Result | Notes |
|---|------------|--------|-------|
| 3.1 | Password <6 characters rejected | ✅ | `jnth` → red error |
| 3.2 | Password without special character rejected | ✅ | `Jonathan1` → red error |
| 3.3 | Password without uppercase letter rejected | ✅ | `jonathan!` → red error |
| 3.4 | Mismatched passwords rejected | ✅ | "Passwords do not match" error |
| 3.5 | Empty submission blocked (all fields required) | ✅ | Button remains disabled |
| 3.6 | Very long password (50+ chars) handled gracefully | ✅ | No crash, proper validation |
| 3.7 | SQL injection attempt blocked (`' OR '1'='1`) | ✅ | Generic error, no DB exposure |
| 3.8 | XSS attempt blocked (`<script>alert()</script>`) | ✅ | Input sanitized, no script execution |

---

##  4. Cross-Browser Compatibility

| # | Browser / Environment | Result | Notes |
|---|------------------------|--------|-------|
| 4.1 | Chrome (latest, Windows) | ✅ | Full functionality |
| 4.2 | Firefox (latest, Windows) | ✅ | Full functionality |

---

##  5. UX & Edge Cases

| # | Checkpoint | Result | Notes |
|---|------------|--------|-------|
| 5.1 | Form remains visible after successful registration | ⚠️ | **Potential UX issue** — user expects redirect |
| 5.2 | Error messages disappear after correction | ✅ | Real-time validation works |
| 5.3 | Tab navigation works between fields | ✅ | Keyboard accessibility |
| 5.4 | Password visibility toggle NOT present | ✅ | Expected (security best practice) |
| 5.5 | Concurrent registration (same user) blocked | ✅ | Second attempt shows "User exists" |
