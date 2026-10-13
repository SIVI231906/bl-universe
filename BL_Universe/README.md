# BL Universe — free starter website

## What is included
- Responsive mobile/desktop design
- Home, Series, BL Shorts, Watchlist, Community, Account and Admin pages
- Search and filters by country, genre, status and official-free availability
- Demo BL catalogue entries (sample metadata only; viewing URLs intentionally blank)
- Watchlist stored in the browser
- Reviews stored in the browser
- Demo profile stored in the browser (NOT secure authentication)
- Add/remove catalogue entries in the local admin prototype
- Official YouTube embeds when a valid YouTube URL is entered
- Direct MP4/WebM/OGG playback when a valid authorized direct video URL is entered
- External links for official sources

## Open locally
1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. Browse the catalogue. Use Admin Studio to add verified official or licensed viewing URLs.
4. Changes are stored in the same browser using localStorage.

## Publish for free (static prototype)
Option A — GitHub Pages:
1. Create a GitHub account and a new public repository.
2. Upload `index.html` (or all files in this folder).
3. In repository Settings → Pages, choose deploy from branch and select `main` / root.
4. Wait for GitHub Pages to publish the site. The URL will be shown in Pages settings.

Option B — Netlify Drop:
1. Open https://app.netlify.com/drop
2. Drag the extracted folder into the upload area.
3. Use the generated free subdomain.

## Important limitations
This is a functional front-end prototype, not a production streaming service:
- User profile, watchlist, reviews and catalogue changes are browser-local. They do not sync between visitors/devices.
- Demo profile is not authentication. The Admin page is not secured and must not be exposed as a real admin tool.
- No video files are uploaded to a server. Videos must be hosted by an authorized provider; YouTube URLs can be embedded where the rights holder allows it.
- Sample titles are catalogue examples. No video links are provided by default; verify legal availability in your region.
- Do not upload, mirror, scrape, or redistribute copyrighted episodes/posters without permission.
- Add privacy policy, terms, community rules, copyright/takedown contact and age-appropriate safeguards before public launch.

## Roadmap to a real multi-user website (free tiers where possible)
### Phase 1 — Prototype (done)
- Responsive front-end and local browser interactions.

### Phase 2 — Publish the static site (1 day)
- Publish with GitHub Pages or Netlify.
- Choose the brand name, logo and colour palette.
- Add real official watch links and rights-cleared promotional artwork.

### Phase 3 — Real database and authentication (1–3 days)
- Create a Supabase project on its free plan (subject to quotas).
- Create `profiles`, `titles`, `episodes`, `watchlist`, `reviews` tables.
- Use Supabase Auth with email verification.
- Add Row Level Security: users can edit only their own profile/reviews/watchlist; only admin roles can manage titles.
- Move catalogue reads/writes from localStorage to the database.
- Never put service-role keys in browser code.

### Phase 4 — Authorized media (2–5 days plus provider approval)
- Start with official YouTube embeds and outbound official links.
- For content you own/license, choose a host that permits your use and embeds/direct playback; check storage, bandwidth, territory and monetization terms.
- Keep a rights record for each title/episode: owner, license scope, territories, expiration date and source.
- Do not proxy, download, or re-upload third-party streams.

### Phase 5 — Community and safety (2–4 days)
- Server-side moderation, report button, block/mute tools and anti-spam limits.
- Validate review lengths and URLs server-side.
- Add privacy policy, terms, copyright takedown process and contact details.
- Set clear content ratings and restrict access where legally required.

### Phase 6 — Launch checks (1–2 days)
- Test Android/iPhone and desktop.
- Test keyboard accessibility, broken links, empty states and slow connections.
- Set backups, error monitoring and a simple admin audit log.
- Track free-tier usage and set spending alerts; free tiers are not unlimited.

## Suggested free-first stack for production
- Frontend: this HTML prototype, later React/Vite if needed.
- Hosting: GitHub Pages or Netlify free tier for static files.
- Authentication/database: Supabase free tier (quotas and terms can change).
- Media: official YouTube embeds first; licensed media hosting only after reviewing provider terms.
- Custom domain: optional and normally paid.
