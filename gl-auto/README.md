# GL Auto Content Workspace — Vercel

## Deploy

1. Unzip this folder and import it into Vercel as a new project.
2. Framework Preset: **Other**. No build command is required. Output Directory: `public`.
3. Deploy.

The calendar is publicly viewable immediately.

Click any calendar item to edit its title, type, date, time, or channel. Use the month arrows and Today button to navigate. Uploaded scripts appear in the Scripts list; click any script to edit its title, owner, shoot date, or status. Changes are shared after Blob storage is connected.

## Enable shared schedules and script uploads

In the Vercel project, open **Storage**, create a **Blob** store, and connect it to this project. New Vercel projects authenticate Blob through short-lived OIDC credentials automatically. Redeploy once after connecting it.

Without Blob connected, visitors can view the included sample schedule, but adding schedules and uploading scripts remain disabled.

## GL Auto notes

- Use a NEW Blob store for this project. Do not connect the Ang Brothers Blob store: both sites save to the same file path, so sharing a store would overwrite each other's calendar.
- The first month's 9 videos (scripts, shoot and post dates) load automatically the first time the site runs with the new Blob store. They live in `lib/seed.js`.
- The header uses a text logo. To use an image logo, add it to `public/` and replace the `wordmark` span in `public/index.html`.
