## Metadata
| Attribute | Value |
|-----------|-------|
| **ID** | TC-Reg-001 |
| **Path** | app-testing/test-cases/TC-Reg-001 |
| **Priority** | Medium |
| **Severity** | Major |
| **Behavior** | Positive |
| **Type** | Functional |
| **Layer** | E2E |
| **Flaky?** | No |
| **Muted?** | No |
| **Automation** | To be automated |
| **Status** | Actual |
| **Milestone** | - |

## Description
Verify registration behavior with various password inputs.

## Preconditions
- Network connection is available.

## Postconditions
- User is registered successfully.

## Test Steps with Detailed Validation

### Step 1: Open site
**Action:** Open https://buggy.justtestit.org/  
**Expected:** Homepage loads successfully.

### Step 2: Click register button
**Action:** Click register button visible on the top right.  
**Expected:** Registration form appears.

### Step 2.1: Enter login
**Action:** Enter `JHwell@32` in login field.  
**Expected:** Field accepts input.

### Step 2.2: Enter First Name
**Action:** Enter `Jonathan` in First Name field.  
**Expected:** Field accepts input.

### Step 2.3: Enter Last Name
**Action:** Enter `Hwell` in Last Name field.  
**Expected:** Field accepts input.

### Step 2.4: Password Field Validation Sequence

#### **Step 2.4.1: Test short password**
**Action:** Change previously inserted password to a password with 4 letters (e.g. `jnth`).  
**Expected:** Field accepts input, there is **no error message** (obserwacja: brak walidacji w czasie rzeczywistym).

#### **Step 2.4.2: Test password with special characters**
**Action:** Delete previously inserted password and change it to a password that contains special characters (e.g. `Jnth@n123`).  
**Expected:** Field accepts input, there is **no error message**.

#### **Step 2.4.3: Test password mismatch in confirmation field**
**Action:** In the "Confirm Password" field, enter password without any special characters, with only 6 letters and one capital letter (e.g., `Jnth`).  
**Expected:** **Red error message** displays under the Confirm Password field with: *"Passwords do not match"*.

#### **Step 2.4.4: Correct the password mismatch**
**Action:** In the same field, input the same password used in step 2.4.2 (`Jnth@n123`).  
**Expected:** Red error message **disappears**.

### Step 3: Observe 'Register' button
**Action:** Check the state of the 'Register' button.  
**Expected:** Button should become **active**.

### Step 4: Complete registration
**Action:** Click the 'Register' button.  
**Expected:** **Green information message** appears: *"Registration is successful"*. User is not redirected; the form remains visible.

### Step 5: Locate log-in form
**Action:** Find log-in form on the navbar on top of the site.  
**Expected:** Login and password fields are visible with greyed-out *'Login'* and *'Password'* placeholders.

### Step 6: Input registration login
**Action:** Input login used for registration (`JHwell@32`).  
**Expected:** Field accepts input.

### Step 7: Input registration password
**Action:** Input password used for registration from step 2.4.2 (`Jnth@n123`).  
**Expected:** Field accepts input.

### Step 8: Click 'Login' button
**Action:** Click 'Login' button next to the log-in form.  
**Expected:** Log-in form **disappears**; user account menu becomes visible.

### Step 9: Logout
**Action:** Click 'Logout' button.  
**Expected:** User is logged off; the log-in form becomes visible again.

## Pass/Fail Criteria
- **PASS:** All expected results match actual behavior
- **FAIL:** Any deviation from expected results (e.g., missing error messages, button not enabling)

##  Obserwacje i notatki
1. **Brak walidacji w czasie rzeczywistym:** System nie sprawdza wymagań hasła podczas wpisywania (tylko przy submisie).
2. **Kolejność kroków ważna:** Child steps (2.4.x) testują różne stany tego samego pola.
3. **Test pełnego przepływu:** Rejestracja → Logowanie → Wylogowanie.
4. **Gotowy do automatyzacji:** Struktura jest sekwencyjna.


<img width="607" height="858" alt="tc-reg-001-preview_1 of 2" src="https://github.com/user-attachments/assets/b8d713cc-1f59-4b7a-8d85-92881b939094" />
<img width="607" height="795" alt="tc-reg-001-preview_2 of 2" src="https://github.com/user-attachments/assets/76444a02-cb8a-4b1a-ab0a-6affb54ae52a" />




