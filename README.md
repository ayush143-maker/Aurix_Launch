# Aurix_Launch

Aurix_Launch is a static HTML landing page for **Aurix**, a music player. Visitors can read about the app and follow links to downloads and its source. The page describes features including music search, a personal library, lyrics, and offline listening; these descriptions are about the app, not features implemented by this landing page. It is not the Android player itself.

## Preview locally

Open `index.html` in a browser, or serve the repository over HTTP:

    python -m http.server 8000

Visit http://localhost:8000. No deployment provider or procedure is documented. To host the landing page, serve `index.html` and the supporting files in `src/` together as static files.

## Making and reviewing changes

`index.html` is the main page, and `src/` contains supporting visual assets. After editing, reload the page in your browser and check that the layout, asset paths, and download or source links appear and work as intended. If an asset is missing, check that its path in the page matches the file in `src/`. Keep asset paths and links up to date.