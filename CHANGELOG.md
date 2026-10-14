# Changelog

All notable changes to NGSF are listed here. Versions follow [Semantic Versioning](https://semver.org): MAJOR for changes that need config migration, MINOR for new features, PATCH for fixes.

## [1.0.0] - 2026-10-xx

First public release, based on internal version 2.11.0.

### Included
- Config-driven pages, sections and fields
- Section types: table, matrix, dashboard, gantt, warehouse, content
- OTP email login and role-based access
- Rules, cascades, derived columns, and `{{count:…}}` / `{{list:…}}` / `{{sum:…}}` / `{{avg:…}}` tokens
- Version history, soft delete and restore
- PDF printing from Google Doc templates
- Email notifications
- CSV and XLSX import (XLSX needs the Drive API advanced service)
- In-app builder
- PatchSync (optional)

### Notes
- Replace all code files together when updating.
- `Algorithm.gs` (vehicle routing) is optional and can be deleted.
