# willwhipple.github.io

Public pages for all my apps: privacy policies, support pages, and anything else App Store Connect or users need a URL for. App source code stays in each app's own private repo.

Live at https://willwhipple.github.io

## Layout

```
index.html          List of apps (add each new app here)
assets/style.css    Shared styling, light and dark mode
<app-slug>/
  privacy/index.html   → https://willwhipple.github.io/<app-slug>/privacy/
  support/index.html   → https://willwhipple.github.io/<app-slug>/support/
_template/          Starting point for a new app (not published)
```

## Adding a new app

1. Copy `_template/` to a new folder named with the app's slug (lowercase, no spaces), e.g. `cp -R _template myapp`.
2. Replace `APP_NAME`, `APP_SLUG`, and the effective date in both pages.
3. **Rewrite the privacy policy to match what the app actually does.** The template assumes no data collection, on-device storage, and optional iCloud sync. If the app uses analytics, accounts, a server, ads, or third-party SDKs, say so, and keep it consistent with the app's App Store privacy labels and `PrivacyInfo.xcprivacy`.
4. Rewrite the support FAQ for the app.
5. Add the app to `index.html`.
6. Commit and push. GitHub Pages updates within a minute or two.

Folders starting with `_` aren't published, which is why `_template/` stays private.
