# Bootstrap v3.4.2 (Tricentis security patch)

Security fixes for **CVE-2024-6484**, **CVE-2024-6485**, and **CVE-2025-1647**:

- **CVE-2024-6484 (Carousel XSS):** Sanitize `data-target`, `data-slide-to`, and `href` in carousel data-api; only allow safe `#id` selectors and integer slide indices.
- **CVE-2024-6485 (Button XSS):** Sanitize `data-loading-text` (and related text) with DOMPurify when available, otherwise HTML-escape before setting button content.
- **CVE-2025-1647 (Tooltip/Popover XSS / DOM clobbering):** Use DOMPurify for HTML sanitization when available; read tooltip/popover options from explicit `data-*` attributes to prevent DOM clobbering.

**Usage:** Include [DOMPurify](https://github.com/cure53/DOMPurify) before Bootstrap for full sanitization (e.g. `<script src="dompurify.min.js"></script>`). Without DOMPurify, built-in sanitization/escaping still reduces risk.

---

**Repository:** https://github.com/tompotri/bootstrap-tri
