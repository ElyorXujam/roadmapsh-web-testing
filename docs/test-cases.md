# Test Cases — Roadmap.sh
**URL:** https://roadmap.sh | **Date:** May 2026 | **Author:** QA Engineer

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

## Phase 1 — Authentication

---

### TC-AUTH-01 — Register with valid email and password
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is not logged in. Email address has not been registered before. |

**Steps:**
1. Navigate to https://roadmap.sh
2. Click "Sign Up" or "Register"
3. Enter a valid unique email address
4. Enter a password that meets the stated requirements
5. Submit the form

**Expected Result:** Account is created. User is redirected to the dashboard or home page in an authenticated state. A confirmation email is sent (if applicable).

**Status:** Not Run

---

### TC-AUTH-02 — Register with already-used email
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | An account already exists for the email being used. |

**Steps:**
1. Navigate to the registration page
2. Enter an email address already registered
3. Enter any valid password
4. Submit the form

**Expected Result:** Registration is rejected. A clear error message is displayed: "Email already in use" or similar. No duplicate account is created.

**Status:** Not Run

---

### TC-AUTH-03 — Register with invalid email format
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is not logged in. |

**Steps:**
1. Navigate to the registration page
2. Enter an invalid email (e.g., `notanemail`, `test@`, `@domain.com`)
3. Enter a valid password
4. Submit the form

**Expected Result:** Form is not submitted. An inline validation error indicates the email format is invalid.

**Status:** Not Run

---

### TC-AUTH-04 — Register with empty fields
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | User is not logged in. |

**Steps:**
1. Navigate to the registration page
2. Leave all fields empty
3. Click the submit button

**Expected Result:** Form is not submitted. Required field errors are shown for each empty field.

**Status:** Not Run

---

### TC-AUTH-05 — Login with valid email and password
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | A registered account exists. User is logged out. |

**Steps:**
1. Navigate to the login page
2. Enter the registered email
3. Enter the correct password
4. Click "Sign In"

**Expected Result:** User is authenticated and redirected to the home page or dashboard. Username or avatar is visible in the navigation.

**Status:** Not Run

---

### TC-AUTH-06 — Login with incorrect password
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | A registered account exists. User is logged out. |

**Steps:**
1. Navigate to the login page
2. Enter a valid registered email
3. Enter an incorrect password
4. Click "Sign In"

**Expected Result:** Login fails. An error message is shown: "Invalid credentials" or similar. User remains on the login page.

**Status:** Not Run

---

### TC-AUTH-07 — Login with unregistered email
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged out. |

**Steps:**
1. Navigate to the login page
2. Enter an email not registered on the platform
3. Enter any password
4. Click "Sign In"

**Expected Result:** Login fails. An error message is displayed. User is not authenticated.

**Status:** Not Run

---

### TC-AUTH-08 — Login via GitHub OAuth
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User has a valid GitHub account. User is logged out of roadmap.sh. |

**Steps:**
1. Navigate to the login page
2. Click "Sign in with GitHub"
3. Authorize the roadmap.sh OAuth application on GitHub
4. Return to roadmap.sh

**Expected Result:** User is authenticated. A roadmap.sh account is created or linked. User is redirected to the dashboard in an authenticated state.

**Status:** Not Run

---

### TC-AUTH-09 — Login via Google OAuth
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User has a valid Google account. User is logged out of roadmap.sh. |

**Steps:**
1. Navigate to the login page
2. Click "Sign in with Google"
3. Select or authenticate a Google account
4. Authorize the application if prompted

**Expected Result:** User is authenticated and redirected to the dashboard. Account is created or linked.

**Status:** Not Run

---

### TC-AUTH-10 — Forgot password flow
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | A registered email account exists. User is logged out. |

**Steps:**
1. Navigate to the login page
2. Click "Forgot Password"
3. Enter the registered email address
4. Submit the form
5. Check the inbox for the reset email
6. Click the reset link
7. Enter and confirm a new password
8. Submit

**Expected Result:** A reset email is sent. The link is functional. The password is updated. User can log in with the new password.

**Status:** Not Run

