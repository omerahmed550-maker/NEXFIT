# Security Policy

## Reporting a vulnerability
Please do not open a public issue for security problems.
Use GitHub's private reporting: the **Security** tab, then **Report a vulnerability**.
You will get a reply as soon as possible.

## Scope and design notes
- NEX FIT is a static web app. There is no backend, no accounts and no server-side storage.
- User data stays on the device (IndexedDB). Hosting only serves the app files.
- Imported text and Google Sheet content is escaped before it is displayed.
- The Google Sheet import only reads public CSV links and sends no credentials.
- Never commit API keys, tokens, passwords or exported backups (`nexfit-backup-*.json`) to this repository.
