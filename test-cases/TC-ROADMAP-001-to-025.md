# TC-ROADMAP — Roadmap Browsing & Viewing Test Cases
> Module: Roadmap Content & Navigation | Total: 25 Test Cases

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

### TC-ROADMAP-001 — Homepage displays list of roadmaps

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-001 |
| **Priority** | P1 |
| **Preconditions** | User is on roadmap.sh homepage (logged in or out) |
| **Steps** | 1. Navigate to roadmap.sh |
| **Expected Result** | A list/grid of available roadmaps is displayed (e.g., Frontend, Backend, DevOps) |
| **Status** | Not Run |

---

### TC-ROADMAP-002 — Open a roadmap by clicking its card

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-002 |
| **Priority** | P1 |
| **Preconditions** | User is on homepage |
| **Steps** | 1. Click on any roadmap card (e.g., "Frontend Developer") |
| **Expected Result** | Roadmap opens; interactive diagram/flowchart is visible |
| **Status** | Not Run |

---

### TC-ROADMAP-003 — Roadmap nodes are clickable

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-003 |
| **Priority** | P1 |
| **Preconditions** | A roadmap is open |
| **Steps** | 1. Click on any topic node (e.g., "HTML") |
| **Expected Result** | A detail panel or popup opens with description, links, or resources for that topic |
| **Status** | Not Run |

---

### TC-ROADMAP-004 — Roadmap loads completely without errors

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-004 |
| **Priority** | P1 |
| **Preconditions** | User navigates to a specific roadmap URL |
| **Steps** | 1. Open any roadmap page <br> 2. Check browser console for errors <br> 3. Verify all nodes and connections render |
| **Expected Result** | Page loads fully; no broken nodes; no console errors |
| **Status** | Not Run |

---

### TC-ROADMAP-005 — Roadmap zoom in/out functionality

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-005 |
| **Priority** | P2 |
| **Preconditions** | A roadmap is open |
| **Steps** | 1. Use mouse scroll wheel or zoom controls to zoom in <br> 2. Zoom out |
| **Expected Result** | Roadmap scales smoothly; content remains readable; layout preserved |
| **Status** | Not Run |

---

### TC-ROADMAP-006 — Roadmap pan/drag navigation

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-006 |
| **Priority** | P2 |
| **Preconditions** | A roadmap is open and larger than viewport |
| **Steps** | 1. Click and drag the roadmap canvas |
| **Expected Result** | Roadmap pans smoothly in the dragged direction |
| **Status** | Not Run |

---

### TC-ROADMAP-007 — Mark a topic as "Done"

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-007 |
| **Priority** | P1 |
| **Preconditions** | User is logged in; roadmap is open |
| **Steps** | 1. Click a topic node <br> 2. Click "Mark as Done" |
| **Expected Result** | Node is visually marked as done (e.g., green highlight); progress updates |
| **Status** | Not Run |

---

### TC-ROADMAP-008 — Mark a topic as "In Progress"

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-008 |
| **Priority** | P1 |
| **Preconditions** | User is logged in; roadmap is open |
| **Steps** | 1. Click a topic node <br> 2. Select "In Progress" status |
| **Expected Result** | Node is visually updated to "In Progress" state |
| **Status** | Not Run |

---

### TC-ROADMAP-009 — Mark a topic as "Skipped"

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-009 |
| **Priority** | P2 |
| **Preconditions** | User is logged in; roadmap is open |
| **Steps** | 1. Click a topic node <br> 2. Select "Skip" or "Skipped" |
| **Expected Result** | Node is visually updated to skipped state |
| **Status** | Not Run |

---

### TC-ROADMAP-010 — Topic detail panel contains resources/links

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-010 |
| **Priority** | P2 |
| **Preconditions** | A roadmap node is clicked and panel is open |
| **Steps** | 1. Open a topic detail panel <br> 2. Verify links, articles, or videos are listed |
| **Expected Result** | Resources are visible and links are functional |
| **Status** | Not Run |

---

### TC-ROADMAP-011 — External resource links open in new tab

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-011 |
| **Priority** | P2 |
| **Preconditions** | Topic detail panel is open with external links |
| **Steps** | 1. Click an external resource link |
| **Expected Result** | Link opens in a new browser tab; user remains on roadmap.sh |
| **Status** | Not Run |

---

### TC-ROADMAP-012 — Roadmap breadcrumb/back navigation

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-012 |
| **Priority** | P2 |
| **Preconditions** | User is on a specific roadmap page |
| **Steps** | 1. Use breadcrumb or back button to navigate to homepage |
| **Expected Result** | User is taken back to the roadmap list without losing session |
| **Status** | Not Run |

---

