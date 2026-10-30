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

## Asset and loading review checklist

These are review actions, not verified results or performance measurements:

- [ ] Confirm `src/favicon.png` and `src/apple-touch-icon.png` exist at the paths referenced by `index.html`. Inspect any other image, audio, video, or font paths in the page and verify their local files.
- [ ] Check whether assets in `src/` are still used before removing them; verify references in `index.html` and any relevant stylesheets first.
- [ ] Look for unusually large images or other media relative to their displayed role. Consider resizing or compressing where appropriate, then inspect the page to ensure the result remains suitable.
- [ ] The page references Outfit through Google Fonts (`fonts.googleapis.com` and `fonts.gstatic.com`). Confirm this external font dependency is intentional, and check the page's typography and fallback if the remote font is unavailable.
- [ ] Inspect script references, if any, and confirm each external or local script is intentional and needed.

## Manual review checklist

These are actions to perform, not verified results:

- [ ] Open `index.html` in a browser, or start the local server above and open its address.
- [ ] Check that the favicon and touch-icon paths resolve and review other image or media references in `index.html` for missing files.
- [ ] Try the download and source links and any other visible links or controls; check that each leads to its intended destination. The landing page's feature descriptions do not establish that player features work here.
- [ ] Inspect the layout at narrow and wide viewport widths, including text wrapping and link usability.

## Accessibility review checklist

These are future browser checks, not compliance claims or verified results:

- [ ] Use Tab and Shift+Tab to reach the download, source, and any other interactive links or controls. Check that the keyboard order is logical and each control is usable without a pointer.
- [ ] Confirm each focused link or control has a visible focus indicator against the landing page's styling.
- [ ] Check that link text communicates its destination or action; do not rely on visual appearance or an icon alone to explain a control.
- [ ] Check contrast for the page text, links, and controls against their backgrounds, including at narrow viewport widths.
- [ ] If meaningful imagery is present or added to `index.html` or `src/`, check that it has an appropriate text alternative; treat decorative imagery as decorative.
- [ ] If motion or animated effects are present or added, check that they respect the browser or operating system's reduced-motion preference.

No review results are recorded here; complete the checklists in a browser after making changes.