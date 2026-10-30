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

## Deployment-readiness checklist

These are actions to complete before and after publishing, not evidence that a deployment exists or that any checks have passed.

- [ ] Use the repository root as the source directory: it contains `index.html` and `src/`. The published site root must serve `index.html` as the landing page. No separate build output directory or build script is listed for this repository.
- [ ] Include `src/favicon.png` and `src/apple-touch-icon.png` at those relative paths in the published files, or update the corresponding references in `index.html` and verify the replacement paths. Check any other local references before publishing.
- [ ] The page loads Outfit from Google Fonts using external links. Retain network access for those requests if you want that typography, and check the page's fallback appearance if the font resource is unavailable.
- [ ] No `.env.example` or separate configuration file is listed. Do not invent environment variables or add credentials to `index.html` or other tracked assets. Browser-delivered content is visible to visitors.
- [ ] Before publishing, open the page locally and check its layout, icons, font behavior, and visible links. The landing page's feature descriptions do not establish that the separate player features work here.
- [ ] After publishing, open the published page in a browser. Confirm that `index.html` renders, local icons load, and the visible download, source, and other links lead to their intended destinations. Inspect the browser Console and Network panel for failed requests; distinguish local asset paths from Google Fonts requests.
- [ ] Review the published page at narrow and desktop-sized viewports, and try its visible links and controls. Record any issues; no compatibility or deployment results are recorded here.

## Contributor handoff

Keep changes focused on the landing page or its supporting files in `src/`. Preserve existing filenames and relative references, including the icon paths, unless a move or rename is necessary; update the references in `index.html` if paths change. Summarize what changed and which files were affected. Manually review the page before publishing; the checklist above describes review actions, not results already verified.

## Troubleshooting

These are diagnostic steps, not reports of known problems.

1. Confirm that `index.html` is the page being opened or served, with `src/` available alongside it.
2. If the icons do not load, check that `src/favicon.png` and `src/apple-touch-icon.png` exist at the referenced relative paths. Preserve those paths when moving files, or update the references in `index.html`.
3. Inspect the browser Console and Network panel for errors and failed requests. The icons are local assets; Outfit is loaded from Google Fonts (`fonts.googleapis.com` and `fonts.gstatic.com`) and therefore depends on network access. Check the failed request URL to distinguish a missing local file from an unavailable external font, and review the fallback typography if the font cannot load.

## Configuration and data handling

This repository is a static page; its listed files do not include an `.env.example` or separate configuration file. Do not put credentials, private tokens, or personal data in `index.html` or other tracked assets. HTML and browser-delivered values are visible to visitors and cannot be secret. The Google Fonts links are remote resource references, not a place to store credentials. If you add a configuration template, use placeholders only and do not commit real local values. The landing page's links and feature descriptions do not establish how the separate app handles user data.

## Browser and asset review checklist

These are review actions, not verified results or performance measurements. No browser compatibility testing is recorded here.

- [ ] Open the page in current versions of browsers relevant to its audience. Record browser and version when reporting an issue.
- [ ] Compare a narrow mobile-sized viewport with a desktop-sized viewport. Check text wrapping, layout, and whether download, source, and other visible links remain usable.
- [ ] Try the download and source links and any other visible controls; confirm each leads to its intended destination. The landing page's feature descriptions do not establish that player features work here.
- [ ] Before publishing edits, review tracked files for accidentally added credentials or private data. Anything included in this static page is available to visitors.

## Accessibility review checklist

These are future browser checks, not compliance claims or verified results:

- [ ] Use Tab and Shift+Tab to reach visible links and controls. Check keyboard order, operation, and visible focus indicators.
- [ ] Check that link text communicates its destination or action, and review text, link, and control contrast.
- [ ] If meaningful imagery is present or added, check its text alternative; treat decorative imagery accordingly. If motion is present or added, check reduced-motion behavior.

No review results are recorded here; complete the checklists in a browser after making changes.