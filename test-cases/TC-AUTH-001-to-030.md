# TC-AUTH — Authentication Test Cases
> Module: User Authentication | Total: 30 Test Cases

---

## Legend

| Field | Description |
|---|---|
| **TC-ID** | Unique test case identifier |
| **Priority** | P1 / P2 / P3 |
| **Preconditions** | State required before executing steps |
| **Steps** | Numbered actions to perform |
| **Expected Result** | What should happen |
| **Status** | Pass / Fail / Blocked / pass |

---

### TC-AUTH-001 — Register with valid email and password

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-001 |
| **Priority** | P1 |
| **Preconditions** | User is not registered; browser is open on roadmap.sh |
| **Steps** | 1. Navigate to roadmap.sh <br> 2. Click "Sign Up" <br> 3. Enter a valid unique email <br> 4. Enter a valid password (min 8 chars) <br> 5. Click "Create Account" |
| **Expected Result** | Account is created; user is redirected to dashboard or onboarding page |
| **Status** | Pass |

---

### TC-AUTH-002 — Register with already existing email

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-002 |
| **Priority** | P1 |
| **Preconditions** | An account with the target email already exists |
| **Steps** | 1. Navigate to Sign Up page <br> 2. Enter an already-registered email <br> 3. Enter any valid password <br> 4. Click "Create Account" |
| **Expected Result** | Error message displayed: "User already exists with same email.." or similar; account not created |
| **Status** | Pass |

---

### TC-AUTH-003 — Register with invalid email format

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-003 |
| **Priority** | P1 |
| **Preconditions** | User is on Sign Up page |
| **Steps** | 1. Enter malformed email (e.g., "userexample.com", "user@", "@domain.com") <br> 2. Enter valid password <br> 3. Click "Create Account" |
| **Expected Result** | Inline validation error shown; form not submitted |
| **Status** | Pass |

---

### TC-AUTH-004 — Register with weak/short password

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-004 |
| **Priority** | P1 |
| **Preconditions** | User is on Sign Up page |
| **Steps** | 1. Enter valid email <br> 2. Enter a password shorter than minimum requirement (e.g., "abc") <br> 3. Click "Create Account" |
| **Expected Result** | Validation error: "Password too short" or similar; account not created |
| **Status** | Pass |

---

### TC-AUTH-005 — Register with empty fields

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-005 |
| **Priority** | P1 |
| **Preconditions** | User is on Sign Up page |
| **Steps** | 1. Leave email and password fields empty <br> 2. Click "Create Account" |
| **Expected Result** | Validation errors shown for both required fields; form not submitted |
| **Status** | Pass |

---

### TC-AUTH-006 — Login with valid credentials

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-006 |
| **Priority** | P1 |
| **Preconditions** | A registered account exists |
| **Steps** | 1. Navigate to Login page <br> 2. Enter registered email <br> 3. Enter correct password <br> 4. Click "Login" |
| **Expected Result** | User is logged in and redirected to dashboard |
| **Status** | Pass |

---

### TC-AUTH-007 — Login with wrong password

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-007 |
| **Priority** | P1 |
| **Preconditions** | A registered account exists |
| **Steps** | 1. Navigate to Login page <br> 2. Enter registered email <br> 3. Enter incorrect password <br> 4. Click "Login" |
| **Expected Result** | Error message shown: "Invalid credentials" or similar; user not logged in |
| **Status** | Pass |

---

### TC-AUTH-008 — Login with unregistered email

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-008 |
| **Priority** | P1 |
| **Preconditions** | User is on Login page |
| **Steps** | 1. Enter an email that has no account <br> 2. Enter any password <br> 3. Click "Login" |
| **Expected Result** | Error message shown; user not logged in |
| **Status** | Pass |

---

### TC-AUTH-009 — Login with empty fields

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-009 |
| **Priority** | P1 |
| **Preconditions** | User is on Login page |
| **Steps** | 1. Leave email and password fields empty <br> 2. Click "Login" |
| **Expected Result** | Validation errors displayed for both fields; form not submitted |
| **Status** | Pass |

