# TC-CUSTOM-ROADMAP — Custom Roadmap Test Cases
> Module: Custom Roadmap Creation & Management | Total: 20 Test Cases

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

### TC-CUSTOM-001 — Create a new custom roadmap

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-001 |
| **Priority** | P1 |
| **Preconditions** | User is logged in |
| **Steps** | 1. Navigate to "Custom Roadmap" or "Create Roadmap" option <br> 2. Enter a title <br> 3. Click "Create" |
| **Expected Result** | New custom roadmap is created and opens in editor |
| **Status** | Not Run |

---

### TC-CUSTOM-002 — Add a node to custom roadmap

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-002 |
| **Priority** | P1 |
| **Preconditions** | User is in custom roadmap editor |
| **Steps** | 1. Click "Add Node" or drag a node onto the canvas <br> 2. Enter node label |
| **Expected Result** | Node is added to the roadmap canvas with the entered label |
| **Status** | Not Run |

---

### TC-CUSTOM-003 — Edit an existing node label

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-003 |
| **Priority** | P1 |
| **Preconditions** | Custom roadmap has at least one node |
| **Steps** | 1. Double-click or right-click a node <br> 2. Edit the label text <br> 3. Confirm/save |
| **Expected Result** | Node label updates to the new text |
| **Status** | Not Run |

---

### TC-CUSTOM-004 — Delete a node from custom roadmap

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-004 |
| **Priority** | P1 |
| **Preconditions** | Custom roadmap has at least one node |
| **Steps** | 1. Select a node <br> 2. Press Delete key or use delete option |
| **Expected Result** | Node is removed from canvas; connected edges also removed |
| **Status** | Not Run |

---

### TC-CUSTOM-005 — Connect two nodes with an edge

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-005 |
| **Priority** | P1 |
| **Preconditions** | Custom roadmap has at least two nodes |
| **Steps** | 1. Hover over a source node <br> 2. Drag from the connection point to a target node |
| **Expected Result** | An arrow/edge is drawn connecting the two nodes |
| **Status** | Not Run |

---

### TC-CUSTOM-006 — Delete an edge between nodes

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-006 |
| **Priority** | P2 |
| **Preconditions** | Custom roadmap has connected nodes |
| **Steps** | 1. Click on an edge/arrow <br> 2. Press Delete or use context menu |
| **Expected Result** | Edge is removed; nodes remain intact |
| **Status** | Not Run |

---

### TC-CUSTOM-007 — Save custom roadmap

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-007 |
| **Priority** | P1 |
| **Preconditions** | User is editing a custom roadmap |
| **Steps** | 1. Make changes to the roadmap <br> 2. Click "Save" |
| **Expected Result** | Changes are saved; success confirmation shown |
| **Status** | Not Run |

---

### TC-CUSTOM-008 — Custom roadmap auto-saves

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-008 |
| **Priority** | P2 |
| **Preconditions** | User is editing a custom roadmap with auto-save enabled |
| **Steps** | 1. Add or modify a node <br> 2. Wait a few seconds without clicking Save |
| **Expected Result** | "Auto-saved" indicator appears; changes persist after refresh |
| **Status** | Not Run |

---

### TC-CUSTOM-009 — Rename a custom roadmap

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-009 |
| **Priority** | P2 |
| **Preconditions** | User has a custom roadmap |
| **Steps** | 1. Navigate to roadmap settings or title field <br> 2. Change the title <br> 3. Save |
| **Expected Result** | Roadmap is renamed; new title shown in list and editor |
| **Status** | Not Run |

---

### TC-CUSTOM-010 — Delete a custom roadmap

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-010 |
| **Priority** | P1 |
| **Preconditions** | User has at least one custom roadmap |
| **Steps** | 1. Navigate to custom roadmap list <br> 2. Select a roadmap <br> 3. Click "Delete" and confirm |
| **Expected Result** | Roadmap is permanently deleted; no longer appears in list |
| **Status** | Not Run |

