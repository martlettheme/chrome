# Martlet for Chrome

## Test locally

Run `npm run build`. Open `chrome://extensions`, enable Developer mode, choose **Load unpacked**, and select `themes/light` or `themes/dark`. Only one Chrome theme is active at a time. These themes color browser chrome and new-tab surfaces; they do not recolor websites.

## Packages

Build produces `dist/martlet-light-chrome.zip` and `dist/martlet-dark-chrome.zip`, each with manifest.json at its root. These are Chrome Web Store upload archives, not one-click signed installers. They contain no scripts, permissions, tracking, fonts, or remote assets. Manifest V3. Store registration, listing screenshots, review, and publication remain to do. Chrome may retain system colors on browser-controlled surfaces.

These are generated distributions of [Martlet Theme](https://martlettheme.dev/), version 1.0.0. Canonical colors and generators live in [martlettheme/martlettheme](https://github.com/martlettheme/martlettheme). The source repository may require maintainer access. This repository includes a complete color snapshot in source.json and can build without access to that repository.

MIT license. Copyright 2026 James P. Howard, II.

## Maintenance

Edit the canonical palette and generator upstream, then run npm run build there. The complete distribution directories are emitted under artifacts/repositories/. Sync the relevant directory into this repository. To reproduce a snapshot here, run npm run build, then npm test. Node.js 22 or newer is used in CI. No registry publication runs automatically.
