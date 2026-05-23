# Lovable Prompt — Annie's Donuts (Portland)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **Annie's Donuts**. Real data, real Yelp reviews, real address — already filled in.
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
BUSINESS NAME:   Annie's Donuts
BUSINESS TYPE:   donut shop
LOCATION:        Portland, OR
FULL ADDRESS:    Portland, OR
PHONE:           (503) 284-2752
RATING / VOLUME: 4.6★ from 271 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/annies-donuts-portland
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Mon – Fri: 5:30 AM – 1:00 PM
  - Sat – Sun: 6:00 AM – 1:00 PM
TODAY'S HOURS:   Open 24 Hours

MENU / SERVICES (display each as a card with price + description):
  - Classic Glazed — $1.50 — The original — light, airy, glazed fresh hourly.
  - Old-Fashioned — $2.00 — Cake donut, crisp edges, dipped in glaze.
  - Apple Fritter — $3.75 — Hand-folded, loaded with cinnamon apples.
  - Filled Donuts — $2.50 — Bavarian cream, raspberry, lemon, custard.
  - Dozen Box — $15 — Mix & match any flavors — feeds the whole office.
  - Coffee & Donut — $4 — Fresh-brewed coffee plus any classic donut.

BRAND FEEL:      fresh, cozy, friendly — soft pink + cream

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "Best little doughnut shop. When you want doughnuts that taste good, go to Annie's." — Verified Customer
  - "Forget the long lines elsewhere — this is the REAL thing. Old-fashioned, traditional donuts." — Verified Customer
  - "The best Portland has to offer." — Verified Customer
```

---

## STEP 2 — Paste the STEP 1 block above + this prompt into Lovable

> Build a fully functional restaurant website. Use React + Tailwind + shadcn/ui. Backend: Supabase (Lovable will prompt to connect — say yes).
>
> **The business:** *(the STEP 1 block above)*
>
> ### Pages / sections (single-page, sticky nav, smooth scroll)
> 1. **Hero** — restaurant name in serif, one-line tagline matching the brand feel, two CTAs: "Reserve a Table" (scrolls to Reservations) and "Order Online" (opens a placeholder URL — owner adds DoorDash/Grubhub/Uber Eats links). Full-bleed food background image, dark overlay for contrast.
> 2. **Menu** — display every dish from STEP 1 as cards with name, price, and one-line description. Group naturally if needed (Apps, Mains, Sides, Drinks).
> 3. **Reservations** (CORE FEATURE) — date picker (no past dates, no closed days), 30-minute time slots within business hours, party-size dropdown (1–10), name/phone/email + optional notes. On submit: insert into Supabase `reservations` table, show confirmation, fire a Resend email to the owner.
> 4. **Online Ordering** — three big buttons linking to DoorDash, Grubhub, Uber Eats (placeholder URLs — owner fills in).
> 5. **Gallery** — 8-image responsive grid with click-to-enlarge lightbox. Use tasteful food photos.
> 6. **Reviews — LIVE from Google** (this is what sells the site). In a Supabase edge function:
>    - Call Places API `findplacefromtext` with `input = "{BUSINESS NAME from STEP 1} {FULL ADDRESS from STEP 1}"` to resolve the `place_id`.
>    - Call Places API `place/details` with that `place_id` and `fields=reviews,rating,user_ratings_total,url`.
>    - Render the 3 most relevant reviews: 5-star row, reviewer's real name + profile photo (from the API response), relative time ("a month ago"), verbatim review text (truncate at ~200 chars with "Read more" linking to Google).
>    - Show the overall rating + total count ("{rating}★ · {count} reviews on Google").
>    - Cache the API response in a Supabase table for 24 hours (Places API has quotas).
>    - Add a prominent "Read all reviews on Google" button linking to the API's returned Maps `url`.
>    - **Fallback** if the API call fails or `GOOGLE_PLACES_API_KEY` isn't set: render the verbatim Yelp reviews from STEP 1 plus an honest rating-and-count callout.
> 7. **Visit** — full address, embedded Google Map of the real address, hours table, click-to-call phone, "Get Directions" button.
> 8. **Contact** — short form (name, email, phone, message) → Supabase `messages` table + owner email.
> 9. **Footer** — name, address, phone, hours, social icons (Yelp / Facebook / Instagram).
>
> ### Functional features (non-negotiable)
> - **Reservation system** — Supabase `reservations` table (id, date, time, party_size, name, phone, email, notes, status, created_at). Already-booked slots not selectable for the same date. Resend email to owner on each booking.
> - **Contact form** — Supabase `messages` table + owner email.
> - **Owner admin dashboard at `/admin`** — Supabase Auth (email + password). Two tabs: **Reservations** (table sorted by date, with Seated / No-Show / Cancelled buttons, today's bookings highlighted) and **Messages** (newest first, mark-as-read toggle).
>
> ### Design + SEO
> - Premium, modern, mobile-first. Use the brand-feel colors from STEP 1.
> - Serif font (Playfair Display or similar) for headings; clean sans (Inter) for body.
> - Floating "Reserve a Table" button bottom-right on mobile.
> - Subtle scroll animations. Accessible: proper alt text, contrast, keyboard nav.
> - Proper page title, meta description, Open Graph tags, and LocalBusiness JSON-LD with name, address, phone, hours, and rating.
> - Semantic HTML.
>
> Build the complete site now. Start with the full layout + reservation system + live Google reviews, then the admin dashboard.
>
> ### Required environment variables (Lovable will prompt)
> - `GOOGLE_PLACES_API_KEY` — get one at https://console.cloud.google.com/apis (enable "Places API"). Free $200/month credit covers far more than this site will use. **This powers the live Google reviews — the most important authenticity feature.**
> - `RESEND_API_KEY` — get one at https://resend.com (3K emails/month free). Powers the reservation/contact email notifications.
