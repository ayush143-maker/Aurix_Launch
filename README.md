# Aurix_Launch

Aurix_Launch is a static HTML landing page for **Aurix**, a music player. Visitors can read about the app and follow links to downloads and its source. The page describes features including music search, a personal library, lyrics, and offline listening; these are descriptions of the app, not features implemented by the landing page. This is not the Android player itself.

## Preview locally

Open `index.html` in a browser, or serve the repository over HTTP:

```sh
python -m http.server 8000
```

Visit [http://localhost:8000](http://localhost:8000). To host the landing page, serve `index.html` and the supporting files in `src/` together as static files.

## Personalize

Edit the landing-page copy and presentation in `index.html`. The page references `src/favicon.png` and `src/apple-touch-icon.png`; keep those files at those paths, or update the corresponding references in `index.html` if you replace or relocate them. The page also loads Outfit from Google Fonts, so retain its font links if you want to keep that typography.

## Manual review checklist

These are actions to perform, not verified results:

- [ ] Open `index.html` in a browser, or start the local server above and open its address.
- [ ] Check that `src/favicon.png` and `src/apple-touch-icon.png` resolve. Inspect any other image or media references in `index.html` and confirm their files are available at the referenced paths.
- [ ] Try the download and source links and any other visible links or controls; check that each leads to its intended destination. The landing page's feature descriptions do not establish that player features work here.
- [ ] Inspect the layout at narrow and wide viewport widths, including text wrapping and link usability.
- [ ] If reviewing typography, check how the page appears with its Google Fonts links available; the page references Outfit from Google Fonts.

No review results are recorded here; complete the checklist in the browser after making changes.