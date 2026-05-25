# TC-UI — UI/UX & Visual Testing Test Cases
> Module: UI/UX & Visual Testing | Total: 30 Test Cases
> Reference: Chapter 5 — UI/UX & Visual Testing

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

## 5.2 Consistency Checks

### TC-UI-001 — Typography is consistent across pages

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-001 |
| **Priority** | P2 |
| **Preconditions** | User is on roadmap.sh |
| **Steps** | 1. Open Homepage <br> 2. Open a Roadmap page <br> 3. Open Profile/Settings page <br> 4. Compare heading, body, and caption font sizes across all three |
| **Expected Result** | Font sizes for headings, body text, and captions are visually consistent across all pages |
| **Status** | Not Run |

---

### TC-UI-002 — Button colors are consistent across pages

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-002 |
| **Priority** | P2 |
| **Preconditions** | User is browsing multiple pages |
| **Steps** | 1. Identify primary CTA buttons on Homepage, Login, Roadmap, and Profile pages <br> 2. Compare color, style, and size |
| **Expected Result** | Primary buttons use the same color scheme on all pages; no inconsistencies |
| **Status** | Not Run |

---

### TC-UI-003 — Error state color is consistently red

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-003 |
| **Priority** | P2 |
| **Preconditions** | User is on Login and Registration pages |
| **Steps** | 1. Trigger a validation error on the Login form <br> 2. Trigger a validation error on the Registration form <br> 3. Compare error message color and style |
| **Expected Result** | Error messages use the same red color, icon, and position on both forms |
| **Status** | Not Run |

---

### TC-UI-004 — Success state color is consistently green

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-004 |
| **Priority** | P2 |
| **Preconditions** | User is logged in and can mark roadmap topics |
| **Steps** | 1. Mark a topic as "Done" <br> 2. Observe success indicator color <br> 3. Compare with any other success state on the site (e.g., saved profile) |
| **Expected Result** | All success states use the same green color consistently |
| **Status** | Not Run |

---

### TC-UI-005 — Card spacing and padding is uniform

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-005 |
| **Priority** | P2 |
| **Preconditions** | User is on pages that display cards (roadmap list, custom roadmaps, guides) |
| **Steps** | 1. Open the roadmap list page <br> 2. Open the custom roadmap list <br> 3. Open the guides list (if available) <br> 4. Compare card padding and spacing between cards |
| **Expected Result** | Cards across all listing pages have uniform internal padding and consistent gap between cards |
| **Status** | Not Run |

---

### TC-UI-006 — Main navigation is identical on all pages

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-006 |
| **Priority** | P1 |
| **Preconditions** | User navigates between multiple pages |
| **Steps** | 1. Visit Homepage, a roadmap page, settings page, and profile page <br> 2. Compare the navigation bar on each |
| **Expected Result** | Navigation bar looks and behaves identically on every page — same links, same layout |
| **Status** | Not Run |

---

### TC-UI-007 — Primary, secondary, and destructive buttons are visually distinct

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-007 |
| **Priority** | P2 |
| **Preconditions** | User is browsing the site |
| **Steps** | 1. Identify a primary button (e.g., "Save"), a secondary button (e.g., "Cancel"), and a destructive button (e.g., "Delete") across the site <br> 2. Compare their visual styles |
| **Expected Result** | All three button types are visually distinct from each other; each type is consistent with itself across pages |
| **Status** | Not Run |

---

### TC-UI-008 — Error messages are consistently styled across all forms

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-008 |
| **Priority** | P2 |
| **Preconditions** | User can trigger errors on multiple forms |
| **Steps** | 1. Trigger error on Login form <br> 2. Trigger error on Registration form <br> 3. Trigger error on Profile Update form <br> 4. Compare error message color, icon, and position |
| **Expected Result** | All error messages share the same color, icon style, and placement pattern |
| **Status** | Not Run |

---

### TC-UI-009 — Loading states are consistent across async content

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-009 |
| **Priority** | P2 |
| **Preconditions** | User is browsing pages with async content (roadmaps, profile) |
| **Steps** | 1. Observe loading state on roadmap page load <br> 2. Observe loading state on any form submission <br> 3. Compare spinners/skeletons |
| **Expected Result** | Loading indicators are visually consistent — same spinner style or skeleton pattern |
| **Status** | Not Run |

---

