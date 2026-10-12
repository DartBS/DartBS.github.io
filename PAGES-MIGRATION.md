# Nahan Installer: Cloudflare Pages migration

This fork changes the installer deployment target from Workers Scripts to Cloudflare Pages Direct Upload.

## Changes
- Creates/updates a Pages project rather than a Workers script.
- Uploads Nahan's `_worker.js` as the Pages advanced-mode runtime.
- Configures the `IOT_DB` D1 binding on production and preview environments.
- Uses the `https://<project>.pages.dev` URL instead of `workers.dev`.
- Extends the optional installer proxy's allowlist for Pages project and deployment endpoints.

## Requirements
- Cloudflare API token with Pages Edit and D1 Edit permissions.
- The account's D1 API access enabled.
- A Pages project name containing lowercase letters, digits, and hyphens.

The Cloudflare API may reject deployment if the account or token lacks the required Pages permissions. Check the exact API error shown by the installer.
