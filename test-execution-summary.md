# 📈 Test Execution Summary

**Project:** Personal Portfolio Website — Manual QA Pass
**Date Executed:** 04.09.2026
**Tester:** Petar Sotirovski

---

## Overall Results

| Metric | Count |
|---|---|
| Total Test Cases | 18 |
| Passed | 16 |
| Failed | 2 |
| Blocked / Not Executed | 0 |
| **Pass Rate** | **88.9%** |

## Results by Category

| Category | Total | Passed | Failed |
|---|---|---|---|
| Navigation & Functional Flow | 4 | 3 | 1 |
| Forms | 3 | 3 | 0 |
| Responsiveness | 2 | 2 | 0 |
| Cross-Browser Compatibility | 1 | 1 | 0 |
| Accessibility | 2 | 1 | 1 |
| Performance & Technical Health | 5 | 5 | 0 |

## Defects Summary

| Bug ID | Title | Severity | Status |
|---|---|---|---|
| BUG-001 | Broken/placeholder link in footer | Medium | Open |
| BUG-002 | Missing alt text on portfolio thumbnails | Low | Open |

## Notes & Observations

- No critical or blocking defects were identified — the site is functionally stable across all core user flows (navigation, contact form, responsive layout).
- Both identified defects are low-to-medium severity and low-effort to resolve, typical of the kind of polish issues found in a personal/independent project rather than systemic failures.
- Accessibility testing surfaced a genuine, common real-world issue (missing alt text) — a good example of why accessibility checks belong in a standard QA pass rather than being treated as optional.
- This test cycle covered functional, responsiveness, cross-browser, accessibility, and technical health testing categories, reflecting a well-rounded manual QA approach suitable for a junior QA role.

## Next Steps

- [ ] Fix BUG-001 (update footer link destination)
- [ ] Fix BUG-002 (add descriptive alt text to all project thumbnails)
- [ ] Re-test TC-007 and TC-013 after fixes are deployed
- [ ] Expand suite with additional edge-case and negative test scenarios in a future test cycle
