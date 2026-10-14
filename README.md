# NGSF

**A config-driven app framework for Google Sheets.**

**[➜ Make a copy of NGSF v1.0.0](https://docs.google.com/spreadsheets/d/TEMPLATE_ID/copy)** · [Install guide](#install-about-15-minutes) · [Releases](../../releases) · [License](#license)

NGSF turns a Google Sheet into a working web app. Pages, sections and fields are rows in config sheets, so most features are built by editing config, not code. It runs entirely on Google Apps Script: no server, no hosting bill.

> Screenshot: add `docs/screenshot.png` here.

## What you get

- Pages, sections and fields defined in `Config_Pages`, `Config_Sections` and `Config_Fields`
- Section types: table, matrix, dashboard, gantt, warehouse, content
- Field types: text, number, date, select, upload, lookup, formula, auto ID and more
- Role-based access with one-time-code (OTP) email login, no passwords
- Rules, cascades and derived columns for workflow logic
- Version history and soft delete on every record
- PDF printing from Google Doc templates, email notifications, CSV/XLSX import
- A builder inside the app for creating pages without touching the sheet

## Install (about 15 minutes)

1. Open the template link and click **Make a copy**. You need a Google account; the copy goes into your own Drive with the script included.
   **https://drive.google.com/drive/folders/1vrAiPqMKFr-djEP9MM7bp9Yz-9op_Rrd?usp=sharing**

   Already running NGSF? Don't make a new copy, or you'll start with empty data. See [Updating](#updating) instead.
2. In your copy, open **Extensions → Apps Script**.
3. Click **Deploy → New deployment → Web app**. Set *Execute as* to **Me**, choose who has access, and click **Deploy**.
4. Authorize the script when Google asks. You'll see an "unverified app" warning; this is normal for a personal Apps Script project.
5. Open the Web app URL (ends in `/exec`). The spreadsheet owner is Admin automatically.

Full guide: [docs/quick-start.md](docs/quick-start.md)

## Updating

Each release is published on the [Releases](../../releases) page with all code files and, when needed, a migration patch. Replace **all** code files from the same release; mixing versions can break features silently. Then create a new deployment version and clear the app cache from the App Admin menu.

## Limits

NGSF runs on Apps Script, so expect roughly 1–2 s for the first load and 0.5–1 s per page change. Apps Script quotas apply. Files in a Shared Drive have no owner, so the automatic owner-as-Admin rule does not apply there.

## License

NGSF is **source-available** under the [PolyForm Noncommercial License 1.0.0](LICENSE).

- **Free** for personal use, study and research, and for use by educational institutions, public research organizations, charities, and government bodies.
- **Commercial use requires a license.** That includes using NGSF to run a business's operations, building apps on it for paying clients, and selling or reselling NGSF or apps built on it. See [COMMERCIAL.md](COMMERCIAL.md).

NGSF is not affiliated with or endorsed by Google. Google Sheets and Google Apps Script are trademarks of Google LLC.

## Security

See [SECURITY.md](SECURITY.md) for what a deployed app can access and how to report a vulnerability.

## Contributing

Bug reports and suggestions are welcome as GitHub issues. Pull requests can only be accepted with a signed Contributor License Agreement, because NGSF is also offered under commercial licenses.
