# AP Assistant Professor (Pharmacy) brochure

Interactive one-page brochure for the Pharmakaksha batch for the APPSC Assistant Professor (Pharmacy) screening test (CBT, 3 December 2026, 09:30–12:30).

It has a countdown to the exam, a +3 / −1 score calculator with category cut-offs, a guessing guide, the selection steps, the subjects covered and a WhatsApp enrol button. It is a single static `index.html`, so no build step is needed.

## Before sharing: fill in the batch details

Open `index.html`, find `const CONFIG` near the bottom and fill in the values. Anything left as `""` shows as **TBA** on the page.

```js
const CONFIG = {
  fee: "₹4,999",
  offer: "Early-bird ₹3,999 till 31 Oct",
  batchStart: "20 Oct 2026",
  timings: "Mon–Sat, 7–9 PM",
  whatsapp: "https://www.whatsapp.com/channel/0029VbDs5dyIN9ipjEeNYg3x",
  exam: "2026-12-03T09:30:00+05:30"
};
```

## Publish on GitHub Pages

1. On GitHub, create a **public** repository, for example `ajreddys/ap-asst-prof-pharmacy`.
2. From this folder:
   ```bash
   git init -b main
   git add .
   git commit -m "AP Assistant Professor Pharmacy brochure"
   git remote add origin https://github.com/ajreddys/ap-asst-prof-pharmacy.git
   git push -u origin main
   ```
3. In the repository, go to **Settings → Pages**, set **Source = Deploy from a branch**, branch `main`, folder `/ (root)`.
4. The page is live in a minute or two at `https://ajreddys.github.io/ap-asst-prof-pharmacy/`.

### Custom domain: apur26.pharmakaksha.com

The `CNAME` file in this folder already contains `apur26.pharmakaksha.com`.
1. At your domain provider, add a DNS record: Type `CNAME`, Host `apur26`, Value `ajreddys.github.io`.
2. In the repository, go to **Settings → Pages**, enter `apur26.pharmakaksha.com` as the **Custom domain** and save.
3. Once the DNS check passes, tick **Enforce HTTPS**.

### Optional: link preview image

WhatsApp and Telegram show a preview card when the link is shared. To add an image, put a 1200×630 `og-image.jpg` in this folder and add this line inside `<head>` (it needs the full URL):

```html
<meta property="og:image" content="https://apur26.pharmakaksha.com/og-image.jpg">
```

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The brochure page (styles and script included) |
| `logo.jpg` | Pharmakaksha logo, used as the favicon |
| `CNAME` | The custom domain `apur26.pharmakaksha.com` |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

Exam facts come from the APPSC web note dated 05.10.2026 and the AU, SVU and SPMVV recruitment notifications. Recheck them if APPSC updates the schedule.
