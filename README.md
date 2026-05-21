# Domain Age Alert — Outlook Add-in

An Outlook add-in that checks how old a sender's domain is and warns you when it was registered recently — one of the top indicators of phishing and business email compromise scams.

## Risk Levels

| Domain Age | Risk Level |
|---|---|
| 0–7 days | 🚨 Critical |
| 8–30 days | ⛔ High Risk |
| 31–90 days | ⚠️ Elevated |
| 1+ year | ✅ Safe |

## Setup — 3 steps after importing this repo

### Step 1 — Enable GitHub Pages
1. Go to **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** / folder: **/ (root)**
4. Click **Save**
5. Wait 60 seconds — your URL will be: `https://YOUR-USERNAME.github.io/domain-age-alert`

### Step 2 — Update manifest.xml
1. In this repo, click **manifest.xml**
2. Click the **pencil (edit) icon**
3. Press **Ctrl+H** — Find: `GITHUB_PAGES_URL` → Replace with your actual URL
   Example: `https://jcruz99.github.io/domain-age-alert`
4. Click **Commit changes**

### Step 3 — Install in Outlook
1. Go to **https://outlook.office.com**
2. Open any email → click **...** → **Get Add-ins**
3. Click **My Add-ins** → scroll to **Custom Add-ins**
4. Click **+ Add a custom add-in** → **Add from URL...**
5. Paste: `https://YOUR-USERNAME.github.io/domain-age-alert/manifest.xml`
6. Click Install → restart Outlook desktop

## Files

| File | Purpose |
|---|---|
| `taskpane.html` | Main add-in UI panel |
| `commands.html` | Background event handler |
| `manifest.xml` | Outlook add-in manifest |
| `icon-16/32/80.png` | Toolbar icons |

## Security & Privacy
- Only the sender's **domain name** is ever sent externally (to public RDAP registries)
- No email content, subject, or personal data is transmitted
- Uses public RDAP infrastructure — no API keys required
- Read-only `ReadItem` permission — cannot send email or access other items
