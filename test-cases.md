# 📊 Test Case Suite — Personal Portfolio Website

**Scope:** Functional, UI, responsiveness, cross-browser, accessibility, and technical health testing.
**Test Type:** Manual, Black-Box Testing

---

## 1. Navigation & Functional Flow

### TC-001: Mobile Navigation Responsiveness
- **Objective:** Verify that the hamburger menu functions smoothly across iOS/Android mobile browsers.
- **Pre-conditions:** Device resolution set to mobile layout (< 768px).
- **Execution Steps:**
  1. Load the homepage on a mobile browser viewport.
  2. Click the hamburger navigation icon in the top right corner.
  3. Attempt to scroll vertically while the overlay menu is active.
- **Expected Result:** The menu remains securely anchored, links are fully clickable, and layout structure stays intact.
- **Status:** ✅ PASSED

### TC-004: Desktop Navigation Bar Functionality
- **Objective:** Verify all desktop navigation links route to the correct section/page.
- **Execution Steps:**
  1. Load the homepage on desktop viewport (≥1024px).
  2. Click each nav item (Home, About, Projects, Contact) in sequence.
  3. Observe hover/active state on each item.
- **Expected Result:** Each link navigates or scrolls to the correct section; hover state is visually distinct.
- **Status:** ✅ PASSED

### TC-005: Internal Anchor Link Scrolling
- **Objective:** Confirm smooth-scroll anchor links land at the correct section without offset/overlap issues.
- **Execution Steps:**
  1. Click a nav link that scrolls to an in-page section (e.g., "Projects").
  2. Observe scroll behavior and final resting position.
- **Expected Result:** Page scrolls smoothly and section heading is fully visible, not obscured by a sticky header.
- **Status:** ✅ PASSED

### TC-006: External Link Behavior
- **Objective:** Verify external links (GitHub, LinkedIn, email) open correctly and safely.
- **Execution Steps:**
  1. Click each external link/icon.
  2. Confirm destination and whether it opens in a new tab.
- **Expected Result:** Correct destination loads; external links open in a new tab (`target="_blank"`) without breaking the portfolio tab.
- **Status:** ✅ PASSED

### TC-007: Broken Link / 404 Check
- **Objective:** Confirm no links on the site lead to dead pages or incorrect destinations.
- **Execution Steps:**
  1. Click through every link on the site (nav, footer, project cards, social icons).
  2. Note the destination URL and page status for each.
- **Expected Result:** All links resolve to valid, intended destinations with no 404s.
- **Status:** ❌ FAILED — see `BUG-001` in `bug-reports.md`

---

## 2. Forms

### TC-002: Contact Form Validation Logic
- **Objective:** Ensure data input validation blocks improper email formats from processing.
- **Execution Steps:**
  1. Navigate to the contact interface page.
  2. Enter alphanumeric text without proper domain notation (e.g., "petartest") into the Email field.
  3. Click the "Submit" action button.
- **Expected Result:** System triggers an inline visual warning stating "Invalid Email Format," and form submission is halted.
- **Status:** ✅ PASSED

### TC-008: Contact Form Empty Field Submission
- **Objective:** Verify the form cannot be submitted with required fields left blank.
- **Execution Steps:**
  1. Navigate to the contact form.
  2. Leave all fields empty.
  3. Click "Submit."
- **Expected Result:** Validation errors appear for each required field; form does not submit.
- **Status:** ✅ PASSED

### TC-009: Contact Form Successful Submission
- **Objective:** Confirm a correctly filled form submits successfully and gives clear user feedback.
- **Execution Steps:**
  1. Fill in name, valid email, and message fields correctly.
  2. Click "Submit."
- **Expected Result:** A success confirmation message/state is displayed to the user.
- **Status:** ✅ PASSED

---

## 3. Responsiveness

### TC-003: Asset Loading Stability (Smoke Test)
- **Objective:** Confirm heavy high-resolution portfolio images scale dynamically on 4K resolutions without visual degradation.
- **Execution Steps:**
  1. Open the project presentation portfolio on a UHD monitor profile.
  2. Expand view to maximum browser resolution.
