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


## Customizable checklist (v5)
- Settings: six themes, custom accent, density, checkbox styles, expand icons and independent text/icon/row/indent sizes.
- Nested task collapse/expand and note previews; bookmark tasks and filter bookmarks; optional reminder text.
- Drag and drop to reorder tasks within the same parent list on desktop.
- All preferences stored separately in localStorage (`planforge.preferences.v2`); task data remains in `planforge.v1`.
- Reminder values are saved as labels only; automatic notifications are not implemented.


## Version 6: Custom scopes and saved color presets

- Settings now allows editing scope labels and colors, and creating unlimited custom scopes.
- Scope filters include custom scopes. Imported JSON keeps scope IDs, including unknown scopes.
- Settings supports custom page, panel, card, text, border and accent colors with live preview.
- Save, apply, rename, duplicate, and delete any number of named color presets.
- Preferences and scope definitions are stored locally on each browser/device; JSON plan exports include topic scope IDs but do not export device theme presets.
- Built-in Starter/Future scope IDs cannot be deleted for backwards compatibility. Scopes assigned to any topic cannot be deleted until reassigned.
