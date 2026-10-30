# Aurix_Launch

Aurix_Launch is a static HTML landing page for **Aurix**, a music player. It presents information about the app, including descriptions of music search, a personal library, lyrics, and offline listening, along with download and source links. These descriptions are about the separate app; they do not mean the landing page implements those features. This is not the Android player itself.

## Preview locally

Open `index.html` in a browser, or serve the repository over HTTP:

```sh
python -m http.server 8000
```

Visit [http://localhost:8000](http://localhost:8000). To host the page, serve `index.html` and the supporting files in `src/` together as static files.

## Customize

Edit the landing-page copy and presentation in `index.html`. The page references `src/favicon.png` and `src/apple-touch-icon.png`; keep these files at those paths or update the references if they move. Outfit is loaded from Google Fonts, so those font requests require network access if you want to retain the current typography.

## File references

- `index.html` — landing-page entry point, content, and asset references.
- `src/favicon.png` — favicon referenced by the page.
- `src/apple-touch-icon.png` — Apple touch icon referenced by the page.

The visible download and source links should be checked at their published destinations. The page’s copy and links do not establish how the separate app works or handles user data.