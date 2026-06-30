# Jason Aguirre Group — A2P-ready real estate website

A complete static website (HTML/CSS/JS, no build step) designed to satisfy
**A2P 10DLC** brand/campaign review on GoHighLevel while functioning as a real,
credible business site. Host it free on GitHub Pages.

## Files

| File | Purpose | Submit to A2P? |
|------|---------|----------------|
| `index.html` | Main site + compliant opt-in form | ✅ Yes — this is your **opt-in / consent URL** |
| `privacy.html` | Privacy Policy with SMS non-sharing clause | ✅ Yes — **Privacy Policy URL** |
| `terms.html` | Messaging Terms (SMS program disclosures) | ✅ Yes — **Terms URL** |
| `styles.css` | Shared design system | — |

---

## ⚠️ Edit before you submit (search each file for `EDIT:`)

1. **Business name** — On the site it reads *Jason Aguirre Group*. This **must
   exactly match the legal entity name on the EIN** you used to register your
   A2P brand. If your EIN is under a different LLC, either change the name
   everywhere or register *Jason Aguirre Group* as your **DBA** in the brand
   registration. Name mismatch is a top rejection reason.
2. **Email** — Replace `hello@jasonaguirregroup.com` with your real address
   (appears in `index.html`, `privacy.html`, `terms.html`).
3. **Effective dates** — Set the dates in `privacy.html` and `terms.html`.
4. **Form capture (optional)** — The form is client-side (shows a thank-you).
   To capture real leads, point it at your GoHighLevel embedded form or a form
   endpoint. **Leave the consent UI exactly as built.**

---

## Deploy on GitHub Pages

1. Create a new public repo (e.g. `jag-site`).
2. Upload all four files to the repo root (keep them in the **same folder** so
   the relative links work).
3. Repo **Settings → Pages → Build and deployment** → Source: *Deploy from a
   branch* → Branch: `main` / `/root` → **Save**.
4. Your site goes live at `https://<username>.github.io/jag-site/` in ~1 min.
5. (Optional) Add a custom domain under the same Pages settings.

Your three submission URLs will be:
```
https://<username>.github.io/jag-site/            ← opt-in form
https://<username>.github.io/jag-site/privacy.html
https://<username>.github.io/jag-site/terms.html
```

---

## What makes this A2P-compliant

- **Real, substantial site** — full nav, about, services, process, areas, and
  contact, so it doesn't read as a thin "compliance front."
- **Privacy Policy** explicitly states mobile/SMS opt-in and consent data are
  **not sold or shared with third parties** (the most common missing piece).
- **Messaging Terms** include program name, message types, *message frequency
  varies*, *message and data rates may apply* (verbatim), and bold **STOP** /
  **HELP** instructions plus carrier-liability language.
- **Opt-in form:**
  - Phone is **optional**; the consent box is **optional** and **unchecked** by
    default — neither gates form submission (consent is never coerced).
  - The checkbox label is the **CTA disclosure only** (brand, purpose,
    frequency, rates, STOP/HELP) — it contains **no** third-party language.
  - **Privacy Policy + Messaging Terms links sit below the form**, not inside
    the checkbox.
- **Footer on every page** links to the Privacy Policy and Messaging Terms.

## Before you resubmit a rejected campaign
TCR often flags only the first problem it finds, so fix the **whole** submission
— make sure the opt-in method you describe in the campaign matches what's shown
on `index.html`, and that your sample messages include your business name and an
opt-out line.

> These pages are a strong, compliant starting point, not legal advice. Have
> your own counsel review them for your business and jurisdiction.

---

## Deploy on Vercel

This is a plain static site — no build step. Three ways, fastest first:

**1. Drag & drop (Vercel Drop) — instant, no Git**
Unzip `jag-site.zip`, go to **vercel.com/new**, and drag the unzipped **jag-site** folder onto the drop area. Vercel serves it as-is and gives you a live URL in seconds.

**2. GitHub → Vercel (recommended — auto-deploys on every edit)**
Push these files to a GitHub repo, then in Vercel: **Add New → Project → Import** the repo. For a static site, leave Framework Preset as **Other**, leave Build Command blank, and set **Output Directory** to `.` (a single period). Click **Deploy**. Every future `git push` redeploys automatically — ideal while you swap in real photos and listings.

**3. Vercel CLI — one terminal command**
```bash
npm i -g vercel
cd jag-site
vercel            # logs in via your browser, creates a preview
vercel --prod     # promotes to production
```

The included `vercel.json` turns on **clean URLs**, so your pages live at `/privacy` and `/terms` (no `.html`). Add a custom domain anytime under **Project → Settings → Domains** — HTTPS is automatic and free on the Hobby plan.
