# AP Assistant Professor (Pharmacy) brochure

Interactive one-page brochure for the Pharmakaksha batch for the APPSC Assistant Professor (Pharmacy) screening test (CBT, 3 December 2026, 09:30–12:30).

It has a countdown to the exam, an index bar, the selection steps, a +3 / −1 score calculator, a guessing guide, posts by university, what the batch includes, the subjects, a day-by-day study plan, fees with offers, contact details and social links. It is a single static `index.html`, so no build step is needed.

## Editing the details

Open `index.html` and find `const CONFIG` near the bottom. It holds the fee and offers, the registration close date, batch start, contact links (WhatsApp channel, WhatsApp chat, email), the share message and the Cloudflare analytics token. The day-by-day study plan is the `PLAN` list a little further down.

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
3. In the repository, go to **Settings → Pages** and set **Source = GitHub Actions**. The workflow in `.github/workflows/deploy.yml` publishes on every push to `main`.
4. The page is live in a minute or two at `https://ajreddys.github.io/ap-asst-prof-pharmacy/`.

### Custom domain: apur26.pharmakaksha.com

The `CNAME` file in this folder already contains `apur26.pharmakaksha.com`.
1. At your domain provider, add a DNS record: Type `CNAME`, Host `apur26`, Value `ajreddys.github.io`.
2. In the repository, go to **Settings → Pages**, enter `apur26.pharmakaksha.com` as the **Custom domain** and save.
3. Once the DNS check passes, tick **Enforce HTTPS**.

### Link preview image

`og-image.jpg` (1200×630) is the preview card WhatsApp and Telegram show when the link is shared. The `og:image` tag in `<head>` points to it by full URL.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The brochure page (styles and script included) |
| `logo.jpg` | Pharmakaksha logo, used as the favicon |
| `CNAME` | The custom domain `apur26.pharmakaksha.com` |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |
| `og-image.jpg` | Link preview card |

Exam facts come from the APPSC web note dated 05.10.2026 and the AP state universities' recruitment notifications. Pharmacy posts: AU 10, Krishna 6, ANU 4, Adikavi Nannaya 4, SVU 4, SKU 1 (29). Recheck them if APPSC updates the schedule.
