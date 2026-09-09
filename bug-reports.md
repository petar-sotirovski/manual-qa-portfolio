# 🐞 Bug Reports — Personal Portfolio Website

Formal defect reports filed during manual testing, following standard bug lifecycle documentation practice.

---

## BUG-001: Broken/Placeholder Link Found in Footer

- **Linked Test Case:** TC-007 (Broken Link / 404 Check)
- **Severity:** Medium
- **Priority:** Medium
- **Environment:** Chrome 128, Windows 11 (also reproducible in Firefox)

**Steps to Reproduce:**
1. Navigate to the homepage.
2. Scroll to the footer section.
3. Click the [social/project] link icon.

**Expected Result:**
Link should navigate to the correct, live destination URL.

**Actual Result:**
Link either points to a placeholder (`#`) href or an outdated destination, resulting in no navigation or an incorrect page load.

**Notes:**
Likely a leftover placeholder from initial site scaffolding that wasn't updated before deployment. Low complexity fix — update the `href` attribute to the correct destination.

**Status:** Open

---

## BUG-002: Missing Alt Text on Portfolio Thumbnail Images

- **Linked Test Case:** TC-013 (Alt Text Presence on Images)
- **Severity:** Low
- **Priority:** Medium (accessibility impact)
- **Environment:** Chrome 128, Windows 11

**Steps to Reproduce:**
1. Navigate to the Projects section.
2. Inspect each project thumbnail image via DevTools (Elements panel).
3. Check the `alt` attribute value for each `<img>` tag.

**Expected Result:**
Each project thumbnail should include a descriptive `alt` attribute (e.g., `alt="3D character render – sci-fi helmet project"`).

**Actual Result:**
Several thumbnail images have empty (`alt=""`) or missing `alt` attributes entirely.

**Notes:**
This affects screen reader accessibility (WCAG 1.1.1 — Non-text Content) and slightly impacts SEO image indexing. Fix is low-effort: add descriptive alt text per image during the next content update.

**Status:** Open

---
