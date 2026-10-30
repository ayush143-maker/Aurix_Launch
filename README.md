# Aurix_Launch

Aurix_Launch is a static promotional landing page for the Android music player Aurix. It advertises music search, playlists, artists, albums, favorites, lyrics, and downloads for offline playback; the player features are descriptions of a separate app, not functionality implemented by this page.

## Preview locally

Open `index.html` in a browser, or serve the repository over HTTP:

```sh
python -m http.server 8000
```

Visit [http://localhost:8000](http://localhost:8000). For static hosting, publish `index.html` and its supporting files in `src/` together, preserving their relative paths.

## Download and installation

The page displays Android, version 7.1.0, a size of 104 MB, and an October 2026 release date, and links to the Aurix GitHub repository and an APK. The download script currently assigns every download link a hard-coded GitHub APK URL. If that constant is emptied, the script can instead query GitHub’s latest-release API for the first `.apk` asset and update the links and displayed size. Request failures are silently ignored. Check the actual published destination and release metadata before distributing the page; the displayed information is not independent verification that an APK is available or current.

The install section includes Android-specific steps and a troubleshooting note for the “track couldn't be resolved” message. Review those instructions against the current release process before publishing.

## Page behavior and assets

Scrolling updates the top progress indicator, and sections reveal as they enter view; browsers without `IntersectionObserver` get an immediate-reveal fallback. A canvas draws a changing ECG-like waveform while visible, except when reduced motion is requested. On narrow screens, screenshots drift horizontally and pause during touch or pointer interaction before resuming after a delay. Most screenshots load lazily.

The page references local assets under `src/`, including its logo, favicon, Apple touch icon, share image, and screenshots. Keep those files and paths in sync with references in `index.html`. Outfit is loaded from Google Fonts, so that typography requires network access. Edit the copy, styling, links, and asset references in `index.html`. The page’s scripts do not provide a music player or local storage for music or settings.