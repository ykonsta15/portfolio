# Central Portfolio (Astro)

A central portfolio website that lists your deployed apps and links to each app + repository.

## Stack

- Astro
- Static JSON data source: `src/data/projects.json`
- Client-side search
- Minimalist cards with publication date + links

## Local development

```bash
npm install
npm run dev
```

Then open `http://localhost:4321`.

## Build and preview

```bash
npm run build
npm run preview
```

## Deploy to Vercel

1. Push this repo to GitHub.
2. In Vercel, click **Add New Project** and import the GitHub repo.
3. Use these build settings:
   - Framework Preset: `Astro`
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Install Command: `npm install`
4. Click **Deploy**.

Vercel will automatically redeploy on every push to your main branch.

## Add a new app

1. Open `src/data/projects.json`.
2. Add one new project object with this schema:

```json
{
  "title": "Project Name",
  "description": "Short summary",
  "publishedAt": "2026-03-02",
  "appUrl": "https://your-app-url.vercel.app",
  "repoUrl": "https://github.com/your-username/your-repo"
}
```

3. Commit and push. Vercel will redeploy automatically.

## Notes

- `publishedAt` should use ISO format (`YYYY-MM-DD`) so sorting works correctly.
- Update `site` in `astro.config.mjs` to your final production domain for fully accurate OpenGraph URLs.
