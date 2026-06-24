# Roadmap.sh QA Portfolio Project

[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)](#)
[![Test Cases](https://img.shields.io/badge/Test%20Cases-127%20Written-blue)](#)
[![Pass Rate](https://img.shields.io/badge/Pass%20Rate-90.6%25-blue)](#)
[![Bugs Found](https://img.shields.io/badge/Bugs%20Found-18%20Reported-orange)](#)
[![Coverage](https://img.shields.io/badge/P1%20Coverage-100%25-brightgreen)](#)

> **Production-Grade Black-Box QA Audit**
> A comprehensive manual test cycle, accessibility check, and exploratory testing framework executed against the live, production developer platform [roadmap.sh](https://roadmap.sh)

---

## 📊 Findings Summary

| Metric | Result |
| :--- | :--- |
| **QA Engineer** | **Elyor Xujam** ([elyorxujam.uz](https://elyorxujam.uz)) |
| **Total Test Cases** | 127 Written & 100% Executed |
| **Pass Rate** | **90.6%** (115 Passed, 11 Failed) |
| **P1 Coverage** | **100%** |
| **Defect Density** | 0.14 bugs / TC (18 total defects found) |

*   **⚡ Module Health:** Authentication (30 TCs) and AI Tutor (20 TCs) achieved a perfect **100% Pass Rate**. Custom Editor (95%), Roadmap Viewer (91.7%), and Progress Tracking (85%) remain highly stable.
*   **⚠️ Primary Risk Areas:** The Search module contains a high concentration of low-severity bugs. Dedicated keyboard-only navigation infrastructure is currently absent across interactive layers.
*   **🚦 Go / No-Go Verdict:** **GO.** The live application remains fully deployable and operational. No critical blockers were identified during the cycle, and all primary core user journeys are functioning as intended.

---

## 🎯 Testing Scope & Matrix

| Feature Module | Tested? | Key Validation Notes |
| :--- | :--- | :--- |
| **Authentication** | ✅ Yes | Registration, Login, and GitHub OAuth verification (100% stable) |
| **AI Tutor** | ✅ Yes | Dynamic quiz flows, content generation, and prompt handling (100% stable) |
| **Custom Editor** | ✅ Yes | Node creation constraints, layout rendering, and link submissions |
| **Roadmap Viewer** | ✅ Yes | Component interactions, node clicks, and path view filtering |
| **Progress Tracking** | ✅ Yes | Status updates (Done/Skip actions) and basic metric tracking |
| **Search Engine** | ✅ Yes | Global queries, community indexing, and boundary input handling |
| **Exploratory Testing** | ✅ Yes | Targeted unscripted testing (Order, Data Boundary, State, and Touch attacks) |
| **Performance** | ⚠️ Partial | Basic UI performance auditing and rendering benchmarks |

---

## 🐛 Core Defect Registry

Out of the 18 total defects discovered, these are the key technical findings prioritized for future engineering sprints[cite: 1]:

| Bug ID | Summary Description | Severity | Area |
| :--- | :--- | :--- | :--- |
| **BUG-001** | Browser tab crashes due to lack of upper limit on node creation in custom editor | 🟡 Medium | Custom Roadmap |
| **BUG-003** | System accepts deleted GitHub repository links without validation during project submission | 🟡 Medium | Roadmap -> Project |
| **BUG-005** | Text overflows outside node boundaries when typing long strings in custom editor | 🟡 Medium | Accessibility / UI |
| **Search Bugs** | Multiple low-severity display and query boundary discrepancies | 🟢 Low | Search Engine |
