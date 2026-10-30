# PlanForge — Offline Checklist Planner

A static, mobile-friendly Progressive Web App (PWA). No framework, database, hosting backend, or account required.

## Included
- Multiple plans (create, edit, switch, delete)
- 18 seeded game-development topics with comprehensive checklist items
- Add/edit/delete topics and checklist items, add notes, mark complete
- Search, filter, expand/collapse, progress stats
- Copy checklist as text; export current plan or all plans as JSON; import backups
- Autosave on the device using `localStorage`
- Installable PWA with offline app shell (after first online load)

## Deploy with GitHub Pages
1. Create a new public GitHub repository (for example `planforge`).
2. Upload the **contents** of this folder into the repository root (not the enclosing folder).
3. In the repository, go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then save.
5. Open the GitHub Pages URL after publishing: `https://YOUR-USERNAME.github.io/planforge/` (replace the example).
6. On Android Chrome, open the site, tap the three-dot menu, then **Install app** or **Add to Home screen** (depending on browser).

## Data and backups
Everything is stored **locally in the browser on each device**. GitHub Pages does not sync your plans. Use **Backup all plans** and **Import backup** to transfer or restore them. Clearing site storage/browser data can erase unbacked-up plans.

## Local testing
For reliable PWA installation/offline testing, serve the folder via localhost rather than opening `index.html` with `file://`. For example: `python -m http.server 8000`, then visit `http://localhost:8000`.

## Notes
The initial checklist is a planning template, not a claim that systems are implemented. Starter vs Future indicates roadmap category, not completed development.

## Nested checklist items
Use the **＋** button beside any checklist item to add a child. Children can have their own children, allowing multi-level trees. Progress, search, JSON import/export, and TXT export include descendants. Existing plans remain compatible; export a backup before deploying updates.
