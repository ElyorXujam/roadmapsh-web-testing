# TC-PROGRESS — Progress Tracking Test Cases
> Module: User Progress Tracking | Total: 20 Test Cases

---

## Legend

| Field | Description |
|---|---|
| **TC-ID** | Unique test case identifier |
| **Priority** | P1 / P2 / P3 |
| **Preconditions** | State required before executing steps |
| **Steps** | Numbered actions to perform |
| **Expected Result** | What should happen |
| **Status** | Pass / Fail / Blocked / Not Run |

---

### TC-PROGRESS-001 — Progress percentage updates when topic is marked Done

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-001 |
| **Priority** | P1 |
| **Preconditions** | User is logged in; roadmap is open with no topics completed |
| **Steps** | 1. Note current progress percentage <br> 2. Mark one topic as "Done" |
| **Expected Result** | Progress percentage increases proportionally |
| **Status** | Not Run |

---

### TC-PROGRESS-002 — Progress persists after logout and login

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-002 |
| **Priority** | P1 |
| **Preconditions** | User is logged in with some topics marked |
| **Steps** | 1. Mark several topics as Done <br> 2. Log out <br> 3. Log back in <br> 4. Open the same roadmap |
| **Expected Result** | All previously marked topics remain in their saved state |
| **Status** | Not Run |

---

### TC-PROGRESS-003 — Progress persists after browser refresh

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-003 |
| **Priority** | P1 |
| **Preconditions** | User is logged in; topics have been marked |
| **Steps** | 1. Mark a topic as Done <br> 2. Refresh the page |
| **Expected Result** | Topic still shows as Done after refresh |
| **Status** | Not Run |

---

### TC-PROGRESS-004 — Unmarking a topic reduces progress

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-004 |
| **Priority** | P1 |
| **Preconditions** | User is logged in; at least one topic is marked Done |
| **Steps** | 1. Note current progress percentage <br> 2. Click a Done topic <br> 3. Unmark / reset its status |
| **Expected Result** | Progress percentage decreases; node returns to default state |
| **Status** | Not Run |

---

### TC-PROGRESS-005 — Progress bar reflects correct percentage on dashboard

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-005 |
| **Priority** | P2 |
| **Preconditions** | User is logged in and has progress on at least one roadmap |
| **Steps** | 1. Navigate to user dashboard <br> 2. View progress bars for enrolled roadmaps |
| **Expected Result** | Progress bar percentage matches actual topic completion ratio |
| **Status** | Not Run |

---

### TC-PROGRESS-006 — Multiple roadmaps tracked independently

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-006 |
| **Priority** | P1 |
| **Preconditions** | User is logged in |
| **Steps** | 1. Mark topics in Frontend roadmap <br> 2. Open Backend roadmap <br> 3. Check progress |
| **Expected Result** | Backend roadmap shows 0% or its own independent progress; Frontend progress not mixed in |
| **Status** | Not Run |

---

### TC-PROGRESS-007 — Reset progress for a roadmap

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-007 |
| **Priority** | P2 |
| **Preconditions** | User is logged in with roadmap partially completed |
| **Steps** | 1. Find "Reset Progress" option (settings or roadmap menu) <br> 2. Confirm reset |
| **Expected Result** | All topics reset to default; progress drops to 0% |
| **Status** | Not Run |

---

### TC-PROGRESS-008 — "In Progress" topics counted separately from "Done"

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-008 |
| **Priority** | P2 |
| **Preconditions** | User is logged in; roadmap has topics in different states |
| **Steps** | 1. Mark some topics as Done, some as In Progress <br> 2. Check progress stats |
| **Expected Result** | Done and In Progress are displayed as separate counts or categories |
| **Status** | Not Run |

---

### TC-PROGRESS-009 — 100% completion state displayed correctly

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-009 |
| **Priority** | P2 |
| **Preconditions** | User is logged in on a roadmap |
| **Steps** | 1. Mark all topics as Done |
| **Expected Result** | Progress shows 100%; a completion message or badge may appear |
| **Status** | Not Run |

---

