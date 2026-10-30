# PlanForge

**Your project workspace — plan, organize, and track what matters.**

PlanForge is a free, offline-first checklist planner for projects of any size. Break big ideas into topics, tasks, and deeply nested subtasks; track progress; keep notes; and tailor the interface to your workflow.

Built as a responsive Progressive Web App (PWA) using **HTML, CSS, and vanilla JavaScript**. No account, subscription, database, or backend is required.

## Highlights

- **Multiple plans:** Create, rename, describe, switch between, and delete plans.
- **Topics and custom scopes:** Organize tasks into topics with color-coded labels such as Starter, Future, or your own custom scopes.
- **Nested checklists:** Create children and subchildren, expand or collapse branches, and track completion across descendants.
- **Task controls:** Tick a checkbox to complete a task. Select a task's text/card to open its **Edit / Delete** menu. Separate bookmark and note icons provide quick access.
- **Task notes:** View notes in a focused popup over a blurred backdrop. Click **X** to close directly, or click the backdrop to receive a **Close this note?** confirmation. Edit notes from the popup.
- **Bookmarks and reminders:** Mark important tasks and save optional reminder text/date information.
- **Progress tracking:** See topic counts, total checklist items, completed items, and completion percentages.
- **Search and filters:** Find tasks, filter by completion or scope, and view bookmarks.
- **Flexible appearance:** Choose themes, checkbox styles, expand/collapse icons, spacing, text sizes, indentation, and optional interface elements.
- **Custom color presets:** Adjust interface colors and save, apply, rename, duplicate, or delete named presets.
- **Import and export:** Copy checklists, export a plan as JSON or TXT, back up all plans as JSON, and import a plan as new or replace an existing plan.
- **Responsive PWA:** Works in desktop, tablet, and phone browsers; installable on supported devices, with offline app-shell caching after an initial successful load.

## Getting started

1. Open PlanForge in your browser.
2. Create a plan or select an existing plan.
3. Add topics, then checklist items and nested child tasks.
4. Use the checkbox to mark work complete. Use the task row to edit or delete.
5. Open **Settings** to personalize the interface.
6. Use **Backup all plans** regularly to save a JSON copy.

## Task notes and actions

| Action | Behavior |
| --- | --- |
| Click a task checkbox | Toggle completion |
| Click a task's text/card | Open task options: **Edit** and **Delete** |
| Click a task's note icon | Open its note popup |
| Click **X** in a note popup | Close the note immediately |
| Click the blurred background | Ask **Close this note?**; choose **Keep Open** or **Yes, Close** |
| Click **Edit** in the note popup | Edit the task and its note |
| Choose **Delete** from task options | Ask for confirmation before deleting the task and its children |

On smaller screens, some task actions may be grouped into a compact menu.

## Appearance and personalization

Open **Settings** to customize:

- Themes: Light, Dark, Neutral, Blue, Green, and Purple
- Accent and individual interface colors
- Named custom color presets
- Checklist density and checkbox appearance
- Expand/collapse icon style
- Task text, note text, icon size, row height, and child indentation
- Optional bookmarks, reminders, child progress, and animations
- Topic scope names and colors

**Note:** Plans and appearance preferences are saved in the browser on the current device. Saved theme presets and custom scope definitions are not automatically synchronized between devices.

## Data, privacy, and backups

PlanForge uses browser `localStorage` for plan data and settings. Your checklists are not automatically uploaded to a server, and there is no built-in account sync.

**Back up before clearing browser data, changing phones, or updating your deployment.** Clearing website storage may permanently erase plans that have not been exported.

- **Export plan → JSON:** Importable PlanForge plan
- **Export plan → TXT:** Human-readable checklist
- **Backup all plans:** JSON backup of all plans
- **Import plan / update:** Import as a new plan or replace an existing plan (replacement overwrites the selected plan)

Custom theme presets and device preferences are not included in standard plan JSON exports.

## Install on a device

Visit your published PlanForge URL using a supported browser. On Android Chrome, open the browser menu and choose **Install app** or **Add to Home screen**, if offered.

PWA installation depends on the browser and device. Offline use requires that the app resources have already been cached; imported/exported files and data backups remain your responsibility.

## Deploy with GitHub Pages

1. Create a public GitHub repository.
2. Upload `index.html`, `app.js`, `data.js`, `style.css`, `manifest.webmanifest`, `sw.js`, and the `icons/` directory to the repository root.
3. Open **Settings → Pages** in GitHub.
4. Select **Deploy from a branch**, choose `main` and `/ (root)`, then save.
5. Wait for deployment and visit `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

For the `atk-ho/PlanForge` repository, the expected URL is:

**https://atk-ho.github.io/PlanForge/**

For subsequent updates, replace **only the files that changed**, unless a release explicitly requires more files. Your browser may briefly serve cached PWA assets; refresh after deployment.

## Run locally

You can serve the project folder with Python:

```bash
python -m http.server 8000
```

Then visit **http://localhost:8000**.

For PWA/service-worker testing, use localhost or HTTPS rather than opening `index.html` directly via `file://`.

## Project structure

```text
PlanForge/
├── index.html             # Application markup
├── style.css              # Layout, themes, and responsive styles
├── app.js                 # Planner logic and interactions
├── data.js                # Starter/sample plan data
├── manifest.webmanifest   # PWA metadata
├── sw.js                  # Offline app-shell cache
├── icons/                 # App icons
└── README.md              # Project documentation
```

## Current limitations

- **No cloud sync or collaboration:** Data is stored per browser/device.
- **No scheduled reminder notifications:** Reminder information is saved, but notifications are not sent automatically.
- **Desktop-first drag-and-drop:** Reordering works best with a mouse; touch reordering may be limited.
- **Browser storage limits apply:** Large plans or disabled/cleared storage can affect saving.
- **PWA behavior varies:** Installation and offline support depend on browser/device capabilities.

## Roadmap ideas

Potential future improvements (not currently promised as implemented):

- Touch-friendly drag-and-drop reordering
- Optional reminder notifications
- Portable export/import of appearance presets and custom scopes
- Accessibility and keyboard-navigation improvements
- More advanced note formatting and attachments

## Built for flexible planning

Use PlanForge for software projects, schoolwork, study plans, personal goals, event preparation, business workflows, game development, or anything else that benefits from a structured checklist.

**PlanForge — Turn plans into progress.**
