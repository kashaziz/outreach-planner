# ACME Outreach Planner

A lightweight, single-file outreach management tool for marketing teams. No backend, no database — everything runs in the browser.

![Dashboard Screenshot](screenshots/home.png)

## Overview

Outreach Planner helps marketers manage their outreach pipeline from a single HTML file. Track contacts, store reusable email templates, and maintain a full activity log — all without needing a CRM subscription.

## Features

- **Dashboard** — At-a-glance stats: total contacts, emails sent, response rate, meetings booked. Pipeline overview and upcoming follow-ups.
- **Contacts** — Add and manage prospects with status tracking (New → Contacted → Replied → Meeting Booked). Search and filter by status or company.
- **Email Templates** — Store and reuse outreach templates for every stage (Initial, Follow-up, Meeting, LinkedIn, Re-engagement). One-click copy to clipboard.
- **Activity Log** — Log every touchpoint: emails, calls, meetings, LinkedIn messages. Filter by type or search by contact.

## Screenshots

| Dashboard | Contacts |
|-----------|----------|
| ![Dashboard](screenshots/home.png) | ![Contacts](screenshots/contacts.png) |

| Templates | Activity Log |
|-----------|--------------|
| ![Templates](screenshots/templates.png) | ![Log](screenshots/log.png) |

## Getting Started

No installation needed. Just open the file:

```bash
# Clone the repo
git clone <repo-url>
cd outreach-planner

# Open in browser
open outreach-planner.html       # macOS
start outreach-planner.html      # Windows
xdg-open outreach-planner.html  # Linux
```

Or simply double-click `outreach-planner.html` in your file explorer.

## Usage

### Managing Contacts

1. Click **Add Contact** in the top-right or sidebar
2. Fill in name, company, email, and status
3. Use the search and filter bar to find contacts quickly
4. Click the **+** icon on any contact row to log an activity

### Using Templates

1. Browse existing templates by category
2. Click **Copy to clipboard** to grab the full email (subject + body)
3. Paste into your email client and personalise the `[FirstName]`, `[Company]` placeholders
4. Add new templates with the **New Template** button

### Logging Activities

1. Go to the **Activity Log** tab
2. Click **Log Activity** and select a contact, type, and date
3. Add any notes about the interaction

## Data & Privacy

All data is stored in-memory within the browser session. **Data does not persist between page refreshes.** For persistent storage, a future version may add:

- `localStorage` export/import
- CSV export
- CRM integrations (HubSpot, Salesforce, Pipedrive)

## Tech Stack

- Plain HTML5, CSS (Tailwind CSS via CDN), Vanilla JavaScript
- No build step, no dependencies to install
- Font Awesome icons via CDN

## Roadmap

- [ ] localStorage persistence (data survives refresh)
- [ ] CSV import/export for contacts
- [ ] Email sequence builder (automate follow-up cadences)
- [ ] CRM sync (HubSpot, Salesforce)
- [ ] Team sharing via URL params or JSON export
- [ ] Dark mode

## Contributing

1. Fork the repo
2. Make your changes in `outreach-planner.html`
3. Test in browser
4. Submit a pull request

---

Built for the ACME marketing team. Keep your outreach organised. 🎯
