# domain-age-alert — Is This Legit? TEST BUILD

**Test-only** hosting for the Is This Legit? Outlook add-in. Client tenants do **not** load from here. Production is [`IsThisLegit-For-Clients`](https://github.com/JeffMattNJ/IsThisLegit-For-Clients).

**Test URL:** https://JeffMattNJ.github.io/domain-age-alert/taskpane.html (footer shows **TEST BUILD**)

## Test add-in

| Item | Value |
|---|---|
| Manifest | `manifest-TEST-1.0.0.1.xml` |
| Display name | Is This Legit? TEST (ribbon group "Security TEST") |
| GUID | `b3f23b7f-81d1-4904-b942-30d0c63778a1` (never use for clients) |
| Next version | 1.0.0.2 |
| Assigned to | Test users only (e.g. `apptest`), never All users |

## Workflow

1. Change `taskpane.html` here, then merge.
2. Test as `apptest` in Outlook on the web, new Outlook and classic Outlook. Use real flagged emails.
3. When it passes, copy the identical `taskpane.html` to `IsThisLegit-For-Clients`.

## Old files

Older manifests in this repo (`manifest-current.xml`, `manifest_7282026_working.xml`, etc.) are history only. Don't upload them anywhere.