---

### TC-AUTH-010 — Login via GitHub OAuth

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-010 |
| **Priority** | P1 |
| **Preconditions** | User has a valid GitHub account |
| **Steps** | 1. Navigate to Login page <br> 2. Click "Login with GitHub" <br> 3. Authorize on GitHub OAuth page |
| **Expected Result** | User is logged in via GitHub and redirected to dashboard |
| **Status** | pass |

---

### TC-AUTH-011 — Login via Google OAuth

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-011 |
| **Priority** | P1 |
| **Preconditions** | User has a valid Google account |
| **Steps** | 1. Navigate to Login page <br> 2. Click "Login with Google" <br> 3. Authorize on Google OAuth page |
| **Expected Result** | User is logged in via Google and redirected to dashboard |
| **Status** | pass |

---

### TC-AUTH-012 — Logout from active session

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-012 |
| **Priority** | P1 |
| **Preconditions** | User is logged in |
| **Steps** | 1. Click on user avatar/profile menu <br> 2. Click "Logout" |
| **Expected Result** | User is logged out; session is cleared; redirected to homepage or login page |
| **Status** | pass |

---

### TC-AUTH-013 — Session persistence after page refresh

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-013 |
| **Priority** | P2 |
| **Preconditions** | User is logged in |
| **Steps** | 1. Log in successfully <br> 2. Refresh the browser page |
| **Expected Result** | User remains logged in; session is preserved |
| **Status** | pass |

---

### TC-AUTH-014 — Password reset — valid email

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-014 |
| **Priority** | P1 |
| **Preconditions** | Registered account exists |
| **Steps** | 1. Navigate to "Forgot Password" page <br> 2. Enter registered email <br> 3. Click "Send Reset Link" |
| **Expected Result** | Confirmation message shown; password reset email sent |
| **Status** | pass |

---

### TC-AUTH-015 — Password reset — unregistered email

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-015 |
| **Priority** | P2 |
| **Preconditions** | User is on Forgot Password page |
| **Steps** | 1. Enter an email with no registered account <br> 2. Click "Send Reset Link" |
| **Expected Result** | Generic message shown (no account enumeration leak); no email sent |
| **Status** | pass |

---

### TC-AUTH-016 — Password reset link expiry

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-016 |
| **Priority** | P2 |
| **Preconditions** | Password reset email received |
| **Steps** | 1. Wait until the reset link expires (e.g., 24h) <br> 2. Click the expired link |
| **Expected Result** | Error page shown: "Link expired or invalid" |
| **Status** | pass |

---

### TC-AUTH-017 — Set new password via reset link

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-017 |
| **Priority** | P1 |
| **Preconditions** | Valid password reset link received and not expired |
| **Steps** | 1. Click the reset link from email <br> 2. Enter a new valid password <br> 3. Confirm new password <br> 4. Submit |
| **Expected Result** | Password updated successfully; user can log in with new password |
| **Status** | pass |

---

### TC-AUTH-018 — New password matches old password

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-018 |
| **Priority** | P2 |
| **Preconditions** | User is on reset password page via valid link |
| **Steps** | 1. Enter the same password as the previous one <br> 2. Submit |
| **Expected Result** | Error message: "New password must differ from old password" (if enforced) OR password is accepted — document actual behavior |
| **Status** | pass |

---

### TC-AUTH-019 — Password confirmation mismatch

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-019 |
| **Priority** | P1 |
| **Preconditions** | User is on reset or registration page |
| **Steps** | 1. Enter password in first field <br> 2. Enter a different value in confirm password field <br> 3. Submit |
| **Expected Result** | Validation error: "Passwords do not match"; form not submitted |
| **Status** | pass |

---

