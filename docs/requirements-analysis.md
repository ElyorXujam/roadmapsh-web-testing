# All Requirements for Roadmap.sh Website
> Requirements collected via analyzing the site's behavior, implied requirements, and stated claims.

---

## 1. Authentication Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| AUTH-01 | The system shall allow users to register with an email and password. | High |
| AUTH-02 | The system shall allow users to sign in via GitHub OAuth. | High |
| AUTH-03 | The system shall allow users to sign in via Google OAuth. | High |
| AUTH-04 | The system shall allow users to sign in via Linkedin OAuth. | High |
| AUTH-05 | The system shall allow users to sign in via Apple OAuth. | High |
| AUTH-06 | The system shall support email/password login with secure credential handling. | High |
| AUTH-07 | The system shall provide a "Forgot Password" flow that sends a reset link to the registered email. | High |
| AUTH-08 | Authenticated state shall persist across browser sessions (remember me). | Medium |
| AUTH-09 | The system shall restrict access to protected features (progress, custom roadmaps, profile) to authenticated users only. | High |
| AUTH-10 | The system shall display prompts to sign in or register when unauthenticated users attempt to access gated features. | Medium |

---

## 2. Roadmap Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| RM-01 | The system shall provide role-based roadmaps (e.g., Frontend, Backend, DevOps, Full Stack, AI Engineer). | High |
| RM-02 | The system shall provide skill-based roadmaps (e.g., React, Python, Docker, SQL). | High |
| RM-03 | Each roadmap shall be rendered as an interactive node graph with clickable topic nodes. | High |
| RM-04 | Clicking a node shall open a resource panel with descriptions, links, and learning materials. | High |
| RM-05 | Roadmaps shall clearly indicate recommended order of topics using visual flow (arrows/edges). | High |
| RM-06 | Each roadmap shall have a shareable public URL. | High |
| RM-07 | The system shall display a roadmap's last-updated date or changelog reference. | Medium |
| RM-08 | Roadmaps shall be community-maintained and reflect current industry standards. | High |
| RM-09 | The system shall support "Best Practices" roadmaps as a distinct content type. | Medium |
| RM-10 | The system shall allow users to zoom and pan the roadmap canvas on both desktop and mobile. | High |
| RM-11 | The system shall support "New" labels on recently added roadmap nodes or entire roadmaps. | Low |
| RM-12 | Each roadmap page shall include a table of contents or topic summary for quick navigation. | Medium |
| RM-13 | Each roadmap page shall include a progress bar on top of the roadmap. | Medium | 

---

## 3. Progress Tracking Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| PROG-01 | Authenticated users shall be able to mark individual roadmap topics as "Done", "In Progress", or "Skip". | High |
| PROG-02 | Progress status shall persist across sessions and devices for authenticated users. | High |
| PROG-03 | The roadmap UI shall visually reflect progress status using distinct color indicators per node. | High |
| PROG-04 | The system shall display an overall completion percentage for each roadmap. | High |
| PROG-05 | Users shall be able to reset all progress for a given roadmap. | Medium |
| PROG-06 | Progress data shall be linked to the user's account, not the browser. | High |
| PROG-07 | Unauthenticated users shall be prompted to log in when attempting to mark progress. | Medium |
| PROG-08 | The system shall show a summary of all roadmaps the user has started on their profile or dashboard. | Medium |

---

## 4. Search Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| SRCH-01 | The system shall provide a search bar accessible from "Roadmap Chat" in the Ai Tutor navigation. | High |
| SRCH-02 | Search shall cover all official roadmaps. | High |
| SRCH-03 | Search results shall appear in real-time as the user types. | High |
| SRCH-04 | Search results shall display result type roadmap alongside the title. | Medium |
| SRCH-05 | Search shall be non case-insensitive and support partial keyword matching. | High |
| SRCH-06 | The system shall surface the most relevant results first. | High |
| SRCH-07 | Search results shall be keyboard-navigable. | Medium |
| SRCH-08 | The system shall provide a search bar accessible from "Community Roadmaps" in the Roadmaps navigation. | High |
| SRCH-09 | The system shall display a "no results found" message for unmatched queries for Community Roadmaps search bar. | Medium |



---

## 5. Custom Roadmap Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| CR-01 | Authenticated users shall be able to create custom roadmaps from scratch using a visual editor. | High |
| CR-02 | The editor shall allow adding, editing, and deleting nodes and connecting edges. | High |
| CR-03 | Users shall be able to set custom titles and descriptions for each node. | High |
| CR-04 | Custom roadmaps shall support public and private visibility settings. | High |
| CR-05 | The system shall generate a shareable public URL for public custom roadmaps. | High |
| CR-06 | Users shall be able to duplicate an existing official roadmap as a starting template for a custom one. | Medium |
| CR-07 | Custom roadmaps shall appear in the user's profile under a dedicated section. | Medium |
| CR-08 | Users shall be able to delete or archive their custom roadmaps. | Medium |
| CR-09 | The system shall support exporting a custom roadmap as an image (PNG/SVG). | Low |
| CR-10 | Progress tracking shall apply to custom roadmaps in the same way as official ones. | Medium |

---

