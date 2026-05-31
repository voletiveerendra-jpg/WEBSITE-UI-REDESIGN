# UI/UX Usability Audit: Starbucks Hero Component

This document serves as a usability evaluation and layout bug report for the initial **Starbucks Landing Page Header** design iteration, based on industry-standard design heuristics and alignment frameworks.

---

## 1. Severity Rating System

To ensure smooth cross-functional collaboration, tracked layout issues are categorized by impact level:
* 🔴 **Critical:** Severe text clipping, broken structural overlapping, or functional ambiguity.
* 🟡 **Major:** Alignment breaks, text truncation, or clear visual balance imbalances.
* 🔵 **Minor:** Small cosmetic adjustments or spacing consistency tweaks.

---

## 2. Documented Layout & Usability Issues

### 🛑 Issue 1: Text Clipping and Truncation in Utility Search Bar
* **Severity:** 🔴 Critical
* **Heuristic:** Aesthetic and Minimalist Design / Prevent Errors
* **Description:** Inside the header navigation, the search placeholder text reads `SEARCH COFFES,`. The word "COFFEES" is misspelled, and the trailing comma indicates that the text layer bounding box is too narrow—clipping or cutting off the end of the text block.
* **Impact:** Looks unpolished to the end-user and physically risks hiding critical placeholder context on slightly narrower desktop viewports.
* **Recommended Fix:** 
  * Correct the spelling to `SEARCH COFFEE` or `Search...`.
  * Expand the width of the text layer container in Figma or set the horizontal resizing behavior to **Auto Width**.

---

### ⚠️ Issue 2: Inconsistent Horizontal Kerning and Alignment in Promo Banner
* **Severity:** 🟡 Major
* **Heuristic:** Consistency and Standards
* **Description:** The black promotional banner text reads `GET 15%OFFER UPTO $15   USE CODE : VEERU`. There is a total absence of spacing between `15%` and `OFFER` (`15%OFFER`), while an unnaturally large gap exists between `$15` and the coupon code section.
* **Impact:** Reduces readability of the key marketing trigger and value proposition.
* **Recommended Fix:** 
  * Standardize word spacing: `GET 15% OFFER UP TO $15 | USE CODE: VEERU`.
  * Utilize Auto-Layout on the banner to evenly distribute spacing between the offer announcement and the code badge.

---

### ⚠️ Issue 3: Interactive Button Sizing Discrepancies (Login vs. Cart)
* **Severity:** 🟡 Major
* **Heuristic:** Flexability and Efficiency of Use (Touch Targets)
* **Description:** The `LOGIN` feature uses an explicit, rounded rectangle pill border framing its user icon and text label. Conversely, the `CART` element relies entirely on raw text and a standalone cart icon without an underlying bounding box or balanced spacing.
* **Impact:** Unequal visual weights create a confusing interactive hierarchy, making it unclear if the login button and cart button function as peer-level utilities.
* **Recommended Fix:** 
  * Turn both elements into uniform components. Wrap both the Login group and Cart group in matching Auto-Layout frames with subtle, matching padding or background fills to normalize the hit-target sizes.

---

### 🔵 Issue 4: Navigation Links Alignment with Global Container
* **Severity:** 🔵 Minor
* **Heuristic:** Visual Hierarchy
* **Description:** The primary navigation sub-links (`HOME`, `SHOP ALL`, `ABOUT`) are bunched close together and lack a hard alignment anchor point relative to either the left-aligned Starbucks brand logo or the right-side global actions.
* **Impact:** The layout feels slightly loose, risking accidental clicks on adjacent links on standard interactive viewports.
* **Recommended Fix:** 
  * Apply a standardized gap of `24px` or `32px` between each individual nav item.
  * Center-align the link group container globally within the header frame.

---

## 3. Next Actions for Design Hand-off
1. [ ] Correct spelling arrays across headers.
2. [ ] Standardize typography spacing variables inside the markdown promotional bar component.
3. [ ] Convert Utility UI icons into unified interactive component states (`Default`, `Hover`, `Focused`).
4.
