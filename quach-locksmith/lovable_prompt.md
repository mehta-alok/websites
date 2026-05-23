# Lovable Prompt — Quach's Locksmith (Oakland)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **Quach's Locksmith**. Real data, real Yelp reviews, real address — already filled in.
>
> **How to use.**
> 1. Open https://lovable.dev/ and start a new project.
> 2. Copy everything below (both STEP 1 and STEP 2) and paste it into the chat.
> 3. When Lovable asks to connect Supabase, say yes.
> 4. Add a Resend API key (free 3K emails/mo) when prompted — that powers booking/quote notifications.
> 5. In Supabase Auth, add one user with **the Quach family**'s email + a password. That's their admin login.
> 6. Publish → get the live URL → send it to the owner.

---

## STEP 1 — Business details (copy this block as-is)

```
BUSINESS NAME:   Quach's Locksmith
BUSINESS TYPE:   locksmith
LOCATION:        Oakland, CA
FULL ADDRESS:    106 International Blvd, Oakland, CA 94606
PHONE:           (510) 839-8888
RATING / VOLUME: 4.5★ from 65 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/quach-locksmith-oakland-4
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Mon – Fri: 10:30 AM – 6:00 PM
  - Saturday: 11:00 AM – 4:00 PM
  - Sunday: By appointment
TODAY'S HOURS:   10:30 AM – 6:00 PM

MENU / SERVICES (display each as a card with price + description):
  - Re-Key Locks — $50/lock — Same lock, new key — landlord and tenant favorite.
  - Lockout Service — From $75 — House, car, business — fast 30-min response.
  - New Lock Install — From $120 — Deadbolts, smart locks, high-security cylinders.
  - Auto Key Programming — From $80 — Transponder, smart key, fob — 99% of vehicles.
  - Master Key System — From $250 — One key for multiple doors. Commercial spec.
  - Safe Combination Reset — From $95 — Floor safes, gun safes, office safes.

BRAND FEEL:      secure, premium, no-nonsense — dark charcoal + gold accents

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "This is the best locksmith in Oakland. They copied hard-to-cut and old keys that most places could not." — Verified Customer
  - "Quach herself was there to help — really friendly, gave us some good tips." — Verified Customer
  - "Way more reasonable prices than any of the mobile services." — Verified Customer
```

---

## STEP 2 — Paste the STEP 1 block above + this prompt into Lovable

> Build a fully functional service-contractor website. Use React + Tailwind + shadcn/ui. Backend: Supabase (Lovable will prompt to connect — say yes).
>
> **The business:** *(the STEP 1 block above)*
>
> ### Pages / sections (single-page, sticky nav, smooth scroll)
> 1. **Hero** — business name in serif, one-line tagline, two CTAs: "Get a Free Quote" (scrolls to Quote form) and "Call Now" (tel: link). Full-bleed background image fitting the trade.
>       - Above the hero, show a thin top banner: "24/7 Emergency Service — Call now" with the phone number as a tel: link.
> 2. **Services** — display each service from STEP 1 as a card with name, starting price, and a one-line description.
> 3. **Quote Request** (CORE FEATURE) — service type dropdown, name, phone, email, service address, optional details/photo upload. On submit: insert into Supabase `quotes` table, show confirmation, fire a Resend email + (optional) SMS to the owner so they can respond fast.
> 4. **Service Area** — bullet list of cities/areas the business serves.
> 5. **Gallery** — 8-image grid showing recent work (before/after where applicable).
> 6. **Reviews** — three testimonial cards using the verbatim Yelp reviews provided in STEP 1.
> 7. **Visit / Contact** — address, embedded Google Map, hours, click-to-call (prominent), Get Directions.
> 8. **Contact form** — name, email, phone, message → Supabase `messages` + owner email.
> 9. **Footer** — name, address, phone, hours, social icons.
>
> ### Functional features (non-negotiable)
> - **Quote system** — Supabase `quotes` table (id, service, name, phone, email, address, details, status, created_at). Email + optional SMS to owner on each new quote.
> - **Contact form** — Supabase `messages` + owner email.
> - **Owner admin dashboard at `/admin`** — Supabase Auth. Two tabs: **Quotes** (table with Contacted / Quoted / Won / Lost statuses, sortable by date and status) and **Messages** (newest first, mark-as-read).
>
> ### Design + SEO
> - Mobile-first, fast, accessible. Use the brand-feel colors from STEP 1.
> - Click-to-call phone visible everywhere on mobile.
> - Serif headings, clean sans body. Subtle scroll animations.
> - Proper title, meta, Open Graph, LocalBusiness JSON-LD.
>
> Build the complete site now. Start with the full layout + quote system, then the admin dashboard.