### TC-UI-010 — Icons are from the same family and weight

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-010 |
| **Priority** | P3 |
| **Preconditions** | User is browsing navigation, roadmap nodes, and profile area |
| **Steps** | 1. Inspect icons in the navigation bar <br> 2. Inspect icons in roadmap topic nodes <br> 3. Inspect icons in the profile area |
| **Expected Result** | All icons share the same visual family (e.g., all outlined or all filled); no mismatched icon styles |
| **Status** | Not Run |

---

## 5.3 Dark Mode Testing

### TC-UI-011 — Dark mode toggle switches entire page

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-011 |
| **Priority** | P1 |
| **Preconditions** | User is on roadmap.sh in light mode |
| **Steps** | 1. Click the dark/light mode toggle |
| **Expected Result** | Entire page switches to dark mode; no white patches or elements left in light mode |
| **Status** | Not Run |

---

### TC-UI-012 — Dark mode persists on page navigation

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-012 |
| **Priority** | P1 |
| **Preconditions** | User has enabled dark mode |
| **Steps** | 1. Enable dark mode <br> 2. Navigate to a different page (e.g., from Homepage to a roadmap) |
| **Expected Result** | New page loads in dark mode immediately; no white flash on transition |
| **Status** | Not Run |

---

### TC-UI-013 — Text contrast is readable in dark mode

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-013 |
| **Priority** | P1 |
| **Preconditions** | Dark mode is enabled |
| **Steps** | 1. Enable dark mode <br> 2. Browse Homepage, a roadmap page, and settings page <br> 3. Check all text elements for readability |
| **Expected Result** | All text is clearly readable against the dark background; no low-contrast text |
| **Status** | Not Run |

---

### TC-UI-014 — Images and icons display correctly in dark mode

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-014 |
| **Priority** | P2 |
| **Preconditions** | Dark mode is enabled |
| **Steps** | 1. Enable dark mode <br> 2. Inspect images, logos, and icons on the page |
| **Expected Result** | Images and icons look correct; no white background halos or incorrect colors on icons |
| **Status** | Not Run |

---

### TC-UI-015 — Form inputs are readable in dark mode

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-015 |
| **Priority** | P1 |
| **Preconditions** | Dark mode is enabled |
| **Steps** | 1. Enable dark mode <br> 2. Navigate to Login or Registration form <br> 3. Inspect placeholders, field labels, and typed input text |
| **Expected Result** | Placeholder text, labels, and user input are all clearly readable in dark mode |
| **Status** | Not Run |

---

### TC-UI-016 — Dark mode preference persists on page reload

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-016 |
| **Priority** | P1 |
| **Preconditions** | Dark mode is enabled |
| **Steps** | 1. Enable dark mode <br> 2. Press F5 to reload the page |
| **Expected Result** | Page reloads in dark mode; preference is not lost on refresh |
| **Status** | Not Run |

---

### TC-UI-017 — Dark mode preference persists after closing and reopening browser

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-017 |
| **Priority** | P2 |
| **Preconditions** | Dark mode is enabled |
| **Steps** | 1. Enable dark mode <br> 2. Close the browser completely <br> 3. Reopen browser and navigate to roadmap.sh |
| **Expected Result** | Site loads in dark mode; user preference is remembered across browser sessions |
| **Status** | Not Run |

---

## 5.4 Typography & Readability Testing

### TC-UI-018 — No text is cut off or unexpectedly truncated

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-018 |
| **Priority** | P2 |
| **Preconditions** | User is browsing the site at default zoom level |
| **Steps** | 1. Browse Homepage, roadmap list, and a roadmap page <br> 2. Inspect all visible text blocks, headings, and labels |
| **Expected Result** | No text is visually clipped, truncated with "..." unexpectedly, or hidden by overflow |
| **Status** | Not Run |

---

### TC-UI-019 — Roadmap node text does not overflow node boundaries

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-019 |
| **Priority** | P2 |
| **Preconditions** | A roadmap is open |
| **Steps** | 1. Open any roadmap (e.g., Frontend Developer) <br> 2. Inspect nodes with longer labels |
| **Expected Result** | Text inside all nodes stays within node boundaries; no overflow or clipping |
| **Status** | Not Run |

---

### TC-UI-020 — Long roadmap card titles do not break card layout

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-020 |
| **Priority** | P2 |
| **Preconditions** | User is on roadmap listing page |
| **Steps** | 1. Identify roadmap cards with long titles <br> 2. Inspect the card layout at different viewport widths |
| **Expected Result** | Long titles wrap or truncate gracefully; card dimensions and layout remain intact |
| **Status** | Not Run |

