# Test Plan — Roadmap.sh
**URL:** https://roadmap.sh | **Date:** May 2026 | **Author:** QA Engineer (Elyor Xujam)

---

## 1. Project Overview
This plan covers functional, cross-browser, accessibility, and performance testing of roadmap.sh — a community platform for developer learning roadmaps, guides, and an AI Tutor. The goal is to evaluate quality across core user journeys and surface defects before they impact users.

---

## 2. Test Objectives
- Verify the five critical user journeys work across Chrome, Firefox, and Edge.
- Confirm progress data saves and loads correctly across sessions.
- Identify pages exceeding 3s load time on simulated Slow 3G.
- Confirm custom roadmaps save and share without data loss.

---

## 3. Scope

| In Scope | Out of Scope |
|---|---|
| Auth flows (email, GitHub, Google OAuth) | API / backend testing |
| All public roadmaps | Admin panel |
| Progress tracking | Load / stress testing |
| Search | Security penetration testing |
| Custom roadmap editor | Email delivery testing |
| AI Tutor (/ai) | Native mobile apps |
| Profile page | Payments (not applicable) |
| Cross-browser: Chrome, Firefox, Edge | Internalization beyond English |
| Responsive: desktop, tablet, mobile | |
| Accessibility (axe) + Lighthouse audit | |

---

## 4. Test Approach

**Prioritization:** Risk-based. Auth, progress persistence, and roadmap rendering first. Cosmetic/low-risk features last.

**Testing types:** Functional · Exploratory · Cross-browser · Responsive · Accessibility · Performance

**Techniques:** Equivalence partitioning for inputs · Boundary value analysis for field limits · Decision tables for auth logic

### Severity Levels

| Severity | Definition | Example |
|---|---|---|
| Critical | App unusable or data loss | Login broken for all users; progress deleted |
| High | Core feature broken for some users | Progress not saving for GitHub OAuth users |
| Medium | Feature works but incorrectly | Search returns wrong results |
| Low | Minor visual or edge case | Tooltip misaligned on small screens |

---

## 5. Test Environment

| Component | Detail |
|---|---|
| Browsers | Chrome (latest), Firefox (latest), Edge (latest) |
| OS | Windows 11 |
| Resolutions | 1920×1080, 1366×768 |
| Mobile (DevTools) | iPhone 12 Pro (390×844), iPad Air (820×1180) |
| Network | Normal 4G + Slow 3G (performance tests) |
| Auth states | Guest + registered test account |
| Tools | axe DevTools, Chrome Lighthouse |

---

## 6. Risk Assessment

| Risk | Probability | Impact | Priority |
|---|---|---|---|
| Progress not persisting across sessions | Medium | Critical | P1 |
| OAuth (GitHub/Google) login breaking | Low | Critical | P1 |
| Roadmap SVG broken on Firefox | Medium | High | P1 |
| Custom roadmap save failing silently | Medium | High | P1 |
| Search returning irrelevant results | Medium | Medium | P2 |
| Layout broken at mobile sizes | Medium | Medium | P2 |
| External links broken/outdated | High | Medium | P2 |
| SVG accessibility violations | High | Medium | P2 |
| Slow page load on 3G | Medium | Medium | P2 |
| Dark mode inconsistency | Medium | Low | P3 |

---
=
## 7. Entry & Exit Criteria

**Entry** (start when all true):
- Repo set up, requirements complete, test accounts created, axe DevTools installed.

**Exit** (stop when all true):
- All P1 test cases executed. All Critical/High bugs reported. ≥80% test case coverage. Lighthouse audits done. Test summary report complete.