---

### TC-CUSTOM-011 — Custom roadmap listed in user dashboard

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-011 |
| **Priority** | P2 |
| **Preconditions** | User has created at least one custom roadmap |
| **Steps** | 1. Navigate to dashboard or "My Roadmaps" section |
| **Expected Result** | Custom roadmap appears in the list with correct title |
| **Status** | Not Run |

---

### TC-CUSTOM-012 — Share custom roadmap with public link

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-012 |
| **Priority** | P2 |
| **Preconditions** | User is in custom roadmap editor |
| **Steps** | 1. Click "Share" or "Make Public" option <br> 2. Copy generated URL <br> 3. Open URL in incognito window |
| **Expected Result** | Roadmap is viewable by unauthenticated users in read-only mode |
| **Status** | Not Run |

---

### TC-CUSTOM-013 — Private custom roadmap not accessible by others

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-013 |
| **Priority** | P1 |
| **Preconditions** | Custom roadmap is set to private |
| **Steps** | 1. Copy the roadmap URL <br> 2. Log in as a different user or open incognito <br> 3. Navigate to the URL |
| **Expected Result** | Access denied; roadmap not visible to other users |
| **Status** | Not Run |

---

### TC-CUSTOM-014 — Undo last action in editor

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-014 |
| **Priority** | P2 |
| **Preconditions** | User is in custom roadmap editor and has made changes |
| **Steps** | 1. Add a node <br> 2. Press Ctrl+Z (or click Undo) |
| **Expected Result** | Last action is undone; node is removed |
| **Status** | Not Run |

---

### TC-CUSTOM-015 — Redo action in editor

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-015 |
| **Priority** | P2 |
| **Preconditions** | User has undone an action in the editor |
| **Steps** | 1. After undoing, press Ctrl+Y or Redo |
| **Expected Result** | Undone action is reapplied |
| **Status** | Not Run |

---

### TC-CUSTOM-016 — Node repositioning via drag and drop

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-016 |
| **Priority** | P2 |
| **Preconditions** | Custom roadmap editor is open with nodes |
| **Steps** | 1. Click and drag a node to a new position |
| **Expected Result** | Node moves to new position; connected edges follow |
| **Status** | Not Run |

---

### TC-CUSTOM-017 — Create roadmap without a title

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-017 |
| **Priority** | P2 |
| **Preconditions** | User is on create roadmap screen |
| **Steps** | 1. Leave the title field empty <br> 2. Click "Create" |
| **Expected Result** | Validation error shown: "Title is required"; roadmap not created |
| **Status** | Not Run |

---

### TC-CUSTOM-018 — Custom roadmap with maximum nodes

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-018 |
| **Priority** | P3 |
| **Preconditions** | User is in custom roadmap editor |
| **Steps** | 1. Add nodes repeatedly until a limit is reached or performance degrades |
| **Expected Result** | Roadmap handles large number of nodes; or limit error shown gracefully |
| **Status** | Not Run |

---

### TC-CUSTOM-019 — Duplicate a custom roadmap

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-019 |
| **Priority** | P3 |
| **Preconditions** | User has an existing custom roadmap |
| **Steps** | 1. Navigate to roadmap options <br> 2. Click "Duplicate" or "Clone" (if available) |
| **Expected Result** | A copy of the roadmap is created with a modified title (e.g., "Copy of...") |
| **Status** | Not Run |

---

### TC-CUSTOM-020 — Custom roadmap editor accessible on mobile

| Field | Details |
|---|---|
| **TC-ID** | TC-CUSTOM-020 |
| **Priority** | P2 |
| **Preconditions** | Device or emulator set to mobile viewport |
| **Steps** | 1. Navigate to custom roadmap editor on mobile <br> 2. Try to add and connect nodes |
| **Expected Result** | Editor is usable on mobile; touch interactions work; no critical UI breakage |
| **Status** | Not Run |
