# Order Book

A free, offline web app for a tailor: clients and measurements, orders and stages, payments, fabric stock, earnings, WhatsApp messages, receipts and job cards, and scanning handwritten record pages with Google Gemini.

## How it works

- **No server, no accounts.** Everything is stored on the phone in the browser's storage (IndexedDB). Nothing in this repository contains client data.
- **Works offline** once opened. Scanning needs internet.
- **Install** from Chrome: menu → *Add to Home screen* (or *Install app* in Settings).
- **Backups:** Settings → *Save backup* creates one `.json` file with all records and photos. Keep it in Google Drive or send it to yourself on WhatsApp. *Restore from backup* merges it back in, keeping whichever copy of each record is newer.
- **Scanning** uses Google's Gemini API free tier. Get a key at <https://aistudio.google.com/apikey> and paste it in Settings. The key is stored only on the phone and is never included in backups. The model defaults to `gemini-flash-latest` and can be changed in Settings.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app |
| `sw.js` | Offline cache. Bump `VERSION` after changing files |
| `manifest.webmanifest`, `icon*` | Install name and icons |

## Hosting

Served by GitHub Pages from the `main` branch root. Any static host works.
