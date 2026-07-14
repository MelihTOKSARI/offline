# Offline — public web pages (GitHub Pages)

The four public pages the App Store / Google Play listing needs, hosted free on GitHub Pages. Same setup as your `nobuy` repo.

## What's here

```
site/
├── index.html          → https://melihtoksari.github.io/offline/          (Marketing URL)
├── privacy/index.html  → https://melihtoksari.github.io/offline/privacy   (Privacy Policy URL)
├── terms/index.html    → https://melihtoksari.github.io/offline/terms     (Terms of Use)
├── support/index.html  → https://melihtoksari.github.io/offline/support   (Support URL)
├── j/index.html        → https://melihtoksari.github.io/offline/j/?c=CODE (friend-invite landing, deep-links to offline://invite/CODE)
└── .nojekyll           (serve files as-is)
```

Self-contained HTML, light + dark aware, Offline brand (Morning meadow / Campfire at dusk). Folder-per-page gives clean `/privacy` URLs.

## Deploy in ~5 minutes

1. Create a new **public** repo named exactly **`offline`** under `MelihTOKSARI` (Pages URLs are lowercase: `melihtoksari.github.io/offline/`).
2. Upload the **contents of this `site/` folder** to the repo root (root must directly contain `index.html`, `privacy/`, `terms/`, `support/`, `.nojekyll`).
3. Repo → Settings → Pages → Source = Deploy from a branch · Branch = `main` · folder = `/ (root)` → Save.
4. Wait 1–2 min, then open all four URLs.
5. Paste them into App Store Connect + Play Console (they're already referenced in `store/listing-aso.md`).

## Before you submit — checklist

- [ ] All four URLs load publicly (App Review fetches them).
- [ ] Governing law in Terms = US / Delaware — change if you prefer.
- [ ] Contact email `smtoksari@gmail.com` correct everywhere.
- [ ] **App Store privacy label** — unlike NoBuy, Offline is NOT "Data Not Collected." Declare (all *linked to you* via account, **no tracking**, no ads):
  - Identifiers → User ID
  - User Content → Photos, Other User Content (journey stories)
  - Health & Fitness → n/a (don't declare; activity logs aren't health data)
  - Usage Data → Product Interaction (analytics)
  - Purchases → Purchase History (via RevenueCat)
  - Contact Info → Name/Email only if Apple/Google sign-in used
- [ ] **Play Data safety** — mirror the same: data collected (user IDs, in-app actions, photos user-provided), encrypted in transit, deletable via in-app account deletion; no data sold/shared for ads.
- [ ] Screen Time / usage data: on-device only — do NOT declare as collected (matches Privacy Policy §3).

## Updating later

Edit HTML, commit — Pages redeploys in minutes. Bump "Last updated" on Privacy/Terms for material changes.
