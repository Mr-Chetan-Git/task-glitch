TaskGlitch – SDE Bug Fix Assignment

TaskGlitch is a task management web application designed for sales teams to track, prioritize, and analyze tasks based on ROI (Return on Investment).

This repository contains fixes for multiple functional and UX bugs identified in the original implementation.

---

Live Demo

👉 https://task-glitch-chetans-projects-7f3af693.vercel.app

(Deployed on Vercel – publicly accessible)

---

 Tech Stack

- React (TypeScript)
- Vite
- Material UI (MUI)
- Context API + Custom Hooks
- Vercel (Deployment)

---

 Bugs Fixed

 Bug 1 – Double Fetch Issue
- Prevented duplicate API calls on initial page load.
- Ensured tasks are fetched exactly once.
- Removed unintended secondary fetch logic.

Bug 2 – Undo Snackbar Bug
- Fixed issue where snackbar did not auto-close.
- Ensured deleted task state resets when snackbar closes.
- Undo now works only during active snackbar window.

 Bug 3 – Unstable Sorting
- Removed random sorting behavior.
- Added deterministic tie-breaker for tasks with same ROI and priority.
- Sorting is now stable across re-renders.

✅ Bug 4 – Double Dialog Opening
- Fixed event bubbling issue in task rows.
- Ensured only the intended dialog opens (View / Edit / Delete).
- Prevented overlapping dialogs.

 ✅ Bug 5 – ROI Calculation Errors
- Handled division by zero and invalid inputs safely.
- Prevented NaN / Infinity values.
- Ensured consistent numeric formatting.

 Setup Instructions

```bash
npm install
npm run dev
