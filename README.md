# Zoho CRM UI Blueprint
**A pixel-perfect, fully functional Zoho CRM frontend clone for use as a base for CRM projects.**

> This is a UI/design reference implementation. It replicates Zoho CRM's look, feel, and interactions exactly — use it as a starting point for building custom CRM systems.

---

## 🎯 Purpose

This repo serves as the **UI foundation** for all your CRM projects. Instead of building CRM UIs from scratch every time, use this as your base — it has:

- ✅ All 16 Zoho CRM modules fully designed
- ✅ Every button, modal, and interaction working
- ✅ Production-quality HTML/CSS/JS
- ✅ localStorage data persistence
- ✅ Realistic solar industry sample data

---

## 🚀 Quick Start

```bash
# Just open index.html in any browser
open index.html

# Or serve it
python3 -m http.server 8000
# Then visit http://localhost:8000
```

**No build step, no dependencies, no framework.** Pure HTML + CSS + JS.

---

## 📋 Modules Implemented

| Module | Status | Notes |
|--------|--------|-------|
| **Leads** | ✅ Full | List, Detail, Create, Edit, Delete, Clone, Convert |
| **Contacts** | ✅ Full | List, Detail, Create, Edit, Delete, Import |
| **Accounts** | ✅ Full | List, Detail, Create, Edit, Delete |
| **Deals** | ✅ Full | List, Detail, Create, Edit, Delete, Kanban View |
| **Activities** | ✅ Full | Tasks, Events, Calls — List, Detail, Create |
| **Campaigns** | ✅ Full | List, Detail, Create, Launch |
| **Products** | ✅ Full | List, Detail, Create, Edit |
| **Quotes** | ✅ Full | List, Detail, Create, Generate |
| **Sales Orders** | ✅ Full | List, Detail, Create |
| **Invoices** | ✅ Full | List, Detail, Create |
| **Vendors** | ✅ Full | List, Detail, Create |
| **Cases** | ✅ Full | List, Detail, Create |
| **Solutions** | ✅ Full | List, Detail, Create |
| **Dashboards** | ✅ Full | KPI widgets, Charts, Pipeline view |
| **Reports** | ✅ Full | Filterable report list |
| **Settings** | ✅ Full | Module configs, org settings |

---

## 🔘 Buttons & Interactions That Work

### Global Actions
- `+` Add (creates new record)
- 🔔 Notifications panel
- 👤 User menu (profile, settings, logout)
- 🔍 Global search (Ctrl/Cmd + K)
- 🔔 Notifications bell

### Record Actions
- **Save** — saves form data to localStorage
- **Edit** — opens edit modal
- **Delete** — confirms then removes record
- **Clone** — duplicates record with new ID
- **Close** — closes any open modal
- **Cancel** — cancels current action

### Module-Specific
- **Convert Lead** — converts to Contact + Account + Deal
- **Create Quote** — from a Deal
- **Submit for Approval** — workflow action
- **Approve / Reject** — approval response
- **Send Email** — compose email modal
- **Log Activity** — add task/call/event
- **Add Note** — comment/feed item
- **Schedule Meeting** — event creation
- **Launch Campaign** — change status
- **Export** — triggers download
- **Import** — file upload flow
- **Refresh** — reloads list from localStorage
- **Mass Update** — bulk edit selected rows
- **Merge Duplicates** — deduplication UI

---

## 🎨 Design System

### Colors
```
Primary Blue:     #294a85
Accent Orange:    #e8a838
Success Green:    #28a745
Danger Red:       #dc3545
Warning Yellow:   #ffc107
Light BG:         #f5f7fa
White:            #ffffff
Dark Text:        #333333
Border:           #dde3e9
```

### Typography
- **Font:** Roboto (Google Fonts)
- **Headers:** 600 weight
- **Body:** 400 weight
- **Sizes:** 12px (small), 14px (body), 16px (subtitle), 20px (title), 24px (heading)

### Spacing
- Base unit: 4px
- Common: 8px, 12px, 16px, 24px, 32px
- Card padding: 16px
- Modal padding: 24px

---

## 🗂️ Layout Structure

```
┌─────────────────────────────────────────────────────────────┐
│ HEADER (56px)                                               │
│ [Logo] [Module Tabs........] [Search] [Notif] [User Menu]  │
├──────────┬──────────────────────────────────────────────────┤
│ SIDEBAR  │ SUBHEADER                                        │
│ (220px)  │ [View▾] [Filter] [Sort] [+Add] [⋮ Actions]    │
│          ├──────────────────────────────────────────────────┤
│ Module   │                                                  │
│ Nav      │ CONTENT AREA                                     │
│          │                                                  │
│ Collapse │ List View / Detail View / Dashboard / Report    │
│ Button   │                                                  │
│          │                                                  │
└──────────┴──────────────────────────────────────────────────┘
```

---

## 💾 Data

Data persists in **localStorage**. Each module stores records as JSON.

Pre-populated with **solar industry data** (Bangalore context):
- 8 Leads: Solar installation enquiries
- 8 Contacts: Facility managers, ops heads
- 8 Accounts: Residential complexes, commercial buildings
- 8 Deals: Solar panel installations in progress
- 8 Activities: Site visits, follow-ups, calls
- 5 Campaigns: Summer solar drive, commercial outreach
- 8 Products: Solar panels, inverters, batteries
- 5 Quotes: Installation proposals
- And more...

---

## 🔧 Customization

### Add a new module
1. Add module to `SIDEBAR_MODULES` in JS
2. Create schema in `MODULE_SCHEMAS`
3. Add sample data in `INITIAL_DATA`
4. The rest is automatic

### Change colors
Edit the CSS variables at the top of the `<style>` section:
```css
:root {
  --primary: #294a85;
  --accent: #e8a838;
  /* ... */
}
```

### Connect to a real backend
Replace the `localStorage` calls in `saveRecord()`, `getRecords()`, etc. with your API calls.

---

## 📁 Project Structure

```
zoho-crm-ui-blueprint/
├── index.html          ← Everything: HTML, CSS, JS (single file)
├── README.md           ← This file
└── UI-REFERENCE/      ← Zoho UI screenshots for reference
    └── (images from Zoho KB)
```

---

## 📸 UI Reference

This repo pairs with the **PanaceaX-Knowledge-Base** repo which contains:
- 1,036 scraped Zoho CRM KB articles
- 7,118 UI screenshots from actual Zoho CRM
- Full API V8 reference
- Component taxonomy

See: [PanaceaX-Knowledge-Base](https://github.com/abhishekmightcode/On-going-projets-with-hermes/tree/main/PanaceaX-Knowledge-Base)

---

## 📄 License

Internal Use / Personal Projects

---

*Built with Hermes Agent — abhishekmightcode*
