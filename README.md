# ASLP Calendar 2027–2028

Shared planning calendar for the Asia-Pacific Sharing & Learning Programme (ASLP): ASC, APSG, CWG, SOG and FCG meetings, ASLF, P2P visits, Capacity Development, reports and deadlines for 2027–2028.

## What's here
- `index.html` – the whole website (year-at-a-glance calendar, filters, entry form, repeats, linked types, dark mode)
- `vendor/supabase.js` – bundled Supabase client
- `aslp-logo-light.png`, `aslp-logo-dark.png`, `favicon.png` – branding

## How it works
- **Hosting:** GitHub Pages (this repository, `main` branch, root folder).
- **Data:** Supabase project "ASLP CDS Dashboard" (shared with the CD Strategy dashboard). The website only calls database functions; the tables are not directly readable or writable. No calendar data is stored in this repository.
- **Public summary (no sign-in):** year tabs (2027, 2028, both) showing which types of activity happen on which days — no titles, notes or places. Hidden types (e.g. ASLP Phase 2, Significant Change Process) are left out.
- **Group leads (sign in by emailed link):** full details for entries of their group (an entry counts if its main type or a linked type belongs to the group), a summary of everything else. Only groups allowed in the admin settings see hidden types. CWG leads from the CD Strategy dashboard are recognised automatically.
- **Admins:** see everything, add/edit/delete entries, and use **⚙ Admin** to manage access (admins and group leads), group-lead settings, types (name, colour, filter row, hidden), territories and countries, and the activity log. CD Strategy dashboard coordinators and admins are calendar admins automatically.
- Database: tables `calendar_events`, `cal_users`, `cal_settings`, `cal_log`; functions `cal_public`, `cal_get`, `cal_whoami`, `cal_check_email`, `cal_save`, `cal_admin_get`, `cal_admin_set_users`, `cal_admin_set_setting`.

The Supabase key in `index.html` is the *publishable* key, which is meant to be public.

Maintained with Claude.
