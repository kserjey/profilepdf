# profilepdf-site

Public pages for the ProfilePDF Chrome extension, served by GitHub Pages (Jekyll, no build step).

| Page      | URL                                               | Used for                                    |
| --------- | ------------------------------------------------- | ------------------------------------------- |
| Home      | `https://kserjey.github.io/profilepdf/`           | manifest `homepage_url`, welcome page       |
| Privacy   | `https://kserjey.github.io/profilepdf/privacy/`   | store dashboard, options page `PRIVACY_URL` |
| Support   | `https://kserjey.github.io/profilepdf/support/`   | popup `SUPPORT_URL`, store support link     |
| Changelog | `https://kserjey.github.io/profilepdf/changelog/` | release notes                               |

## Publish

1. Create a **public** repo named `profilepdf` and push this folder to it.
2. Settings → Pages → Source: _Deploy from a branch_, `main`, `/ (root)`.

## Keep in sync with the extension

`privacy.md` describes the extension's actual behaviour. Update it, and its "Last updated" date,
whenever any of these change:

- the telemetry events and properties (`src/core/telemetry-schema.ts`);
- what is stored locally (`src/core/telemetry.ts`);
- the permissions (`public/manifest.json`);
- the PostHog retention or IP settings.
