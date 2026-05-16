# investhelper-legal

Public-facing legal documents for the [InvestHelper](https://github.com/imbilalhassan/InvestHelper) mobile app, hosted via GitHub Pages.

Live URL: <https://imbilalhassan.github.io/investhelper-legal/>

## Files

- `privacy-policy.html` — privacy policy linked from the app's Settings screen and registered with App Store Connect / Google Play Console
- `index.html` — landing page that links to the policy

## Updating

1. Edit `privacy-policy.html` (bump the "Effective date" at the top).
2. Commit and push to `main`.
3. GitHub Pages redeploys automatically — usually within ~1 minute.
4. The URL stays the same, so no app or store-listing changes are needed.

## Why this lives in a separate repo

The main app repo stays clean of public web assets. The Supabase domain (`*.supabase.co`) actively strips the `Content-Type: text/html` header from any HTML response (anti-XSS measure), so Storage and Edge Functions can't be used to host this file. GitHub Pages is free, public, and serves HTML correctly out of the box.
