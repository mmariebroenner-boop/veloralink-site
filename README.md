# Velora Link — Website

Public site for **Velora Link**, the B2B trade platform for premium Thai cannabis flower export to licensed buyers in Australia, Canada, Germany and Portugal.

Live domain: **veloralink.com** (hosted on Netlify, DNS on Namecheap).

---

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The public landing page. Hero, stats, about, farm network, how it works, compliance, contact. |
| `register.html` | The "Register as a Buyer" page — gated form for collecting buyer details + documents. Reveals DBD + PT.10 documents only after a buyer submits. |
| `request-access.html` | Duplicate of `register.html` (kept so older links don't break). Safe to delete if nothing points to it. |
| `farm-indoor-eu.jpg.jpeg` | Indoor cultivation photo (currently unused — both Indoor cards point at `farm-indoor-thai.jpg.JPG`). |
| `farm-indoor-thai.jpg.JPG` | Indoor cultivation photo used for both Indoor EU GACP + Indoor Thai GACP cards. |
| `farm-greenhouse-thai.jpg.JPEG` | Greenhouse Thai GACP card photo. |
| `sample-cbd.jpg.png` | (Currently unused on the landing — kept for future product cards.) |
| `sample-thc.jpg.png` | (Currently unused on the landing — kept for future product cards.) |
| `dbd-page1.jpg .jpg` | First page of the DBD company registration certificate. |
| `export-license-pt10.jpg.jpg` | Controlled Herb Export Licence (PT.10) image. |

---

## How to update common things

### Swap a photo

Save the new image into this folder. Then in `index.html`, find the matching `<img src="…">` line and change the filename. Examples:

- Indoor farm cards → look for `farm-indoor-` in `index.html`
- Greenhouse card → look for `farm-greenhouse-thai`
- Documents (on `register.html`) → look for `dbd-page1` and `export-license-pt10`

The image dimensions don't have to match — CSS handles cropping/scaling.

### Change the email or WhatsApp number

In `index.html`, search for `admin@veloralink.com` or `66895555554` and replace. The WhatsApp button uses `wa.me/<number>` format — no `+` or spaces in the URL, but the displayed text (`+66 89 555 5554`) should keep them.

### Update copy (any text on the site)

Open the file in any text editor, search for the words you want to change, edit, save. Then drag the file back into Netlify (or push to GitHub if connected) to publish.

### Change the registration form fields

In `register.html`, find the `<form class="access-form">` block. Each field has a `<label>` and an `<input>` or `<select>`. Add, remove or rename fields by editing the HTML. Field `name="…"` attributes become the column headers in the Netlify submissions dashboard, so keep them descriptive.

---

## How registrations work

The form on `register.html` is wired to **Netlify Forms**. When a buyer submits:

1. The data and any uploaded files (import licence, business registration, other docs) post to Netlify.
2. The buyer sees a "Thank you" message and the gated DBD + PT.10 documents reveal underneath.
3. The submission appears in the **Netlify dashboard → Forms → "buyer-registration"** — full data + downloadable files.
4. If email notifications are enabled (Site Settings → Forms → Form notifications), a copy emails `admin@veloralink.com`.

To export all submissions as a CSV (for building a buyer directory), use the Export button in the same Forms dashboard.

---

## Deployment

- **Host**: Netlify (free tier).
- **Domain**: `veloralink.com` registered on Namecheap, pointed at Netlify via A + CNAME records. The Google Workspace MX records on Namecheap remain untouched — email keeps working.
- **SSL**: auto-provisioned by Netlify via Let's Encrypt.
- **Repo (optional)**: if connected to a GitHub repo, pushes to `main` auto-deploy.

---

## Key facts (for reference)

- **Brand**: Velora · **Platform**: Velora Link
- **Export licence**: Controlled Herb Export Licence (PT.10), No. **PT10-1773810063**, valid **7 May 2026 → 31 Dec 2028**, held via Remedies Enterprise Co., Ltd.
- **Monthly capacity**: 3 tons (partner farm network).
- **Cultivation profiles offered**: Indoor (Thai or EU GACP), Greenhouse (Thai GACP).
- **Trade desk email**: admin@veloralink.com (Google Workspace).
- **Trade desk WhatsApp**: +66 89 555 5554.
- **Export destinations**: Australia (TGA/ODC), Canada, Germany, Portugal.
- **Testing labs referenced**: TNR Bioscience Co., Ltd. (Thailand), Eurofins (international).
- **Compliance rule**: Never claim certifications not currently held. Describe GACP as "aligned" until certificates are in hand. Documents shown as "On File" only when truly held.

---

## Compliance disclaimer

For licensed B2B partners only. This website does not constitute an offer for sale in jurisdictions where cannabis is not legally permitted for import. Velora Link handles the Thai-side export only — import permits, customs clearance and receiving in the destination country are the buyer's responsibility.
# veloralink-site
