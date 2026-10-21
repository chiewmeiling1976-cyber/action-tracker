# Meeting Action Tracker

A single-page app for teams that keep forgetting what they agreed in meetings.

- Add an action with an owner and a due date
- Actions are grouped by owner, each with a tick box for done
- Open, done and overdue counts at the top; overdue actions are highlighted in red
- Filter by All, Open, Overdue or Done

Everything is in one file, `index.html`. There is no build step and no dependencies.

## Where the data lives

Actions are saved in the browser's local storage. That means each person's list stays on their own device and browser; teammates opening the same link will not see each other's actions. Clearing browser data removes the list.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Deploy to Vercel

1. In Vercel, choose **Add New → Project** and import this GitHub repository.
2. Leave **Framework Preset** as **Other**. Leave the build command and output directory empty.
3. Click **Deploy**.

Every push to `main` redeploys automatically. `vercel.json` adds a few standard security headers and makes sure the page is never served stale after an update.