### TC-ROADMAP-013 — Share roadmap via link

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-013 |
| **Priority** | P2 |
| **Preconditions** | User is on a roadmap page |
| **Steps** | 1. Click "Share" button (if available) <br> 2. Copy the generated link <br> 3. Open link in incognito window |
| **Expected Result** | Roadmap is accessible via the shared link; read-only view shown for non-logged-in users |
| **Status** | Not Run |

---

### TC-ROADMAP-014 — Download roadmap as image/PDF

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-014 |
| **Priority** | P3 |
| **Preconditions** | User is on a roadmap page with download option |
| **Steps** | 1. Click download icon or button <br> 2. Select format (PNG or PDF if applicable) |
| **Expected Result** | File downloads successfully with proper roadmap content |
| **Status** | Not Run |

---

### TC-ROADMAP-015 — Roadmap page title and metadata correct

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-015 |
| **Priority** | P3 |
| **Preconditions** | User opens a roadmap page |
| **Steps** | 1. Check browser tab title <br> 2. Inspect meta tags in page source |
| **Expected Result** | Page title matches roadmap name; meta description present and relevant |
| **Status** | Not Run |

---

### TC-ROADMAP-016 — Roadmap URL structure is correct

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-016 |
| **Priority** | P2 |
| **Preconditions** | User clicks on a roadmap |
| **Steps** | 1. Click "Frontend Developer" roadmap <br> 2. Note the URL |
| **Expected Result** | URL follows expected pattern (e.g., /roadmaps/frontend) |
| **Status** | Not Run |

---

### TC-ROADMAP-017 — Switching between multiple roadmaps

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-017 |
| **Priority** | P2 |
| **Preconditions** | User is logged in |
| **Steps** | 1. Open Frontend roadmap <br> 2. Navigate back <br> 3. Open Backend roadmap |
| **Expected Result** | Each roadmap loads independently; no data bleed between roadmaps |
| **Status** | Not Run |

---

### TC-ROADMAP-018 — Progress is not saved for logged-out users

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-018 |
| **Priority** | P1 |
| **Preconditions** | User is NOT logged in |
| **Steps** | 1. Open a roadmap <br> 2. Click "Mark as Done" on a topic |
| **Expected Result** | Prompt to log in appears; progress not saved without authentication |
| **Status** | Not Run |

---

### TC-ROADMAP-019 — Roadmap renders correctly on tablet screen

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-019 |
| **Priority** | P2 |
| **Preconditions** | Device or emulator set to tablet viewport (~768px) |
| **Steps** | 1. Open a roadmap on tablet viewport |
| **Expected Result** | Roadmap is visible and navigable; no overflow or clipping |
| **Status** | Not Run |

---

### TC-ROADMAP-020 — Roadmap renders correctly on mobile screen

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-020 |
| **Priority** | P2 |
| **Preconditions** | Device or emulator set to mobile viewport (~375px) |
| **Steps** | 1. Open a roadmap on mobile viewport |
| **Expected Result** | Roadmap adapts to mobile; scroll and zoom functional |
| **Status** | Not Run |

---

### TC-ROADMAP-021 — All official roadmaps are listed on homepage

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-021 |
| **Priority** | P2 |
| **Preconditions** | User is on homepage |
| **Steps** | 1. View all roadmap cards listed <br> 2. Compare with roadmap.sh documentation/known list |
| **Expected Result** | All published roadmaps are present; none missing |
| **Status** | Not Run |

---

### TC-ROADMAP-022 — 404 page for invalid roadmap URL

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-022 |
| **Priority** | P2 |
| **Preconditions** | User is browsing the site |
| **Steps** | 1. Navigate to a non-existent roadmap URL (e.g., /roadmaps/invalidroadmap123) |
| **Expected Result** | 404 page displayed; no server error; navigation links available |
| **Status** | Not Run |

---

### TC-ROADMAP-023 — Keyboard navigation through roadmap nodes

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-023 |
| **Priority** | P3 |
| **Preconditions** | Roadmap is open |
| **Steps** | 1. Use Tab key to navigate between interactive nodes <br> 2. Press Enter to open a node |
| **Expected Result** | Nodes are focusable and operable via keyboard |
| **Status** | Not Run |

---

### TC-ROADMAP-024 — Topic panel closes on outside click or Escape key

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-024 |
| **Priority** | P2 |
| **Preconditions** | Topic detail panel is open |
| **Steps** | 1. Click outside the panel OR press Escape key |
| **Expected Result** | Panel closes; user returns to roadmap view |
| **Status** | Not Run |

---

### TC-ROADMAP-025 — Roadmap content is up to date

| Field | Details |
|---|---|
| **TC-ID** | TC-ROADMAP-025 |
| **Priority** | P3 |
| **Preconditions** | Tester has reference to latest roadmap.sh GitHub content |
| **Steps** | 1. Open a roadmap on the site <br> 2. Compare nodes and topics against GitHub source |
| **Expected Result** | Roadmap content matches the latest published version |
| **Status** | Not Run |