---

### TC-UI-021 — Code and technical terms use monospace font

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-021 |
| **Priority** | P2 |
| **Preconditions** | User is viewing a topic detail panel or guide with code content |
| **Steps** | 1. Open a topic that contains code examples or technical terms <br> 2. Inspect font rendering |
| **Expected Result** | Code snippets and inline technical terms are rendered in a monospace/code font |
| **Status** | Not Run |

---

## 5.5 Interactive State Testing

### TC-UI-022 — Buttons show visible hover state

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-022 |
| **Priority** | P2 |
| **Preconditions** | User is browsing the site on desktop |
| **Steps** | 1. Hover mouse over various buttons (CTA, navigation links, icon buttons) |
| **Expected Result** | Each button changes visually on hover (color shift, underline, shadow, or cursor change) |
| **Status** | Not Run |

---

### TC-UI-023 — Focused elements show visible focus indicator (keyboard navigation)

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-023 |
| **Priority** | P1 |
| **Preconditions** | User is on any page with interactive elements |
| **Steps** | 1. Press Tab key to navigate through interactive elements on the page |
| **Expected Result** | Each focused element has a clearly visible focus ring or outline |
| **Status** | Not Run |

---

### TC-UI-024 — Buttons show active/pressed state on click

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-024 |
| **Priority** | P3 |
| **Preconditions** | User is on a page with clickable buttons |
| **Steps** | 1. Click and hold a button without releasing <br> 2. Observe visual state while held |
| **Expected Result** | Button shows a visually pressed/active state while being held down |
| **Status** | Not Run |

---

### TC-UI-025 — Disabled buttons look visually different from enabled buttons

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-025 |
| **Priority** | P2 |
| **Preconditions** | A disabled button exists on the page (e.g., Submit before form is filled) |
| **Steps** | 1. Locate a disabled button <br> 2. Compare its visual appearance to an enabled button |
| **Expected Result** | Disabled button is visually muted (e.g., greyed out, reduced opacity); cursor changes to not-allowed |
| **Status** | Not Run |

---

### TC-UI-026 — Buttons show loading state after triggering server actions

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-026 |
| **Priority** | P1 |
| **Preconditions** | User is on a form that communicates with the server |
| **Steps** | 1. Fill and submit a form (e.g., Login, Save Profile) <br> 2. Observe the submit button immediately after clicking |
| **Expected Result** | Button shows a loading indicator (spinner or disabled state) while the request is in flight; prevents double-submit |
| **Status** | Not Run |

---

## 5.6 Form UX Testing

### TC-UI-027 — Field labels are positioned above input fields

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-027 |
| **Priority** | P2 |
| **Preconditions** | User is on Login, Registration, or Profile forms |
| **Steps** | 1. Inspect all form fields <br> 2. Check label position before and after clicking into a field |
| **Expected Result** | Labels are visible above the field at all times; not hidden as placeholder-only labels that disappear on focus |
| **Status** | Not Run |

---

### TC-UI-028 — Validation errors appear next to their respective field

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-028 |
| **Priority** | P1 |
| **Preconditions** | User is on a form with validation |
| **Steps** | 1. Submit a form with multiple invalid fields <br> 2. Observe error message placement |
| **Expected Result** | Each error message appears directly below or next to the field it relates to; not only at the top of the form |
| **Status** | Not Run |

---

### TC-UI-029 — User input is preserved after a validation error

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-029 |
| **Priority** | P1 |
| **Preconditions** | User is filling in a form |
| **Steps** | 1. Fill in multiple fields with some valid, some invalid values <br> 2. Submit the form <br> 3. Observe field values after the validation error is shown |
| **Expected Result** | Valid field values are preserved; user does not have to retype previously entered data |
| **Status** | Not Run |

---

### TC-UI-030 — Tab order through form fields is logical

| Field | Details |
|---|---|
| **TC-ID** | TC-UI-030 |
| **Priority** | P2 |
| **Preconditions** | User is on a form (Login or Registration) |
| **Steps** | 1. Click into the first form field <br> 2. Press Tab repeatedly through all fields and the submit button |
| **Expected Result** | Focus moves in a logical order — top to bottom, left to right; no fields are skipped or focused out of order |
| **Status** | Not Run |
