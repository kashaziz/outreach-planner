# Outreach Planner — Launch Planning & TODO

> Created: 2026-03-24
> Based on: `improvements.md` review + product analysis

---

## Vision

A **generic, zero-backend outreach dashboard** — a single HTML file anyone can drop into a folder and use immediately. All data persists in localStorage. Export/import JSON for portability. Fully configurable branding so it works for any use case (SEO link building, partnerships, PR, sales outreach, etc.).

---

## Status

| Area | Status |
|---|---|
| Core UI (sidebar, tabs, table, modals) | ✅ Done (v1) |
| LocalStorage persistence | ✅ Done (v2) |
| Collapsible sidebar | ✅ Done (v2) |
| Configurable branding | ✅ Done (v2) |
| Contact detail drawer | ✅ Done (v2) |
| Templates two-panel layout | ✅ Done (v2) |
| Log two-panel + inline form | ✅ Done (v2) |
| Export / Import JSON | ✅ Done (v2) |
| Priority / OutreachType / Country fields | ✅ Done (v2) |
| Updated statuses (7 stages) | ✅ Done (v2) |
| Edit contact / template / log | ✅ Done (v2) |
| Dynamic dashboard stats | ✅ Done (v2) |

---

## Backlog (Post-v2)

### P0 — High impact, low effort

- [ ] **CSV Import** — map columns on upload (contact name, company, email, status)
- [ ] **Bulk status update** — select multiple contacts → change status at once
- [ ] **Quick log from contact row** — inline log without opening modal
- [ ] **Sort contacts** — click column header to sort by name, company, follow-up date, status

### P1 — High impact, medium effort

- [ ] **Contact notes history** — timestamped note entries per contact (currently just one notes field)
- [ ] **Template variables preview** — fill in a sample name/company and see the template rendered
- [ ] **Follow-up reminders** — browser notification API for overdue follow-ups on page load
- [ ] **Dashboard chart** — simple bar/pie chart of contacts by status using a lightweight lib (or pure SVG)
- [ ] **Search everything** — global search bar that searches contacts + log + templates at once

### P2 — Nice to have

- [ ] **Contact website field** — store and link to org website
- [ ] **LinkedIn URL field** — quick link to contact's LinkedIn profile
- [ ] **Template usage tracker** — auto-increment `used` count when template is copied
- [ ] **Log → contact auto-link** — when logging, auto-update contact's `lastContact` date
- [ ] **Dark mode** — toggle via settings
- [ ] **Print / PDF export** — formatted contact list and activity log
- [ ] **Mobile layout** — responsive design for tablet/phone use

---

## Known Issues

- Dashboard "Recent Activity" and "Follow-ups Due" sections are static in v1 → fixed in v2 (dynamic)
- Data lost on page close in v1 → fixed in v2 (localStorage)
- No way to recover from a bad import (should add validation with error message)
- Template `used` count is not incremented when copying a template (nice-to-fix)

---

## Launch Checklist

### Before sharing the template publicly:

- [ ] Remove personal/ACME-specific sample data → replace with generic placeholder data
- [ ] Add a `GETTING_STARTED.md` with setup instructions (1-page guide)
- [ ] Test in Chrome, Firefox, Safari, Edge
- [ ] Test data export → re-import round trip (verify no data loss)
- [ ] Test localStorage persistence (refresh page, confirm data survives)
- [ ] Check mobile layout at 768px width (iPad)
- [ ] Verify all CRUD operations: add/edit/delete for contacts, templates, log entries
- [ ] Verify settings: change brand color → verify all UI updates correctly
- [ ] Verify import: import a JSON file → verify data loads correctly

### README update needed:

- [ ] Add screenshots of v2 (new drawer, two-panel layouts)
- [ ] Document the export/import workflow
- [ ] Document the branding config options
- [ ] Add "Outreach Type" values to customisation guide

---

## Template Distribution Ideas

- GitHub release as a single `.html` file download
- Gumroad (free) for discoverability
- Include a `?demo=1` URL param that loads demo data even if localStorage has saved data
- A "Reset to sample data" button in settings (helpful for demos)

---

## Open Questions

1. **Outreach Types** — current defaults are: Partnership, Link Exchange, Guest Post, Association, Other. Are these the right defaults for a generic template?
2. **CSV Import** — full working implementation or UI placeholder in next release?
3. **Multi-campaign support** — should data be scoped to a single outreach campaign or support multiple named campaigns?
4. **Template sharing** — should users be able to export just templates (separate from contacts/log)?
