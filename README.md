TaskFlow
A modern, installable task manager built as a single-page Progressive Web App (PWA). No backend, no build tools — open it in a browser or install it like a native app.
Live app: https://shreehari005.github.io/TaskFlow/
---
Files in this repo
File	Purpose
`index.html`	The entire app — UI, styling, and logic all in one file. This is the only file that does the actual work.
`manifest.json`	Tells the browser this is an installable app — sets the app name, icon, and colors shown when installed on a phone/laptop.
`sw.js`	Service worker — caches the app's files so it still opens (and tasks load) even without internet.
`icon-192.png`	App icon (small size) — shown on phone home screens.
`icon-512.png`	App icon (large size) — used for app stores/splash screens and high-res displays.
> All 5 files must stay in the same folder. They reference each other by filename.
---
Features
Task management
Add, edit, delete, duplicate tasks
Mark complete/incomplete
Bulk-clear completed tasks
Organization
Custom categories with color tags
Priority levels: High / Medium / Low
Tags, instant search, filter by status/priority/category/due date
Due dates
Set due dates, see overdue tasks highlighted in red
Productivity tracking
Dashboard: total tasks, completion %, overdue count, day streak
Today / This Week / Overdue / Completed views
Experience
Drag-and-drop reordering
Dark/light mode toggle
Keyboard shortcuts: `/` search, `N` new task, `D` dark mode
Toast notifications for every action
Data
Saved locally in your browser (`localStorage`) — private to your device
Automatic backup copy kept alongside main data
Export tasks as JSON, CSV, or PDF
---
How it stores data
TaskFlow has no server and no database. All tasks live in your browser's `localStorage` — similar to how a Notes app saves drafts on your phone without needing internet. This means:
Your tasks stay on the device/browser you use
Clearing browser data will erase tasks (use the Export buttons to back up first)
Tasks won't automatically sync across devices
---
Running it locally
No installation needed:
Download all 5 files into one folder
Double-click `index.html` to open it in your browser
For the install-as-app feature to work, it must be served over HTTPS (a browser security requirement) — opening the file directly won't show the install option. That's why it's hosted on GitHub Pages.
---
Installing as an app
Once visiting the live link above:
Android/Chrome: Menu (⋮) → "Add to Home screen" / "Install app"
iPhone/Safari: Share icon → "Add to Home Screen"
Desktop (Chrome/Edge): Click the install icon (⊕) in the address bar
---
Tech stack
Plain HTML, CSS, and JavaScript — no frameworks, no build step. PDF export uses the jsPDF library loaded from a CDN.
---
Future improvements
Cloud sync (Firebase/Supabase) so tasks follow you across devices
Push notification reminders
Recurring tasks
Subtasks/checklists within a task
Multi-user shared task lists