---

### TC-AUTH-11 — Logout
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Click on the user avatar or profile menu
2. Click "Logout" or "Sign Out"

**Expected Result:** Session is terminated. User is redirected to the home page in a guest state. Navigating to a protected page redirects to login.

**Status:** Not Run

---

### TC-AUTH-12 — Session persists after browser restart
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Log in to roadmap.sh
2. Close the browser completely
3. Reopen the browser and navigate to https://roadmap.sh

**Expected Result:** User remains authenticated without being asked to log in again.

**Status:** Not Run

---

### TC-AUTH-13 — Unauthenticated user cannot access progress tracking
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is not logged in. |

**Steps:**
1. Navigate to any roadmap (e.g., https://roadmap.sh/frontend)
2. Attempt to click on a node to mark it as "Done"

**Expected Result:** A prompt or modal appears asking the user to sign in or register. Progress is not saved. User is not silently ignored.

**Status:** Not Run

---

## Phase 2 — Roadmaps

---

### TC-RM-01 — Homepage displays role-based and skill-based roadmaps
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh
2. Scroll through the homepage

**Expected Result:** Both role-based (e.g., Frontend, Backend, DevOps) and skill-based (e.g., React, Docker, Python) roadmaps are listed and accessible.

**Status:** Not Run

---

### TC-RM-02 — Roadmap renders as an interactive node graph
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Observe the page content

**Expected Result:** An interactive node graph is rendered. Nodes are connected with directional arrows indicating recommended order. All nodes are visible and not overlapping.

**Status:** Not Run

---

### TC-RM-03 — Clicking a node opens the resource panel
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Click on any topic node (e.g., "HTML")

**Expected Result:** A side panel or modal opens showing the topic description, links, and learning resources. The roadmap remains visible in the background.

**Status:** Not Run

---

### TC-RM-04 — Resource panel closes without losing scroll position
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Scroll down the roadmap canvas
3. Click a node to open the resource panel
4. Close the panel (click X or press Escape)

**Expected Result:** Panel closes. The roadmap canvas returns to the same scroll position as before the panel was opened.

**Status:** Not Run

---

### TC-RM-05 — Roadmap page has a shareable public URL
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to any roadmap (e.g., https://roadmap.sh/backend)
2. Copy the URL from the browser address bar
3. Open the URL in a new incognito window

**Expected Result:** The roadmap loads correctly for a guest user without requiring login.

**Status:** Not Run

---

### TC-RM-06 — Roadmap canvas supports zoom and pan on desktop
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Use the mouse scroll wheel to zoom in and out
3. Click and drag the canvas to pan

**Expected Result:** The roadmap canvas zooms and pans smoothly. Nodes remain readable at all zoom levels.

**Status:** Not Run

---

### TC-RM-07 — Best Practices roadmaps are accessible
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/best-practices or find the Best Practices section on the homepage
2. Click on any best practices entry (e.g., API Security)

**Expected Result:** A best practices page loads with structured content distinct from the node-graph roadmap format.

**Status:** Not Run

---

## Phase 3 — Progress Tracking

---

### TC-PROG-01 — Mark a node as Done
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Right-click or click on a topic node
3. Select "Done" from the status options

**Expected Result:** The node's visual state changes (e.g., turns green or shows a checkmark). The change is reflected immediately.

**Status:** Not Run

---

### TC-PROG-02 — Mark a node as In Progress
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Click on a topic node
3. Select "In Progress"

**Expected Result:** Node visual state updates to reflect "In Progress" status with a distinct color or indicator.

**Status:** Not Run

---

### TC-PROG-03 — Mark a node as Skip
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Click on a topic node
3. Select "Skip"

**Expected Result:** Node is visually marked as skipped with a distinct indicator different from Done and In Progress.

**Status:** Not Run

---

### TC-PROG-04 — Progress persists after logout and login
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Mark 3 nodes as Done
3. Log out
4. Log back in
5. Navigate back to https://roadmap.sh/frontend

**Expected Result:** All 3 nodes are still marked as Done. Progress is not lost.

**Status:** Not Run

---

### TC-PROG-05 — Progress percentage updates correctly
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. Roadmap has known total node count. |

**Steps:**
1. Navigate to any roadmap
2. Note the current completion percentage
3. Mark one additional node as Done
4. Observe the percentage

**Expected Result:** Completion percentage increases proportionally (e.g., if 10 nodes total and 1 is marked, percentage shows 10%).

**Status:** Not Run

---

### TC-PROG-06 — Reset progress for a roadmap
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | User is logged in. At least one node has been marked. |

**Steps:**
1. Navigate to a roadmap with progress saved
2. Find and click the "Reset Progress" option
3. Confirm the reset action

**Expected Result:** All nodes return to their unmarked state. Completion percentage resets to 0%.

**Status:** Not Run

---

### TC-PROG-07 — Progress not saved for guest users
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is not logged in. |

**Steps:**
1. Navigate to any roadmap
2. Attempt to mark a node

**Expected Result:** A login prompt appears. No progress is silently saved to the browser.

**Status:** Not Run

---

### TC-PROG-08 — Started roadmaps appear on profile
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | User is logged in. At least one roadmap has progress. |

**Steps:**
1. Navigate to the user profile page
2. Look for a roadmaps or progress section

**Expected Result:** All roadmaps with saved progress are listed with their current completion percentages.

**Status:** Not Run

---

## Phase 4 — Search

---

### TC-SRCH-01 — Search bar is accessible from navigation
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh
2. Locate the search bar in the main navigation

**Expected Result:** A search input is visible and clickable in the main navigation on all pages.

**Status:** Not Run

---

### TC-SRCH-02 — Search returns results in real time
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Click the search bar
2. Type "react" slowly, one character at a time
3. Observe results after each keystroke

**Expected Result:** Results appear after a short debounce delay (not on every single keystroke). Results update as more characters are typed. No full page reload occurs.

**Status:** Not Run

---

### TC-SRCH-03 — Search is case-insensitive
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Search for "REACT"
2. Note the results
3. Search for "react"
4. Compare results

**Expected Result:** Both searches return the same results regardless of case.

**Status:** Not Run

---

### TC-SRCH-04 — Search supports partial keyword matching
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Type "fron" in the search bar

**Expected Result:** Results including "Frontend" roadmap are returned even though the full word was not typed.

**Status:** Not Run

---

### TC-SRCH-05 — Search results show result type
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Search for "python"
2. Inspect the results list

**Expected Result:** Each result displays a label or badge indicating its type (Roadmap, Guide, Article, etc.).

**Status:** Not Run

---

### TC-SRCH-06 — Search shows no results message for unknown query
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Type a nonsense string in the search bar (e.g., "xyzxyzxyz123")

**Expected Result:** A "no results found" message is displayed. No blank or broken state appears.

**Status:** Not Run

---

### TC-SRCH-07 — Search results are keyboard navigable
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Click the search bar and type "docker"
2. Without using the mouse, press the Down arrow key
3. Navigate through results using arrow keys
4. Press Enter on a result

**Expected Result:** Results are navigable with keyboard only. The selected result is visually highlighted. Pressing Enter navigates to the selected page.

**Status:** Not Run

---

## Phase 5 — AI Tutor

---

### TC-AI-01 — AI Tutor page loads
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/ai

**Expected Result:** The AI Tutor chat interface loads with a visible input field and a prompt or welcome message.

**Status:** Not Run

---

### TC-AI-02 — AI Tutor answers a domain-relevant question
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/ai
2. Type: "What should I learn first as a frontend developer?"
3. Submit the message

**Expected Result:** The AI responds with a relevant, coherent answer related to frontend development. A loading indicator is shown while the response generates.

**Status:** Not Run

---

### TC-AI-03 — AI Tutor recommends a roadmap
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/ai
2. Ask: "Which roadmap should I follow to become a backend developer?"

**Expected Result:** The AI recommends the Backend roadmap and provides a link or reference to it on roadmap.sh.

**Status:** Not Run

---

### TC-AI-04 — AI response renders markdown correctly
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/ai
2. Ask a question likely to produce a code block (e.g., "Show me a basic React component")

**Expected Result:** The response renders with proper markdown formatting — code blocks, syntax highlighting, lists, and links are displayed correctly, not as raw markdown text.

**Status:** Not Run

---

### TC-AI-05 — AI shows loading indicator while responding
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Submit any message to the AI Tutor
2. Observe the UI immediately after submission

**Expected Result:** A spinner, typing indicator, or loading animation is shown while the response is being generated.

**Status:** Not Run

---

### TC-AI-06 — AI Tutor handles out-of-scope queries gracefully
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh/ai
2. Ask a completely unrelated question (e.g., "What is the best pizza recipe?")

**Expected Result:** The AI responds gracefully, either declining to answer or redirecting the user toward developer-related topics. It does not crash or return an error.

**Status:** Not Run

---

## Phase 6 — Custom Roadmaps

---

### TC-CR-01 — Authenticated user can open the custom roadmap editor
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Navigate to the custom roadmap creation option (via profile or navigation)
2. Click "Create Roadmap" or equivalent

**Expected Result:** A visual editor canvas opens, ready for the user to add nodes and connections.

**Status:** Not Run

---

### TC-CR-02 — Add, edit, and delete a node
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in and inside the custom roadmap editor. |

**Steps:**
1. Add a new node to the canvas
2. Set a title and description for the node
3. Save the node
4. Edit the node title to something different
5. Delete the node

**Expected Result:** Each action completes successfully. The canvas updates in real time. Deleted nodes are removed from the canvas.

**Status:** Not Run

---

### TC-CR-03 — Connect two nodes with an edge
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is in the editor with at least two nodes on the canvas. |

**Steps:**
1. Drag from one node's connection handle to another node
2. Release to create an edge

**Expected Result:** A directional edge is created connecting the two nodes. The connection is visible on the canvas.

**Status:** Not Run

---

### TC-CR-04 — Save a custom roadmap
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is in the editor with at least one node added. |

**Steps:**
1. Click the Save button
2. Provide a title if prompted
3. Confirm save

**Expected Result:** Roadmap is saved. A success message is shown. The roadmap appears in the user's profile.

**Status:** Not Run

---

### TC-CR-05 — Set custom roadmap to public and get shareable URL
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User has a saved custom roadmap. |

**Steps:**
1. Open the custom roadmap settings
2. Set visibility to "Public"
3. Copy the generated shareable URL
4. Open the URL in an incognito window

**Expected Result:** The roadmap is accessible to a guest user via the shareable URL without requiring login.

**Status:** Not Run

---

### TC-CR-06 — Set custom roadmap to private
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User has a saved custom roadmap previously set to public. |

**Steps:**
1. Open roadmap settings
2. Set visibility to "Private"
3. Open the shareable URL in an incognito window

**Expected Result:** The roadmap is not accessible to guest users. A 404 or access-denied page is shown.

**Status:** Not Run

---

### TC-CR-07 — Delete a custom roadmap
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | User has at least one saved custom roadmap. |

**Steps:**
1. Navigate to the custom roadmaps section in the profile
2. Select a roadmap and choose Delete
3. Confirm the deletion

**Expected Result:** Roadmap is removed. It no longer appears in the profile. Its public URL (if set) returns a 404.

**Status:** Not Run

---

### TC-CR-08 — Custom roadmap appears in user profile
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | User has at least one saved custom roadmap. |

**Steps:**
1. Navigate to the user's profile page

**Expected Result:** The custom roadmaps section lists all saved custom roadmaps with their titles and visibility status.

**Status:** Not Run

---

## Phase 7 — Profile

---

### TC-PROF-01 — Public profile is accessible via unique URL
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | A registered user account exists. |

**Steps:**
1. Navigate to https://roadmap.sh/u/[username]
2. Observe the page

**Expected Result:** A public profile page loads showing the user's avatar, name, and bio. Page is accessible without login.

**Status:** Not Run

---

### TC-PROF-02 — Edit profile information
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Navigate to profile settings
2. Update the display name
3. Update the bio
4. Add a social link (e.g., GitHub URL)
5. Save changes

**Expected Result:** All changes are saved and reflected immediately on the public profile page.

**Status:** Not Run

---

### TC-PROF-03 — Profile displays roadmap progress
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in and has progress on at least one roadmap. |

**Steps:**
1. Navigate to the user's profile page

**Expected Result:** In-progress and completed roadmaps are listed with correct completion percentages.

**Status:** Not Run

---

### TC-PROF-04 — Set profile to private
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | User is logged in. |

**Steps:**
1. Go to profile settings
2. Set profile visibility to "Private"
3. Log out
4. Navigate to the user's public profile URL

**Expected Result:** Profile is not accessible to guests. A 404 or "private profile" message is shown.

**Status:** Not Run

---

### TC-PROF-05 — Delete account
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. Use a throwaway test account for this test. |

**Steps:**
1. Navigate to account settings
2. Find and click "Delete Account"
3. Confirm the deletion (enter password or confirm prompt)

**Expected Result:** Account is permanently deleted. User is logged out. Logging in with the same credentials fails. Public profile URL returns 404.

**Status:** Not Run

---

## Phase 8 — UI & UX

---

### TC-UI-01 — Dark mode toggle works and persists
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh
2. Toggle dark mode on
3. Navigate to a roadmap page
4. Refresh the page

**Expected Result:** Dark mode is applied site-wide. Preference persists after page refresh and navigation. No elements appear broken (invisible text, wrong contrast) in dark mode.

**Status:** Not Run

---

### TC-UI-02 — Navigation contains all expected links
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh
2. Inspect the main navigation bar

**Expected Result:** Navigation includes links to Roadmaps, Guides, Projects, and the AI Tutor. All links work and navigate to the correct pages.

**Status:** Not Run

---

### TC-UI-03 — All interactive elements have hover and focus states
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Navigate through the homepage and a roadmap page
2. Hover over buttons, links, and nodes with the mouse
3. Tab through the page using the keyboard

**Expected Result:** Every interactive element shows a visible hover state on mouse-over and a visible focus ring when focused via keyboard.

**Status:** Not Run

---

## Phase 9 — Cross-Browser & Responsive

---

### TC-CROSS-01 — Roadmap renders correctly on Firefox
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | Firefox latest is installed. |

**Steps:**
1. Open Firefox
2. Navigate to https://roadmap.sh/frontend

**Expected Result:** The roadmap node graph renders fully. All nodes and edges are visible. Interactions (click node, pan, zoom) work correctly.

**Status:** Not Run

---

### TC-CROSS-02 — Roadmap renders correctly on Edge
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | Microsoft Edge latest is installed. |

**Steps:**
1. Open Edge
2. Navigate to https://roadmap.sh/frontend
3. Interact with nodes and resource panel

**Expected Result:** Full parity with Chrome behavior. No rendering issues.

**Status:** Not Run

---

### TC-RESP-01 — Layout is usable on mobile viewport (390×844)
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | Chrome DevTools open. |

**Steps:**
1. Open Chrome DevTools and set device to iPhone 12 Pro (390×844)
2. Navigate to https://roadmap.sh
3. Navigate to a roadmap page
4. Try to interact with the roadmap (tap a node, scroll)

**Expected Result:** Homepage is readable with no horizontal overflow. Roadmap is navigable via pinch-zoom and pan. Nodes are tappable.

**Status:** Not Run

---

### TC-RESP-02 — Layout is usable on tablet viewport (820×1180)
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | Chrome DevTools open. |

**Steps:**
1. Set device to iPad Air (820×1180) in DevTools
2. Navigate through the homepage and a roadmap

**Expected Result:** Layout adapts cleanly. Navigation is usable. Roadmap canvas is fully visible and interactive.

**Status:** Not Run

---

## Phase 10 — Performance

---

### TC-PERF-01 — Roadmap page LCP under 2.5s (desktop)
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | Chrome DevTools Lighthouse available. |

**Steps:**
1. Open Chrome DevTools > Lighthouse
2. Select Desktop mode
3. Run audit on https://roadmap.sh/frontend

**Expected Result:** Largest Contentful Paint (LCP) is under 2.5 seconds. Performance score is noted.

**Status:** Not Run

---

### TC-PERF-02 — Page load under 3s on Slow 3G
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | Chrome DevTools open. |

**Steps:**
1. Set network throttle to Slow 3G in DevTools
2. Run Lighthouse on https://roadmap.sh/frontend in Mobile mode

**Expected Result:** Page becomes usable within 3 seconds on simulated Slow 3G. LCP metric is recorded.

**Status:** Not Run

---

### TC-PERF-03 — CLS score is below 0.1
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | Chrome DevTools Lighthouse available. |

**Steps:**
1. Run a Lighthouse audit on the homepage and a roadmap page
2. Record the Cumulative Layout Shift (CLS) score

**Expected Result:** CLS score is below 0.1 on both pages.

**Status:** Not Run

---

### TC-PERF-04 — Search results appear within 300ms
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | Chrome DevTools Network tab open. |

**Steps:**
1. Open the Network tab in DevTools
2. Type a search query and stop typing
3. Observe when results appear and check the network timing

**Expected Result:** Search results render within ~300ms of the user stopping input.

**Status:** Not Run

---

## Phase 11 — Accessibility

---

### TC-ACC-01 — No critical axe violations on homepage
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | axe DevTools browser extension is installed. |

**Steps:**
1. Navigate to https://roadmap.sh
2. Open axe DevTools and run a full scan

**Expected Result:** Zero critical or serious violations are reported. Any moderate issues are noted for review.

**Status:** Not Run

---

### TC-ACC-02 — No critical axe violations on a roadmap page
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | axe DevTools installed. |

**Steps:**
1. Navigate to https://roadmap.sh/frontend
2. Run axe DevTools full scan

**Expected Result:** Zero critical violations. SVG elements have appropriate ARIA roles or labels.

**Status:** Not Run

---

### TC-ACC-03 — All form fields have accessible labels
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to the registration and login pages
2. Inspect each input field in DevTools or use axe

**Expected Result:** Every input has an associated `<label>` element or `aria-label`. No inputs are label-less.

**Status:** Not Run

---

### TC-ACC-04 — Site is keyboard-navigable without a mouse
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh
2. Use only Tab, Shift+Tab, Enter, and arrow keys
3. Attempt to reach the search bar, a roadmap link, and the login page

**Expected Result:** All key interactive elements are reachable and operable with keyboard only. Focus indicator is clearly visible at every step.

**Status:** Not Run

---

### TC-ACC-05 — Progress status is not communicated by color alone
| Field | Detail |
|---|---|
| **Priority** | P1 |
| **Preconditions** | User is logged in. At least one node is marked. |

**Steps:**
1. Navigate to a roadmap with marked nodes
2. Inspect marked nodes — check for icon, label, or aria attribute alongside the color change

**Expected Result:** Node status is conveyed by an icon, text label, or aria-label in addition to color. Color alone is not the sole indicator.

**Status:** Not Run

---

### TC-ACC-06 — Text scales to 200% without content loss
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to https://roadmap.sh
2. In browser settings, set text size to 200%
3. Navigate through the homepage, a roadmap, and the login page

**Expected Result:** All content remains readable and accessible. No text is clipped, hidden, or overlapping at 200% scale.

**Status:** Not Run

---

### TC-ACC-07 — Modal/panel traps focus when open
| Field | Detail |
|---|---|
| **Priority** | P2 |
| **Preconditions** | None. |

**Steps:**
1. Navigate to a roadmap and click a node to open the resource panel
2. Press Tab repeatedly while the panel is open
3. Close the panel

**Expected Result:** Tab focus stays within the panel while it is open. When closed, focus returns to the node that triggered it.

**Status:** Not Run

---

*Total test cases: 57*
*Coverage: Authentication (13) · Roadmaps (7) · Progress (8) · Search (7) · AI Tutor (6) · Custom Roadmaps (8) · Profile (5) · UI (3) · Cross-Browser & Responsive (4) · Performance (4) · Accessibility (7)*