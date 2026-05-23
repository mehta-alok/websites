# Lovable Prompt — Family Auto Repair (Fremont)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **Family Auto Repair**. Real data, real Yelp reviews, real address — already filled in.
>
> **How to use.**
> 1. Open https://lovable.dev/ and start a new project.
> 2. Copy everything below (both STEP 1 and STEP 2) and paste it into the chat.
> 3. When Lovable asks to connect Supabase, say yes.
> 4. Add a Resend API key (free 3K emails/mo) when prompted — that powers booking/quote notifications.
> 5. In Supabase Auth, add one user with **the owner**'s email + a password. That's their admin login.
> 6. Publish → get the live URL → send it to the owner.

---

## STEP 1 — Business details (copy this block as-is)

```
BUSINESS NAME:   Family Auto Repair
BUSINESS TYPE:   auto repair shop
LOCATION:        Fremont, CA
FULL ADDRESS:    4299 Peralta Blvd, Fremont, CA 94536
PHONE:           (510) 894-4601
RATING / VOLUME: 4.7★ from 45 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/family-auto-repair-fremont-2
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Mon – Fri: 8:00 AM – 5:00 PM
  - Saturday: 8:00 AM – 1:00 PM
  - Sunday: Closed
TODAY'S HOURS:   8:00 AM – 5:00 PM

MENU / SERVICES (display each as a card with price + description):
  - Oil Change — From $40 — Synthetic blend, filter, top-off all fluids.
  - Brake Service — From $200 — Pads, rotors, fluid flush — safety first.
  - Engine Diagnostic — $90 — Full computer scan, expert diagnosis.
  - Tune-Up — From $150 — Plugs, filters, fluids — full performance check.
  - Transmission Service — From $250 — Fluid + filter for automatic & manual.
  - Tire Rotation — $30 — Even wear, longer tire life, alignment check.

BRAND FEEL:      bold, reliable, no-nonsense — red + black + steel

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "Great service — communicated and updated me on every step. They were very trustworthy." — Verified Customer
  - "My family has been coming to Dave for years. He is always fair and honest." — Verified Customer
```

---

## STEP 2 — Paste the STEP 1 block above + this prompt into Lovable

> Build a fully functional service-contractor website. Use React + Tailwind + shadcn/ui. Backend: Supabase (Lovable will prompt to connect — say yes).
>
> **The business:** *(the STEP 1 block above)*
>
> ### Pages / sections (single-page, sticky nav, smooth scroll)
> 1. **Hero** — business name in serif, one-line tagline, two CTAs: "Get a Free Quote" (scrolls to Quote form) and "Call Now" (tel: link). Full-bleed background image fitting the trade.
>    
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
