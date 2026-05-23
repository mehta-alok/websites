# Lovable Prompt — Mike's Plumbing and Piping (San Jose)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **Mike's Plumbing and Piping**. Real data, real Yelp reviews, real address — already filled in.
>
> **How to use.**
> 1. Open https://lovable.dev/ and start a new project.
> 2. Copy everything below (both STEP 1 and STEP 2) and paste it into the chat.
> 3. When Lovable asks to connect Supabase, say yes.
> 4. Add a Resend API key (free 3K emails/mo) when prompted — that powers booking/quote notifications.
> 5. In Supabase Auth, add one user with **Mike**'s email + a password. That's their admin login.
> 6. Publish → get the live URL → send it to the owner.

---

## STEP 1 — Business details (copy this block as-is)

```
BUSINESS NAME:   Mike's Plumbing and Piping
BUSINESS TYPE:   plumbing service
LOCATION:        San Jose, CA
FULL ADDRESS:    San Jose, CA, San Jose, CA 95111
PHONE:           (408) 960-9313
RATING / VOLUME: 4.5★ from 50 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/mikes-plumbing-and-piping-san-jose
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Mon – Sun: 24/7 Emergency Service Available
TODAY'S HOURS:   24/7 Emergency

MENU / SERVICES (display each as a card with price + description):
  - Drain Cleaning — From $99 — Hydro-jet & cable for kitchen, bath, sewer lines.
  - Water Heater Repair — From $200 — Tank or tankless — diagnose and fix same-day.
  - Leak Detection — From $150 — Non-invasive locate, full repair, no guesswork.
  - Faucet & Fixture Install — From $125 — Sinks, faucets, garbage disposals, toilets.
  - Repipe — From $1,500 — Whole-home copper or PEX repipe with warranty.
  - 24/7 Emergency — Same-Day — Burst pipe? Backed-up sewer? We're on the way.

BRAND FEEL:      trustworthy, professional, reliable — navy + gold accents

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "Mike is the best plumber I have ever worked with. He is very meticulous, honest, and excellent in his work." — Verified Customer
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
