# Manual QA Testing Portfolio & Test Suite
**Author:** Petar Sotirovski, BSc in Information Systems  
**Target Application:** Personal Architecture Web Portfolio / Corporate Showcase Web  

## 📌 Project Overview
This repository contains a comprehensive suite of manual testing documentation, structured test cases, and quality assurance logs designed to verify the performance, responsiveness, and functional logic of web architectures under cross-browser environments.

## 📊 Test Cases Suite (Functional & UI Testing)

### Test Case TC-001: Mobile Navigation Responsiveness
* **Objective:** Verify that the hamburger menu functions smoothly across iOS/Android mobile browsers.
* **Pre-conditions:** Device resolution set to mobile layout (< 768px).
* **Execution Steps:**
  1. Load the homepage on a mobile browser viewport.
  2. Click the hamburger navigation icon in the top right corner.
  3. Attempt to scroll vertically while the overlay menu is active.
* **Expected Result:** The menu remains securely anchored, links are fully clickable, and layout structure stays intact.
* **Status:** ✅ PASSED

### Test Case TC-002: Contact Form Validation Logic
* **Objective:** Ensure data input validation blocks improper email formats from processing.
* **Execution Steps:**
  1. Navigate to the contact interface page.
  2. Enter alphanumeric text without proper domain notation (e.g., "petartest") into the Email field.
  3. Click the "Submit" action button.
* **Expected Result:** System triggers an inline visual warning stating "Invalid Email Format", and form submission is halted.
* **Status:** ✅ PASSED

### Test Case TC-003: Asset Loading Stability (Smoke Test)
* **Objective:** Confirm heavy high-resolution portfolio images scale dynamically on 4K resolutions without visual degradation.
* **Execution Steps:**
  1. Open the project presentation portfolio on a UHD monitor profile.
  2. Expand view to maximum browser resolution.
* **Expected Result:** CSS and container boundaries dynamically rescale images (Responsive Design Verification) with clean anti-aliasing.
* **Status:** ✅ PASSED
