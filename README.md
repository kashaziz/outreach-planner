# Outreach Planner

A single-file outreach management tool. No backend, no database, no installation — just open the HTML file in your browser.

![Dashboard](screenshots/home.png)

## Features

### Dashboard
- Greeting with time-of-day and user name
- Stats: Total Contacts, In Pipeline, Converted, Follow-ups Due
- Outreach Pipeline with per-status breakdown
- Priority breakdown with contacted ratios
- Recent activity feed
- Upcoming follow-ups (clickable)

### Contacts
- 50 sample contacts across 15+ countries
- Sortable columns: Organisation, Status, Priority, Type, Country, Follow-up, Last Contact
- Pagination (15 per page)
- Search + filter by status, priority, outreach type
- Add / Edit / Delete via modal
- Contact detail drawer with full info and activity history

### Email Templates
- Two-panel layout: sidebar list + full preview
- Search and category filter
- "When to use" guidance notes
- Placeholder support: `[FirstName]`, `[Company]`, `[Title]`
- Copy to clipboard

### Activity Log
- Inline add-entry form + log table
- Sortable columns (Contact, Activity, Response)
- Clickable contact names (navigates to contact drawer)
- Edit / Delete entries

### Settings
- App name, subtext, brand colour (8 palettes)
- Logo icon picker (10 options) or custom image upload
- Sidebar colour auto-adapts to brand
- User name and title

### Data Safety
- Auto-saves to localStorage on every change
- Export / Import JSON
- Auto-backup download before Reset or Import
- Change counter with backup reminder after 10 unsaved changes
- Browser exit warning when changes are unsaved
- Backup status indicator in sidebar

## Screenshots

| Dashboard | Contacts |
|-----------|----------|
| ![Dashboard](screenshots/home.png) | ![Contacts](screenshots/contacts.png) |

| Templates | Activity Log |
|-----------|--------------|
| ![Templates](screenshots/templates.png) | ![Log](screenshots/log.png) |

| Settings | Contact Detail |
|----------|----------------|
| ![Settings](screenshots/settings.png) | ![Contact Detail](screenshots/contact-detail.png) |

## Getting Started

No installation needed. Just open the file:

```bash
# Clone the repo
git clone <repo-url>
cd outreach-planner

# Open in browser
open outreach-planner.html       # macOS
start outreach-planner.html      # Windows
xdg-open outreach-planner.html   # Linux
```

Or double-click `outreach-planner.html` in your file explorer.

Works fully offline via `file://` protocol — no server required.

## Usage

### Managing Contacts

1. Click **Add Contact** from the Dashboard or Contacts tab
2. Fill in name, company, email, country, status, priority, and outreach type
3. Use search and filters to find contacts quickly
4. Click any row to open the contact detail drawer
5. Click the pencil icon to edit, or the **+** icon to log an activity

### Using Templates

1. Browse templates in the sidebar list
2. Click a template to preview it
3. Click **Copy to Clipboard** to grab subject + body
4. Paste into your email client and replace `[FirstName]`, `[Company]` placeholders

### Logging Activities

1. Go to the **Activity Log** tab
2. Use the inline form on the left to select a contact, type, date, and notes
3. Click **Log It**
4. Click any contact name in the log to jump to their detail view

### Backing Up Data

- Click **Export** on the Dashboard or in Settings to download a JSON backup
- The sidebar shows your backup status (green = recent, amber = overdue, red = never)
- Before any destructive action (Reset, Import), a backup is auto-downloaded
- The browser will warn you before closing if you have 10+ unsaved changes

## Customisation

Open **Settings** to rebrand:

- Change the app name and tagline
- Pick a brand colour (sidebar adapts automatically)
- Choose a logo icon or upload a custom image
- Set your name and title

All settings persist in localStorage.

## Tech Stack

- Single HTML file (~490 KB)
- Tailwind CSS (inlined, only used classes)
- Font Awesome 6 (inlined, 44 icons + 2 webfonts as base64)
- Vanilla JavaScript, no build step, no dependencies
- localStorage for persistence
- Works offline, no CDN required

## Project Structure

```
outreach-planner/
  outreach-planner.html   # The app (single file, fully self-contained)
  data/
    defaults.json          # Reference copy of default data (not loaded at runtime)
  screenshots/
    home.png               # Dashboard
    contacts.png           # Contacts tab
    templates.png          # Templates tab
    log.png                # Activity Log tab
    settings.png           # Settings modal
    contact-detail.png     # Contact drawer
  planning/
    improvements.md        # Feature ideas and roadmap notes
```

## License

MIT

---

Developed by [Kashif Aziz](https://kashifaziz.me)