## 6. Project Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| PROJ-01 | The system shall provide curated project ideas categorized by domain (Frontend, Backend, DevOps). | High |
| PROJ-02 | Each project listing shall include a title, difficulty level, and brief description. | High |
| PROJ-03 | Projects shall link to or be associated with a relevant official roadmap. | Medium |
| PROJ-04 | Authenticated users shall be able to mark projects as completed. | Medium |
| PROJ-05 | The system shall allow users to submit their project solution URL for review or sharing. | Low |
| PROJ-06 | Projects shall be ordered by difficulty (beginner, intermediate, advanced). | Medium |
| PROJ-07 | Project pages shall include acceptance criteria or expected deliverables. | Medium |

---

## 7. AI Chat (AI Tutor) Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| AI-01 | The system shall provide an AI Tutor chat interface accessible at a dedicated URL (/ai). | High |
| AI-02 | The AI Tutor shall answer questions related to topics within roadmap.sh's content domain (developer skills, tools, concepts). | High |
| AI-03 | The AI Tutor shall be able to recommend relevant roadmaps or resources based on the user's query. | High |
| AI-04 | Chat sessions shall persist within a browser session; authenticated users may have persistent history. | Medium |
| AI-05 | The AI Tutor shall gracefully handle out-of-scope queries with a clear response. | Medium |
| AI-06 | The AI Tutor UI shall support markdown rendering in responses (code blocks, lists, links). | High |
| AI-07 | The system shall clearly indicate when the AI is generating a response (loading state). | Medium |
| AI-08 | Authenticated users shall be able to start new chat sessions and view previous ones. | Medium |
| AI-09 | The AI Tutor shall be accessible to both authenticated and unauthenticated users with reasonable rate limits for guests. | Medium |

---

## 8. Profile Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| PROF-01 | Each authenticated user shall have a public profile page accessible via a unique URL (e.g., /u/username). | High |
| PROF-02 | The profile shall display the user's avatar, display name, and bio. | High |
| PROF-03 | The profile shall list the user's in-progress and completed roadmaps with progress percentages. | High |
| PROF-04 | The profile shall list the user's public custom roadmaps. | Medium |
| PROF-05 | Users shall be able to edit their profile information (name, bio, avatar, social links). | High |
| PROF-06 | Users shall be able to set their profile to public or private. | Medium |
| PROF-07 | The profile shall display social links (GitHub, Twitter/X, LinkedIn, website). | Medium |
| PROF-08 | Users shall be able to delete their account and all associated data. | High |
| PROF-09 | The system shall allow users to change their email address with verification. | Medium |
| PROF-10 | The profile shall show a roadmap activity or streak indicator. | Low |

---

## 9. UI & Design Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| UI-01 | The system shall support a dark mode toggle, with the preference persisted per user. | High |
| UI-02 | Navigation shall include quick links to roadmaps, guides, projects, and the AI Tutor. | High |
| UI-03 | The homepage shall display curated role-based and skill-based roadmap lists. | High |
| UI-04 | The system shall use consistent typography, color tokens, and spacing across all pages. | High |
| UI-05 | Roadmap node tooltips or panels shall be dismissible without losing current scroll position. | Medium |
| UI-06 | The system shall display a changelog page summarizing recent updates. | Medium |
| UI-07 | All interactive elements (buttons, links) shall have visible hover and focus states. | High |
| UI-08 | The site shall include a persistent footer with links to community, GitHub, and social channels. | Low |
| UI-09 | Page transitions shall be smooth and not cause layout shift (CLS). | Medium |
| UI-10 | The system shall display appropriate empty states for sections with no content. | Medium |

---

## 10. Performance Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| PERF-01 | Roadmap pages shall achieve a Largest Contentful Paint (LCP) under 2.5 seconds on a standard connection. | High |
| PERF-02 | The system shall lazy-load roadmap node content and resource panels on demand. | High |
| PERF-03 | Static roadmap assets shall be served via a CDN with appropriate cache headers. | High |
| PERF-04 | The system shall achieve a Cumulative Layout Shift (CLS) score below 0.1. | High |
| PERF-05 | Search results shall appear within 300ms of the user stopping input (debounce). | Medium |
| PERF-06 | The system shall minimize JavaScript bundle size using code splitting per route. | Medium |
| PERF-07 | API responses for progress updates shall complete within 500ms under normal load. | Medium |
| PERF-08 | The system shall gracefully degrade performance under high traffic without full outage. | High |

---

## 11. Accessibility Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| ACC-01 | The system shall meet WCAG 2.1 Level AA compliance. | High |
| ACC-02 | All images and icons shall include descriptive alt text or aria-labels. | High |
| ACC-03 | The roadmap interactive canvas shall be keyboard-navigable (tab through nodes, enter to open). | High |
| ACC-04 | Color alone shall not be used to convey progress state; icons or labels shall accompany color. | High |
| ACC-05 | All form fields shall have associated visible or accessible labels. | High |
| ACC-06 | Focus indicators shall be clearly visible on all interactive elements. | High |
| ACC-07 | The site shall be usable with screen readers (NVDA, VoiceOver). | High |
| ACC-08 | Text contrast ratios shall meet a minimum of 4.5:1 for normal text and 3:1 for large text. | High |
| ACC-09 | Modal dialogs and panels shall trap focus when open and restore focus on close. | Medium |
| ACC-10 | The site shall support text scaling up to 200% without loss of content or functionality. | Medium |