# Security

## What a deployed NGSF app can access

NGSF is deployed as a web app that runs **as the deployer** ("Execute as: Me"). Every request uses the deployer's Google permissions:

| Permission | Why NGSF needs it |
|---|---|
| Google Sheets | Reading config and reading/writing app data |
| Google Drive | File uploads, PDF printing, XLSX import, PatchSync |
| Gmail (send) | Login codes and email notifications |
| External requests | Optional integrations |

**Recommendation:** deploy from a Google account that holds only that app's files, not a personal account with your whole Drive in it.

## Who can use the app

Opening the web app URL is not the same as having access. Users sign in with a one-time code sent to their email, and only emails listed in the `Users` sheet (or matched by `Config_UserSources`) see pages, filtered by role. Login codes are single-use and expire.


## Reporting a vulnerability

Please **do not** open a public GitHub issue. Email **nashir.ardiansyah@gmail.com** with steps to reproduce. You'll get a reply within 7 days, and a fix will be released before the issue is made public.

## Supported versions

Only the latest release receives security fixes.
