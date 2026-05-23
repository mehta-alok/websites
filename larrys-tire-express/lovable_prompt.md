# Lovable Prompt — Larry's Tire Express (Hayward)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **Larry's Tire Express**. Real data, real Yelp reviews, real address — already filled in.
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
BUSINESS NAME:   Larry's Tire Express
BUSINESS TYPE:   tire shop
LOCATION:        Hayward, CA
FULL ADDRESS:    750 A Street, Hayward, CA 94541
PHONE:           (510) 581-6020
RATING / VOLUME: 4.6★ from 564 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/larrys-tire-express-hayward
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Mon – Fri: 8:30 AM – 5:30 PM
  - Saturday: 9:00 AM – 3:00 PM
  - Sunday: Closed
TODAY'S HOURS:   8:30 AM – 5:00 PM

MENU / SERVICES (display each as a card with price + description):
  - New Tire Mount — $25/tire — Mount, balance, valve stem, disposal included.
  - Wheel Alignment — From $90 — 4-wheel alignment, computer-precise.
  - Tire Rotation — $30 — Recommended every 5–7K miles. Walk-ins welcome.
  - Flat Repair — $25 — Patch + plug repair — most flats fixable.
  - Used Tires — From $40 — Inspected used tires — major brands.
  - Wheel Balancing — From $60 — Smooth ride, longer tire life, no vibration.

BRAND FEEL:      bold, family-run, dependable — red + black + steel

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "Sal's the best and most knowledgeable guy." — Verified Customer
  - "Great customer service and best price in town!" — Verified Customer
  - "They were quick and made it so easy." — Verified Customer
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
> 6. **Reviews — LIVE from Google** (this is what sells the site). In a Supabase edge function:
>    - Call Places API `findplacefromtext` with `input = "{BUSINESS NAME from STEP 1} {FULL ADDRESS from STEP 1}"` to resolve the `place_id`.
>    - Call Places API `place/details` with that `place_id` and `fields=reviews,rating,user_ratings_total,url`.
>    - Render the 3 most relevant reviews: 5-star row, reviewer's real name + profile photo (from the API response), relative time ("a month ago"), verbatim review text (truncate at ~200 chars with "Read more" linking to Google).
>    - Show the overall rating + total count ("{rating}★ · {count} reviews on Google").
>    - Cache the API response in a Supabase table for 24 hours (Places API has quotas).
>    - Add a prominent "Read all reviews on Google" button linking to the API's returned Maps `url`.
>    - **Fallback** if the API call fails or `GOOGLE_PLACES_API_KEY` isn't set: render the verbatim Yelp reviews from STEP 1 plus an honest rating-and-count callout.
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
> Build the complete site now. Start with the full layout + quote system + live Google reviews, then the admin dashboard.
>
> ### Required environment variables (Lovable will prompt)
> - `GOOGLE_PLACES_API_KEY` — get one at https://console.cloud.google.com/apis (enable "Places API"). Free $200/month credit covers far more than this site will use. **This powers the live Google reviews — the most important authenticity feature.**
> - `RESEND_API_KEY` — get one at https://resend.com (3K emails/month free). Powers the quote/contact email notifications.
