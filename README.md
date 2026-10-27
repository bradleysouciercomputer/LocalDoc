# LocalDoc

LocalDoc is a small, local-first document editor built with Google's official **Material Web** components (`@material/web`), designed for static hosting on GitHub Pages.

## Features

- Create and edit documents with rich-text formatting, headings, quotes, lists, alignment, and links.
- Start from blank, meeting notes, project plan, or letter templates.
- Automatically save edits in this browser's local storage.
- Search documents, star favorites, move documents to trash, restore them, or permanently delete them.
- Duplicate documents, export a document as HTML, print / save as PDF, and import or export a JSON backup.
- Light and dark themes.
- Responsive layout for desktop and mobile.

## GitHub Pages setup

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. The included workflow in `.github/workflows/pages.yml` deploys the static site on pushes to `main`. You can also run it from the Actions tab with **Run workflow**.

After the first successful deployment, GitHub will show the published site URL under **Settings → Pages** and in the workflow run.

## Run locally

Because LocalDoc is a static app, you can serve the repository root with any local static HTTP server. For example, with Python installed:

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Data and privacy

Documents are stored in the current browser's `localStorage`. There is no backend and no account system. Clearing browser site data can delete documents, so use **Export backup** regularly if the documents matter to you. Exported backup files can be brought back with **Import backup**.

The **Copy document link** action copies a browser URL that opens the same locally stored document on this browser profile. It does not upload or share document contents with anyone else.

The official Material Web components and Google Fonts are loaded from external CDNs, so the page needs an internet connection to load those dependencies.

## Technology

- HTML, CSS, and JavaScript modules
- Official Google Material Web components via the `@material/web` ESM CDN import map
- Browser local storage for document persistence
- GitHub Pages for static hosting
