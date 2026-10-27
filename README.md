# gEOregula Project Dashboard

Interactive project control dashboard for the ESA Business Applications project gEOregula (AO10494), run by Space4Good B.V.

Single static page, no build step. Tabs: Overview, Deliverables, Work Packages, Gantt Chart, Monthly Activities, Team.

## Confidentiality

The page embeds contract values, payment milestones and personnel allocations. Treat it as Space4Good internal material. Use a **private** repository. Note that GitHub Pages on a private repository needs a paid GitHub plan (Pro, Team or Enterprise Cloud). On a free plan, Pages only serves public repositories, so do not publish there.

## Publish on GitHub Pages

1. Create a new repository on GitHub (private).
2. Upload the contents of this folder (`index.html`, `.nojekyll`, `README.md`, `.gitignore`) to the repository root.
3. Go to Settings > Pages. Under "Build and deployment", choose "Deploy from a branch", select the `main` branch and the `/ (root)` folder, then Save.
4. After a minute the site is live at `https://<your-org-or-user>.github.io/<repository-name>/`.

## Run locally

Open `index.html` in a browser. No server needed.

## How data is saved

Deliverable statuses, notes, activity checkboxes, highlighted activities, monthly WP statuses and the dashboard clock are stored in the browser's localStorage. They are per browser and per device, and are not shared between people. Clearing site data resets them.

## Updating the plan

All dates, work packages, personnel hours and payments are defined in constants at the top of the `<script>` block in `index.html` (`MILESTONES`, `ADVANCE_PAYMENT`, `WORK_PACKAGES`, `WP_PERSONNEL`, `TEAM`, `DELIVERABLES`). Edit them there and commit.

## Open points in the source data

- The signed contract payment dates fall on the 3rd of the month, which implies a 3 September 2026 kick-off. The dashboard uses 7 September 2026, 11:00 as confirmed by the project lead.
- BDR has no payment in the signed contract, and its date (KOM+3 months) comes from the revised work package descriptions, not from the contract.

## External resources

Fonts (Poppins, Inter, JetBrains Mono) load from Google Fonts. Without internet the page falls back to system fonts.
