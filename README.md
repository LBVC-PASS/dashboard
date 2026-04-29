# dashboard
# Safety & Security Services
## Operations Dashboard

A personal operational dashboard for tracking all active projects, policy development, procurement, facilities, and municipal work. Built as a static HTML file, version-controlled via Git, and updated through Claude Code.

---

## Live Dashboard

> **URL:** `https://[your-username].github.io/[repo-name]/`
> *(Update this once GitHub Pages is enabled)*

---

## How It Works

The dashboard is a **single static HTML file** (`index.html`). All data lives directly in the JavaScript at the top of that file — no backend, no database, no server required.

**The browser UI is read-only for display purposes.** Interactive elements (checkboxes, notes, status badges) show a session-only preview and prompt you to commit changes via Claude Code. Nothing typed or clicked in the browser persists after the tab is closed.

**Claude Code is the pen.** All permanent updates are made by referencing a project ID in Claude Code, which edits the file and commits it to GitHub. GitHub Pages then auto-deploys the change in seconds.

---

## Project ID System

Each project has a unique ID based on its area:

| Prefix | Area |
|--------|------|
| `SEC-` | Security & Safety Services |
| `PRC-` | Procurement |
| `FAC-` | Facilities |
| `MUN-` | Municipal (Sainte-Marthe-sur-le-Lac) |

IDs are sequential within each prefix: `SEC-001`, `SEC-002`, `PRC-001`, etc.

---

## Updating via Claude Code

Reference a project by its ID. Examples:

```
SEC-003 is now Active
```
```
SEC-005 — milestone "Draft GO" is done
```
```
Add to PRC-001 notes: Vendor confirmed delivery for May 15
```
```
New SEC item: GO Evidence Handling, high priority, scope is chain of custody for Genetec Vault exports
```
```
SEC-007 status → Done
```
```
SEC-002 — question "Who handles supervisory review?" is resolved
```

Claude Code will edit `index.html` directly and commit the change to this repo.

---

## Repo Structure

```
/
├── index.html        # The entire dashboard (data + UI in one file)
├── README.md         # This file
├── LICENSE           # All Rights Reserved
└── .gitignore        # Standard ignores
```

---

## GitHub Pages Setup

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Under **Source**, select `Deploy from a branch`
4. Select branch: `main`, folder: `/ (root)`
5. Click **Save**
6. Your dashboard will be live at `https://[username].github.io/[repo-name]/` within ~60 seconds

---

## Access

The repo is **public** — anyone with the URL can view the dashboard. The source code is visible but **All Rights Reserved** — it may not be reused, copied, or adapted without explicit permission.

If you need to restrict access to the live dashboard in the future, options include:
- Switching the repo to **private** (requires GitHub Pro, ~$4 USD/month)
- Adding HTTP basic auth via a third-party service (Cloudflare Access — free tier available)

---

## Tabs

| Tab | Prefix | Contents |
|-----|--------|----------|
| Security | SEC | General Orders, SOPs, IACLEA accreditation work |
| Procurement | PRC | Active procurements, board motions |
| Facilities | FAC | Capital projects |
| Municipal | MUN | Council, CCU, constituent work |
| ✓ Completed | — | Universal archive of all completed projects, grouped by year and origin |

---

## Yearly Review

Completed projects are automatically archived to the **Completed** tab when marked Done, grouped by completion year and origin area. To restore a project for annual review, use the **↩ Restore** button in the Completed tab or tell Claude Code:

```
Restore SEC-004 for annual review
```

---

## Contact

Coordinator, Safety & Security Services — 