### TC-AUTH-020 — Access protected page when logged out

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-020 |
| **Priority** | P1 |
| **Preconditions** | User is not logged in |
| **Steps** | 1. Navigate directly to a protected URL (e.g., /settings, /dashboard) |
| **Expected Result** | User is redirected to login page |
| **Status** | pass |

---

### TC-AUTH-021 — Access login page when already logged in

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-021 |
| **Priority** | P2 |
| **Preconditions** | User is already logged in |
| **Steps** | 1. Navigate to /login or /signup URL directly |
| **Expected Result** | User is redirected away (e.g., to dashboard); login page not shown |
| **Status** | pass |

---

### TC-AUTH-022 — SQL injection in login fields

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-022 |
| **Priority** | P1 |
| **Preconditions** | User is on Login page |
| **Steps** | 1. Enter `' OR '1'='1` in email field <br> 2. Enter any value in password <br> 3. Click "Login" |
| **Expected Result** | Login fails; no database error exposed; app handles input safely |
| **Status** | pass |

---

### TC-AUTH-023 — XSS in registration fields

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-023 |
| **Priority** | P1 |
| **Preconditions** | User is on Sign Up page |
| **Steps** | 1. Enter `<script>alert('XSS')</script>` in name or email field <br> 2. Submit the form |
| **Expected Result** | Script is not executed; input is sanitized or rejected |
| **Status** | pass |

---

### TC-AUTH-024 — Brute force protection on login

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-024 |
| **Priority** | P2 |
| **Preconditions** | User is on Login page |
| **Steps** | 1. Attempt login with wrong password 10+ consecutive times |
| **Expected Result** | Account is temporarily locked or CAPTCHA is triggered; rate limiting applied |
| **Status** | pass |

---

### TC-AUTH-025 — Remember me / stay logged in

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-025 |
| **Priority** | P2 |
| **Preconditions** | Login page has "Remember Me" option |
| **Steps** | 1. Log in with "Remember Me" checked <br> 2. Close browser <br> 3. Reopen browser and navigate to roadmap.sh |
| **Expected Result** | User is still logged in without re-entering credentials |
| **Status** | pass |

---

### TC-AUTH-026 — Profile update — change display name

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-026 |
| **Priority** | P2 |
| **Preconditions** | User is logged in and on profile/settings page |
| **Steps** | 1. Navigate to profile settings <br> 2. Update display name <br> 3. Save changes |
| **Expected Result** | Name is updated and reflected across the UI |
| **Status** | pass |

---

### TC-AUTH-027 — Profile update — change email

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-027 |
| **Priority** | P2 |
| **Preconditions** | User is logged in |
| **Steps** | 1. Go to account settings <br> 2. Enter a new valid email <br> 3. Save |
| **Expected Result** | Confirmation email sent to new address; email updated after verification |
| **Status** | pass |

---

### TC-AUTH-028 — Delete account

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-028 |
| **Priority** | P2 |
| **Preconditions** | User is logged in and on account settings |
| **Steps** | 1. Navigate to account deletion option <br> 2. Confirm deletion (type confirmation text or click confirm) |
| **Expected Result** | Account is deleted; user is logged out; data is cleared |
| **Status** | pass |

---

### TC-AUTH-029 — Token expiry — automatic logout

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-029 |
| **Priority** | P2 |
| **Preconditions** | User is logged in; session token has an expiry |
| **Steps** | 1. Leave session idle past token expiry time <br> 2. Try to perform an authenticated action |
| **Expected Result** | User is redirected to login; session expired message shown |
| **Status** | pass |

---

### TC-AUTH-030 — Multi-device logout (logout all sessions)

| Field | Details |
|---|---|
| **TC-ID** | TC-AUTH-030 |
| **Priority** | P3 |
| **Preconditions** | User is logged in on multiple devices/browsers |
| **Steps** | 1. Navigate to Security settings <br> 2. Click "Logout of all sessions" (if available) |
| **Expected Result** | All active sessions are terminated; user must log in again on all devices |
| **Status** | pass |