- **Expected Result:** CSS and container boundaries dynamically rescale images (Responsive Design Verification) with clean anti-aliasing.
- **Status:** ✅ PASSED

### TC-010: Tablet Layout Responsiveness (768px–1024px)
- **Objective:** Verify layout integrity at tablet breakpoints, a range often overlooked between mobile and desktop design.
- **Execution Steps:**
  1. Resize browser (or use DevTools device toolbar) to 768px and 1024px widths.
  2. Inspect grid layout, text wrapping, and spacing at both widths.
- **Expected Result:** No overlapping elements, broken grids, or horizontal scroll/overflow at either breakpoint.
- **Status:** ✅ PASSED

---

## 4. Cross-Browser Compatibility

### TC-011: Cross-Browser Rendering Consistency
- **Objective:** Confirm consistent layout, font rendering, and color output across major browsers.
- **Execution Steps:**
  1. Open the site in Chrome, Firefox, and Safari.
  2. Compare layout, spacing, fonts, and color rendering across all three.
- **Expected Result:** Visually consistent experience across browsers, with no major layout shifts or font-fallback issues.
- **Status:** ✅ PASSED

---

## 5. Accessibility

### TC-012: Keyboard Navigation & Focus States
- **Objective:** Verify the site is navigable using only a keyboard (Tab/Shift+Tab/Enter), supporting basic accessibility standards.
- **Execution Steps:**
  1. Load the homepage.
  2. Use only the Tab key to move through all interactive elements (links, buttons, form fields).
  3. Observe whether a visible focus indicator appears on each element.
- **Expected Result:** All interactive elements are reachable in a logical order, each with a clearly visible focus state.
- **Status:** ✅ PASSED

### TC-013: Alt Text Presence on Images
- **Objective:** Confirm all meaningful images have descriptive `alt` attributes for screen reader accessibility.
- **Execution Steps:**
  1. Inspect each image element via DevTools.
  2. Check for presence and relevance of `alt` text.
- **Expected Result:** All non-decorative images have descriptive, relevant alt text.
- **Status:** ❌ FAILED — see `BUG-002` in `bug-reports.md`

---

## 6. Performance & Technical Health

### TC-014: Page Load Performance
- **Objective:** Confirm the homepage loads within an acceptable time for a portfolio site.
- **Execution Steps:**
  1. Open DevTools → Network tab.
  2. Hard-reload the homepage.
  3. Record total load time and largest contentful paint (LCP).
- **Expected Result:** Load time under ~3 seconds on a standard broadband connection.
- **Status:** ✅ PASSED

### TC-015: Browser Console Error Check
- **Objective:** Ensure no JavaScript errors or warnings appear during normal site usage.
- **Execution Steps:**
  1. Open DevTools console.
  2. Browse through all pages/sections of the site.
- **Expected Result:** No red (error-level) console output during normal navigation.
- **Status:** ✅ PASSED

### TC-016: Favicon & Page Title Verification
- **Objective:** Confirm correct branding elements appear in the browser tab (SEO/meta basics).
- **Execution Steps:**
  1. Load the site and observe the browser tab.
- **Expected Result:** Correct, descriptive page title and a properly rendered favicon are present.
- **Status:** ✅ PASSED

### TC-017: HTTPS / Secure Connection Check
- **Objective:** Verify the site is served securely with no mixed-content warnings.
- **Execution Steps:**
  1. Load the site and check the browser's address bar security indicator.
  2. Check DevTools console for mixed-content warnings.
- **Expected Result:** Site loads over HTTPS with a valid certificate and no mixed-content warnings.
- **Status:** ✅ PASSED

### TC-018: Responsive Image Optimization Check
- **Objective:** Confirm images are served at appropriately optimized sizes rather than oversized originals, to support performance.
- **Execution Steps:**
  1. Open DevTools → Network tab, filter by image requests.
  2. Compare rendered image dimensions vs. actual file dimensions/size.
- **Expected Result:** Images are reasonably optimized/compressed for web delivery, without excessive oversizing.
- **Status:** ✅ PASSED
