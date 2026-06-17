# TC-SEARCH — Search Functionality Test Cases
> Module: Site Search | Total: 15 Test Cases

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

### TC-SEARCH-001 — Search for a valid roadmap by name

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-001 |
| **Priority** | P1 |
| **Preconditions** | User is on roadmap.sh (logged in or out) |
| **Steps** | 1.Navigate to Community Roadmaps in Roadmap menu 2. Click search icon or focus search bar <br> 3. Type "backend" |
| **Expected Result** | Search results include "Backend" roadmap |
| **Status** | pass |

---

### TC-SEARCH-002 — Search with partial keyword

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-002 |
| **Priority** | P1 |
| **Preconditions** | Search bar is accessible |
| **Steps** | 1. Type "back" in search bar |
| **Expected Result** | Results matching "back" appear (e.g., backend roadmap) |
| **Status** | pass |

---

### TC-SEARCH-003 — Search with exact topic keyword

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-003 |
| **Priority** | P1 |
| **Preconditions** | Search bar is accessible |
| **Steps** | 1. Type "Docker" in search bar |
| **Expected Result** | Roadmaps or topics containing "Docker" are returned |
| **Status** | fail |

---

### TC-SEARCH-004 — Search with no results

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-004 |
| **Priority** | P1 |
| **Preconditions** | Search bar is accessible |
| **Steps** | 1. Type a nonsense query (e.g., "xyzabc123qwerty") |
| **Expected Result** | "No results found" message displayed; no broken UI |
| **Status** | pass |

---

### TC-SEARCH-005 — Search is case-insensitive

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-005 |
| **Priority** | P2 |
| **Preconditions** | Search bar is accessible |
| **Steps** | 1. Search "frontend" (lowercase) <br> 2. Search "FRONTEND" (uppercase) <br> 3. Compare results |
| **Expected Result** | Both queries return the same results |
| **Status** | pass |

---

### TC-SEARCH-006 — Search input with special characters

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-006 |
| **Priority** | P2 |
| **Preconditions** | Search bar is accessible |
| **Steps** | 1. Enter special characters in search: `<>{}[]!@#$%` |
| **Expected Result** | No crash or error; empty results or sanitized query handled gracefully |
| **Status** | fail |

---

### TC-SEARCH-007 — Search with only spaces

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-007 |
| **Priority** | P2 |
| **Preconditions** | Search bar is accessible |
| **Steps** | 1. Type only spaces in search field <br> 2. Submit or observe results |
| **Expected Result** | No results shown or search not submitted; no server error |
| **Status** | pass |

---

### TC-SEARCH-008 — Search result links navigate to correct page

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-008 |
| **Priority** | P1 |
| **Preconditions** | Search returns results |
| **Steps** | 1. Search for "Backend" <br> 2. Click the first result |
| **Expected Result** | User is taken to the correct roadmap or content page |
| **Status** | pass |

---

### TC-SEARCH-009 — Search keyboard shortcut works

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-009 |
| **Priority** | P2 |
| **Preconditions** | User is on any page of roadmap.sh |
| **Steps** | 1. Press the search keyboard shortcut (e.g., "/" or Ctrl+K) |
| **Expected Result** | Search bar is focused and ready for input |
| **Status** | Not Run |

---

### TC-SEARCH-010 — Search autocomplete/suggestions appear

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-010 |
| **Priority** | P2 |
| **Preconditions** | Search bar is focused |
| **Steps** | 1. Begin typing "Dev" |
| **Expected Result** | Dropdown suggestions appear as the user types |
| **Status** | fail |

---

### TC-SEARCH-011 — Pressing Escape closes search

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-011 |
| **Priority** | P2 |
| **Preconditions** | Search bar is open and focused |
| **Steps** | 1. Press Escape key |
| **Expected Result** | Search bar or dropdown closes; user returns to normal view |
| **Status** | fail |

---

### TC-SEARCH-012 — Very long search query handled

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-013 |
| **Priority** | P3 |
| **Preconditions** | Search bar is accessible |
| **Steps** | 1. Paste 500+ characters into the search field <br> 2. Submit |
| **Expected Result** | Input is truncated or handled gracefully; no crash or server error |
| **Status** | fail |

---

### TC-SEARCH-013 — Search results highlight matching keyword

| Field | Details |
|---|---|
| **TC-ID** | TC-SEARCH-014 |
| **Priority** | P3 |
| **Preconditions** | Search returns results |
| **Steps** | 1. Search for "Python" <br> 2. Inspect result items |
| **Expected Result** | The word "Python" is highlighted or bolded in each result item |
| **Status** | fail |