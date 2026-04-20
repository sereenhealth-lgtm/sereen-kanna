# Sereen Wholesale — Drop-in Package

Everything is done. You just need to put these files in your GitHub Desktop folder and push.

## Steps (3 minutes total)

**1.** In Finder, open your synced wholesale repo folder (e.g. `~/Documents/sereen-wholesale`).

**2.** Select ALL 10 files in this package and drag them into the repo folder. When macOS asks if you want to replace `index.html` — **Yes, replace**. (The new one already has the favicon and OG tags built in, plus it keeps your existing Google Analytics and Google Fonts untouched.)

**3.** Open GitHub Desktop. You'll see:
   - Modified: `index.html`
   - Added: 9 new asset files

Type a commit message like `Add favicon and social share image`, click **Commit to main**, then **Push origin**.

Netlify auto-deploys in 30–60 seconds.

## Verify it worked

- **Favicon**: open `https://wholesale.sereenkanna.com/` in an **incognito window** (browsers cache old favicons). Gold "S" should appear in the tab.
- **Social share preview**: paste your URL into the [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) and click **Scrape Again**. The gold wordmark image should render. Do the same at [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/).

If a preview looks blank or old, it's always a platform cache issue — the debugger tools above force a refresh.

## Sanity checks

Quick URLs to confirm files deployed correctly:
- `https://wholesale.sereenkanna.com/favicon.svg` → should display the "S" icon
- `https://wholesale.sereenkanna.com/og-image.jpg` → should display the share image

If either returns a 404, the file didn't push. Check your GitHub Desktop commit.

---

## What changed in index.html

- New `<title>` and `<meta description>` block (same copy as before, just reorganised)
- Added `<link rel="canonical">` and `<meta theme-color>`
- Added 6 favicon links (SVG, ICO, multiple PNG sizes, Apple touch icon, webmanifest)
- Added 11 Open Graph tags (for Facebook/LinkedIn/WhatsApp/Slack/iMessage)
- Added 5 Twitter Card tags
- Removed the old duplicate `<meta description>` that was lower down
- **Kept**: Google Analytics (`G-7TNMMZ4L57`), Google Fonts preconnect + stylesheet, and every other line of your site exactly as it was

Nothing was touched below the `<head>`. All 1700+ lines of your CSS, HTML, and content are identical to before.
