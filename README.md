# Aurix_Launch

Aurix_Launch is the public-facing landing page for **Aurix**, a music player presented around the idea of listening without limits. The page introduces the app, highlights its listening experience, and provides links for downloading the app and exploring its source.

The product highlights described on the page include music search, a personal library, lyrics, and offline listening. These are marketing descriptions of the app; the landing page itself is not the Android player.

## Preview locally

This is a static website. Open index.html in a modern browser, or serve the repository over HTTP:

    python -m http.server 8000

Visit http://localhost:8000 to preview the page.

## Project files

The main page lives in index.html, with supporting visual assets under src/. Keep asset paths relative to the page and check the download/source links whenever those destinations change. The layout is designed as a product landing page, so edits should keep the app introduction, feature highlights, and primary links easy to follow.
