# Test Summary Report: roadmap.sh

**Project:** Roadmap.sh Web App 
**Date:** June 24, 2026  
**QA Engineer:** [Elyor Xujam/ elyorxujam.uz ] 
**Test Cycle:** Full Functional, Accessibility, Exploratory, Performance. 

---

## 📊 Execution Metrics at a Glance

* **Total Test Cases:** 127 written & 100% executed
* **Pass Rate:** **90.6%** (115 Passed, 11 Failed)

* **P1 Requirement Coverage:** **100%**

* **Defect Density:** 0.14 bugs / TC (18 total defects found)

### Module Breakdown
* **100% Pass:** Authentication (30 TCs), AI Tutor (20 TCs)

* **Stable:** Custom Editor (95%), Roadmap Viewer (91.7%), Progress Tracking (85%)
---

## 🚨 Critical Defect & Risk Analysis

Total Defects: **18** (0 Critical, 4 High, 8 Medium, 6 Low)

### 🔴 The 3 Bugs
1. **BUG-001 (Custom roadmap):**Browser tab crashes due to lack of upper limit on node creation in custom roadmap editor

2. **BUG-003 (Roadmap -> Project):** System accepts deleted GitHub repository links without validation during project submission

3. **BUG-005 (Accessibility):** Text overflows outside node boundaries when typing long strings in custom roadmap editor

### 🟡 Buggy aeras 
* **Search Engine Vulnerability:** There are a lot "low" severity bugs.

* **Keyboard Navigaton:** Keyboard Navigation not even exist. 

---

## 🚦 Go / No-Go Recommendation

> **STATUS: GO - there isn't any critical bug and all core user journeys working fine**

