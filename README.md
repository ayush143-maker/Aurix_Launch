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

## Browser and asset review checklist

These are review actions, not verified results or performance measurements. No browser compatibility testing is recorded here.

- [ ] Open the page in current versions of browsers relevant to its audience. Record browser and version when reporting an issue.
- [ ] Inspect the browser Console and Network panel. Investigate JavaScript errors, failed local or remote requests, and unexpected warnings.
- [ ] Confirm `src/favicon.png` and `src/apple-touch-icon.png` exist at the paths referenced by `index.html`. Check other local asset references against the repository files. Verify that remote resource URLs are intentional and reachable.
- [ ] Outfit is loaded from Google Fonts (`fonts.googleapis.com` and `fonts.gstatic.com`). Check the page's typography and fallback appearance if the remote font does not load.
- [ ] Compare a narrow mobile-sized viewport with a desktop-sized viewport. Check text wrapping, layout, and whether download, source, and other visible links remain usable.
- [ ] Try the download and source links and any other visible controls; confirm each leads to its intended destination. The landing page's feature descriptions do not establish that player features work here.

## Accessibility review checklist

These are future browser checks, not compliance claims or verified results:

- [ ] Use Tab and Shift+Tab to reach visible links and controls. Check keyboard order, operation, and visible focus indicators.
- [ ] Check that link text communicates its destination or action, and review text, link, and control contrast.
- [ ] If meaningful imagery is present or added, check its text alternative; treat decorative imagery accordingly. If motion is present or added, check reduced-motion behavior.

No review results are recorded here; complete the checklists in a browser after making changes.