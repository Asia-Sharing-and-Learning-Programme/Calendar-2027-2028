# ASLP Calendar 2027–2028

Shared planning calendar for the Asia-Pacific Sharing & Learning Programme (ASLP): ASC, APSG, CWG, SOG and FCG meetings, ASLF, P2P visits, Capacity Development, reports and deadlines for 2027–2028.

## What's here
- `index.html` – the whole website (year-at-a-glance calendar, filters, entry form, repeats, linked types, dark mode)
- `vendor/supabase.js` – bundled Supabase client
- `aslp-logo-light.png`, `aslp-logo-dark.png`, `favicon.png` – branding

## How it works
- **Hosting:** GitHub Pages (this repository, `main` branch, root folder).
- **Data:** Supabase project "ASLP CDS Dashboard" (shared with the CD Strategy dashboard), table `calendar_events`. The website only calls database functions (`cal_get`, `cal_whoami`, `cal_check_email`, `cal_save`); the table is not directly readable or writable.
- **Private:** the page code is public, but the calendar entries are not. Only people on the ASLP admin list (programme coordinators, CWG leads and other admins, managed in the CD Strategy dashboard) can see them, after signing in with an emailed link. They can then add, edit and delete entries.
- No calendar data is stored in this repository.
- The database is kept awake by the keep-awake workflow in the `cd-strategy` repository.

The Supabase key in `index.html` is the *publishable* key, which is meant to be public.

Maintained with Claude.
