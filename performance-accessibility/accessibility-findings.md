# Accessibility Audit Findings Report

**Date:** June 22, 2026  
**Project:** Roadmap.sh Frontend & Dashboard  
**Compliance Target:** WCAG 2.1 AA  
**Total Issues Found:** 8 Issues (2 Critical, 6 Serious)  

---

## 📊 Executive Summary

This report aggregates automated accessibility testing results across three key pages of the application. Resolving these issues will significantly improve keyboard navigation, screen reader support, and visual readability.

| Target URL | Critical Issues | Serious Issues | Total |
| :--- | :---: | :---: | :---: |
| [`/dashboard?fl=0`](#1-dashboard-dashboardfl0) | 0 | 2 | **2** |
| [`/frontend`](#2-frontend-roadmapshfrontend) | 1 | 3 | **4** |
| [`/account/update-profile`](#3-profile-settings-roadmapshaccountupdate-profile) | 1 | 1 | **2** |
| **Total** | **2** | **6** | **8** |

---

## 🔍 Detailed Findings & Remediation Guide

### 1. Dashboard (`/dashboard?fl=0`)

#### 🔴 Issue 1.1: Insufficient Color Contrast on Action Link
* **Impact:** Serious
* **Category:** Color Contrast (`wcag143`, `wcag2aa`)
* **Element Location:** `.border-dashed`
* **Code Snippet:**
    ```html
    <a class="flex h-[30px] shrink-0 items-center gap-1 rounded-md p-1.5 transition-colors hover:bg-slate-700 border border-dashed border-slate-700 bg-transparent px-3 text-[13px] text-gray-500 hover:border-solid hover:border-slate-700 hover:text-gray-400" href="/teams/new" data-discover="true">
    ```
* **The Problem:** The link text color (`#6a7282` / `text-gray-500`) against the dark background (`#131c30`) yields a contrast ratio of **3.51:1**. The minimum required ratio for normal text is **4.5:1**.
* **Remediation:** Change the text color class to a lighter gray to stand out against the dark background. Switching from `text-gray-500` to `text-gray-300` (`#d1d5db`) or `text-slate-300` will clear the 4.5:1 threshold.

#### 🔴 Issue 1.2: Missing Accessible Text for Graphic SVG
* **Impact:** Serious
* **Category:** Text Alternatives (`wcag111`, `wcag2a`)
* **Element Location:** `svg[role="img"]`
* **Code Snippet:**
    ```html
    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" height="24" width="24" class="inline-block h-5 w-5 fill-current">
    ```
* **The Problem:** The SVG element is marked with `role="img"` but provides no accessible name, rendering it completely empty and confusing for screen readers.
* **Remediation:** Add an explicit `aria-label` attribute directly to the `<svg>` element or embed a `<title>` tag inside it:
    ```html
    <svg role="img" aria-label="Team Icon" ...>
    ```

---

### 2. Frontend (`/frontend`)

#### 🚨 Issue 2.1: Non-Discernible Button Text (Icon Only)
* **Impact:** **Critical** (Blocks screen reader access entirely)
* **Category:** Name / Role / Value (`wcag412`, `wcag2a`)
* **Element Location:** `.rounded-r-full`
* **Code Snippet:**
    ```html
    <button class="flex cursor-pointer items-center justify-center self-stretch rounded-r-full pr-3 pl-2 text-gray-500 transition-colors hover:bg-white/10 hover:text-gray-300">
    ```
* **The Problem:** The button element lacks inner text or any label attribute. Assistive technologies will only announce "button" without communicating its purpose.
* **Remediation:** Inject an `aria-label` describing the specific action of the button:
    ```html
    <button aria-label="Submit search" type="button" class="flex ...">
    ```

#### 🔴 Issue 2.2: Prohibited ARIA Attribute on Generic Element
* **Impact:** Serious
* **Category:** ARIA (`wcag412`, `wcag2a`)
* **Element Location:** `#google_ads_iframe_\/22873384501\/roadmap_0 .close-button`
* **Code Snippet:**
    ```html
    <span class="close-button" aria-label="Close">
    ```
* **The Problem:** The `aria-label` attribute is invalid on a generic `<span>` because it has no default interactive role. Screen readers will discard the label.
* **Remediation:** * *Option A (Best Practice):* Replace the `<span>` element with an explicit `<button>` tag:
        ```html
        <button class="close-button" aria-label="Close Ad" type="button">
        ```
    * *Option B:* If markup changes are restricted, add `role="button"` along with `tabindex="0"` to make it focusable:
        ```html
        <span class="close-button" role="button" aria-label="Close Ad" tabindex="0">
        ```

#### 🔴 Issue 2.3: Low Contrast on Call-To-Action Span
* **Impact:** Serious
* **Category:** Color Contrast (`wcag143`, `wcag2aa`)
* **Element Location:** `.text-yellow-600 > span`
* **Code Snippet:**
    ```html
    <span>Watch demo</span>
    <!-- Parent container has .text-yellow-600 inside a wrapper with bg-yellow-50 -->
    ```
* **The Problem:** The dark yellow foreground text (`#d08700`) sitting over a light yellow container background (`#fefce8`) produces an insufficient contrast ratio of **2.84:1** (expected **4.5:1**).
* **Remediation:** Increase the text darkness. Replace `text-yellow-600` with `text-yellow-800` (`#854d0e`) or a solid dark neutral color for high visibility on warm light backgrounds.

#### 🔴 Issue 2.4: Missing Accessible Text for Graphic SVG (Instance 2)
* **Impact:** Serious
* **Category:** Text Alternatives (`wcag111`, `wcag2a`)
* **Element Location:** `svg[role="img"]`
* **Code Snippet:**
    ```html
    <svg role="img" viewBox="0 0 24 24" ...>
    ```
* **The Problem:** Another instance of an interactive graphic missing descriptive tags for non-sighted users.
* **Remediation:** Add an explicit text alternative via `aria-label` based on what the icon represents (e.g., `aria-label="External link"`).

---

### 3. Profile Settings (`/account/update-profile`)

#### 🚨 Issue 3.1: Missing Labeling on Custom Select Combobox
* **Impact:** **Critical**
* **Category:** Name / Role / Value (`wcag412`, `wcag2a`)
* **Element Location:** `.border-gray-200`
* **Code Snippet:**
    ```html
    <button type="button" role="combobox" aria-controls="radix-_r_l_" aria-expanded="false" aria-autocomplete="none" dir="ltr" data-state="closed" class="flex items-center ju...">
    ```
* **The Problem:** This Radix UI select trigger controls an interactive dropdown menu, but it doesn't pass a clear text label to screen readers.
* **Remediation:** Connect the combobox trigger button to its companion visual input label using `aria-labelledby`, or pass an explicit structural label directly:
    ```html
    <button aria-label="Select profile country" type="button" role="combobox" ...>
    ```

#### 🔴 Issue 3.2: Insufficient Label Contrast on Form Settings
* **Impact:** Serious
* **Category:** Color Contrast (`wcag143`, `wcag2aa`)
* **Element Location:** `label[for="isEmailVisible"]`
* **Code Snippet:**
    ```html
    <label for="isEmailVisible" class="grow cursor-pointer py-1.5">Show my email on profile</label>
    ```
* **The Problem:** The label text color (`#99a1af`) against a stark white background (`#ffffff`) yields a highly illegible contrast value of **2.6:1**.
* **Remediation:** Replace the muted gray class with a highly visible alternative. Changing the color value to `#57534e` (`text-stone-600`) or `#475569` (`text-slate-600`) safely resolves the contrast deficiency while maintaining clean styling.