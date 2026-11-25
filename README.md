# App-Websites

Static GitHub Pages site for App Store support and legal URLs.

## Live URLs

Project Pages base URL:

```text
https://uptonjun.github.io/App-Websites/
```

| App | Purpose | URL |
|---|---|---|
| Notebook Short | Overview | https://uptonjun.github.io/App-Websites/ordio/ |
| Notebook Short | Support | https://uptonjun.github.io/App-Websites/ordio/support/ |
| Notebook Short | Privacy Policy | https://uptonjun.github.io/App-Websites/ordio/privacy/ |
| Notebook Short | Terms of Use | https://uptonjun.github.io/App-Websites/ordio/terms/ |
| ShortGB | Overview | https://uptonjun.github.io/App-Websites/shortgb/ |
| ShortGB | Support | https://uptonjun.github.io/App-Websites/shortgb/support/ |
| ShortGB | Privacy Policy | https://uptonjun.github.io/App-Websites/shortgb/privacy/ |
| ShortGB | Terms of Use | https://uptonjun.github.io/App-Websites/shortgb/terms/ |

The directory slug remains `ordio/` so existing app links, App Store Connect fields, and printed URLs stay valid. Only the visible brand name changed to Notebook Short (formerly CentsCove, originally Ordio).

Use these values in App Store Connect:

- **Support URL:** `https://uptonjun.github.io/App-Websites/ordio/support/`
- **Privacy Policy URL:** `https://uptonjun.github.io/App-Websites/ordio/privacy/`
- **Terms URL (marketing/optional):** `https://uptonjun.github.io/App-Websites/ordio/terms/`

For ShortGB, use:

- **Support URL:** `https://uptonjun.github.io/App-Websites/shortgb/support/`
- **Privacy Policy URL:** `https://uptonjun.github.io/App-Websites/shortgb/privacy/`
- **Terms URL (marketing/optional):** `https://uptonjun.github.io/App-Websites/shortgb/terms/`

## Repository layout

```text
.
├── index.html                 # App directory
├── assets/site.css            # Shared styles
├── ordio/
│   ├── index.html             # App landing page
│   ├── support/index.html
│   ├── privacy/index.html
│   ├── terms/index.html
│   └── assets/icon-256.png
├── shortgb/
│   ├── index.html             # App landing page
│   ├── support/index.html
│   ├── privacy/index.html
│   ├── terms/index.html
│   └── assets/
│       ├── site.css            # Self-contained copy for deployment
│       └── icon-256.png
└── .nojekyll                  # Serve files as-is
```

Every app gets a directory under the repository root with the same four pages and the shared `assets/site.css`.

## GitHub Pages setup

This repository must serve GitHub Pages from the branch root:

1. Open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main** and folder **/ (root)**.
4. Save. The first deployment takes a few minutes.

`.nojekyll` is present, so Jekyll processing is disabled and paths are served directly. All internal links are relative and work under the `/App-Websites/` project path.

## Local preview

```bash
python -m http.server 8000
# http://localhost:8000/
```

## Content rules

- Policies must describe the shipped app, not planned behavior.
- Do not claim a feature or data practice that the app does not implement.
- Keep the effective date and “Last updated” date current.
- Review privacy text whenever app data handling changes.