### TC-PROGRESS-010 — Progress visible on user profile page

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-010 |
| **Priority** | P2 |
| **Preconditions** | User is logged in with progress on roadmaps |
| **Steps** | 1. Navigate to public profile or settings page |
| **Expected Result** | Roadmap progress is displayed on profile (if feature exists) |
| **Status** | Not Run |

---

### TC-PROGRESS-011 — Progress not visible to other users (privacy)

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-011 |
| **Priority** | P2 |
| **Preconditions** | User A has progress; User B views User A's profile |
| **Steps** | 1. Log in as User B <br> 2. Visit User A's public profile URL |
| **Expected Result** | Only publicly shared progress is visible; private progress is hidden |
| **Status** | Not Run |

---

### TC-PROGRESS-012 — Topics marked via keyboard are saved

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-012 |
| **Priority** | P3 |
| **Preconditions** | User is logged in; roadmap open |
| **Steps** | 1. Navigate to a node using keyboard <br> 2. Mark as Done using keyboard/Enter |
| **Expected Result** | Topic status saved correctly via keyboard interaction |
| **Status** | Not Run |

---

### TC-PROGRESS-013 — Correct topic count shown in progress stats

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-013 |
| **Priority** | P2 |
| **Preconditions** | User has marked N topics as done |
| **Steps** | 1. Open roadmap <br> 2. View progress stats area |
| **Expected Result** | "X of Y topics completed" shows correct numbers matching actual marks |
| **Status** | Not Run |

---

### TC-PROGRESS-014 — Skipped topics do not inflate progress

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-014 |
| **Priority** | P2 |
| **Preconditions** | User is logged in on a roadmap |
| **Steps** | 1. Mark several topics as "Skipped" <br> 2. Check progress percentage |
| **Expected Result** | Skipped topics are not counted as completed; percentage is not inflated |
| **Status** | Not Run |

---

### TC-PROGRESS-015 — Progress syncs across two browser tabs

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-015 |
| **Priority** | P3 |
| **Preconditions** | User is logged in; same roadmap open in two tabs |
| **Steps** | 1. Mark a topic as Done in Tab 1 <br> 2. Switch to Tab 2 <br> 3. Refresh Tab 2 |
| **Expected Result** | Updated progress is reflected in Tab 2 after refresh |
| **Status** | Not Run |

---

### TC-PROGRESS-016 — Progress is not tracked for logged-out users

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-016 |
| **Priority** | P1 |
| **Preconditions** | User is NOT logged in |
| **Steps** | 1. Open a roadmap <br> 2. Attempt to mark a topic |
| **Expected Result** | User prompted to log in; no progress recorded |
| **Status** | Not Run |

---

### TC-PROGRESS-017 — Roadmap progress shown on homepage/dashboard card

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-017 |
| **Priority** | P2 |
| **Preconditions** | User is logged in with some roadmap progress |
| **Steps** | 1. Navigate to homepage or dashboard |
| **Expected Result** | Roadmap cards display current progress percentage for the logged-in user |
| **Status** | Not Run |

---

### TC-PROGRESS-018 — Progress export or share feature (if available)

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-018 |
| **Priority** | P3 |
| **Preconditions** | User is logged in with some roadmap progress |
| **Steps** | 1. Look for "Share Progress" or export option <br> 2. Generate a shareable link or image |
| **Expected Result** | Share link or image generated correctly reflecting actual progress |
| **Status** | Not Run |

---

### TC-PROGRESS-019 — Progress API response is correct (if testable)

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-019 |
| **Priority** | P3 |
| **Preconditions** | Tester has access to browser DevTools network tab; user is logged in |
| **Steps** | 1. Mark a topic <br> 2. Inspect network request for progress update API <br> 3. Check request payload and response |
| **Expected Result** | API request is sent with correct topic ID and status; response is 200 OK |
| **Status** | Not Run |

---

### TC-PROGRESS-020 — Bulk mark all topics as Done

| Field | Details |
|---|---|
| **TC-ID** | TC-PROGRESS-020 |
| **Priority** | P3 |
| **Preconditions** | User is logged in; "Mark all as done" option exists (if applicable) |
| **Steps** | 1. Open roadmap <br> 2. Use bulk "Mark All Done" option |
| **Expected Result** | All topics marked as Done; progress jumps to 100% |
| **Status** | Not Run |
