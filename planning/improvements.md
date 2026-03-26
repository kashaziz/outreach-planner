# Outreach Planner — Proposed Improvements

> Compiled on 2026-03-10 after reviewing the HalalCodeCheck reference dashboard.
> Review each item and mark ✅ approved / ❌ skip / 💬 needs discussion before implementing.

---

## A. Dashboard

1. Replace "Meetings Booked" → **"Converted"** stat card
2. Replace "Response Rate %" → **count of Replied + In Negotiation** (actual pipeline number, not a %)
3. Add **Outreach Progress panel** — per-status row breakdown with count (Not Contacted → Contacted → Replied → In Negotiation → Converted → Declined → On Hold)
4. Add **By Priority panel** — High / Medium / Low each showing `contacted / total` ratio
5. Add **By Outreach Type panel** — per type showing `X converted` (e.g. Link Exchange, Partnership, Guest Post)

---

## B. Contacts

6. Add **Priority** field (High / Medium / Low) to each contact
7. Add **Outreach Type** field (Link Exchange / Partnership / Guest Post / Association / Other)
8. Add **Country** field
9. Add **Follow-up Date** field (replaces plain text "Last Contact" — actual datepicker)
10. Expand statuses to: Not Contacted, Contacted, Replied, In Negotiation, **Converted**, Declined, On Hold
11. Add Priority and Outreach Type **filters** to the filter bar
12. Add **Edit contact** — pencil icon opens pre-filled modal
13. Add **Import CSV** button (map columns on upload)

---

## C. Templates

14. Redesign layout: **sidebar list** (left) + **full preview panel** (right) — instead of current card grid
15. Add **Edit template** — in-place editing in the preview panel
16. Add **"When to use" / notes** field per template (shown as a highlighted note in preview)

---

## D. Activity Log

17. Redesign: **inline add-entry form on the left** (always visible, no modal) + log table on the right
18. Add **Template Used** field to each log entry (dropdown of your templates)
19. Add **Response Received** field (Yes / No / Awaiting)
20. Add **Next Action** field (free text, e.g. "Follow up Mar 15")
21. Add **Edit log entry** option

---

## E. Data Persistence

22. **localStorage auto-save** — data survives page refresh (biggest usability win)
23. **Export / Download Data** button (JSON file)
24. **Open File / Import** button (load a previously exported JSON)

---

## Open Questions

- **Outreach Type values** — are Link Exchange, Partnership, Guest Post, Association the right types for ACME, or should these be different?
- **Import CSV (#13)** — full working implementation or just UI placeholder for now?
- **Scope** — implement all 24 in one pass, or prioritise a subset?
