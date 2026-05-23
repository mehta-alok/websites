# Lovable Prompt — All Star Barber Shop (San Mateo)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **All Star Barber Shop**. Real data, real Yelp reviews, real address — already filled in.
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
BUSINESS NAME:   All Star Barber Shop
BUSINESS TYPE:   barbershop
LOCATION:        San Mateo, CA
FULL ADDRESS:    322 E 3rd Ave, San Mateo, CA 94401
PHONE:           (650) 579-7020
RATING / VOLUME: 4.5★ from 310 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/all-star-barber-shop-san-mateo
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Mon – Fri: 10:00 AM – 5:00 PM
  - Saturday: 8:00 AM – 3:00 PM
  - Sunday: Closed
TODAY'S HOURS:   10:00 AM – 5:00 PM

MENU / SERVICES (display each as a card with price + description):
  - Classic Cut — $35 — Precision cut, hot lather neck shave, style.
  - Beard Trim — $20 — Precise beard line-up, shape, trim, oil.
  - Cut + Beard — $50 — Full service — haircut + beard groom.
  - Hot Towel Shave — $40 — Traditional straight razor with hot towel.
  - Kids Cut (12 & under) — $25 — Patient cuts, scared-of-clippers welcome.
  - Senior Cut — $25 — Same craft, kind price.

BRAND FEEL:      classic, masculine, craft — charcoal + bronze accents

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "Gloria actually cares about your hair and is careful to cut it just the way you want." — Verified Customer
  - "Everyone is very nice and the place is always clean." — Verified Customer
  - "Gloria is a master at her trade." — Verified Customer
```

---

## STEP 2 — Paste the STEP 1 block above + this prompt into Lovable

> Build a fully functional salon website. Use React + Tailwind + shadcn/ui. Backend: Supabase (Lovable will prompt to connect — say yes).
>
> **The business:** *(the STEP 1 block above)*
>
> ### Pages / sections (single-page, sticky nav, smooth scroll)
> 1. **Hero** — salon name in serif, one-line tagline, two CTAs: "Book Appointment" (scrolls to Booking) and "Call" (tel: link). Full-bleed background image fitting the salon type.
> 2. **Services** — display each service from STEP 1 as a card with name, price, and one-line description.
> 3. **Booking** (CORE FEATURE) — customer picks a service, picks a date (calendar, no past dates, no closed days), picks an available 30-minute time slot, enters name/phone/email, confirms. On submit: insert into Supabase `bookings` table, show confirmation, fire a Resend email to the owner.
> 4. **Gallery** — 8-image responsive grid with click-to-enlarge lightbox.
> 5. **Reviews — LIVE from Google** (this is what sells the site). In a Supabase edge function:
>    - Call Places API `findplacefromtext` with `input = "{BUSINESS NAME from STEP 1} {FULL ADDRESS from STEP 1}"` to resolve the `place_id`.
>    - Call Places API `place/details` with that `place_id` and `fields=reviews,rating,user_ratings_total,url`.
>    - Render the 3 most relevant reviews: 5-star row, reviewer's real name + profile photo (from the API response), relative time ("a month ago"), verbatim review text (truncate at ~200 chars with "Read more" linking to Google).
>    - Show the overall rating + total count ("{rating}★ · {count} reviews on Google").
>    - Cache the API response in a Supabase table for 24 hours (Places API has quotas).
>    - Add a prominent "Read all reviews on Google" button linking to the API's returned Maps `url`.
>    - **Fallback** if the API call fails or `GOOGLE_PLACES_API_KEY` isn't set: render the verbatim Yelp reviews from STEP 1 plus an honest rating-and-count callout.
> 6. **About** — short, warm 2-paragraph blurb about the salon.
> 7. **Visit** — full address, embedded Google Map of the real address, hours table, click-to-call phone, "Get Directions" button.
> 8. **Contact** — short form (name, email, phone, message) → Supabase `messages` table + owner email.
> 9. **Footer** — name, address, phone, hours, social icons.
>
> ### Functional features (non-negotiable)
> - **Booking system** — Supabase `bookings` table (id, service, date, time, name, phone, email, status, created_at). Already-booked slots for the chosen date are not selectable. Resend email to owner on each booking.
> - **Contact form** — Supabase `messages` table + owner email.
> - **Owner admin dashboard at `/admin`** — Supabase Auth (email + password). Two tabs: **Bookings** (table sorted by date, Confirmed / Completed / Cancelled buttons, today highlighted) and **Messages** (newest first, mark-as-read toggle).
>
> ### Design + SEO
> - Premium, modern, mobile-first. Use the brand-feel colors from STEP 1.
> - Serif font for headings, clean sans for body.
> - Floating "Book Now" button bottom-right on mobile.
> - Subtle scroll animations. Accessible.
> - Proper title, meta, Open Graph, LocalBusiness JSON-LD.
>
> Build the complete site now. Start with the full layout + booking system + live Google reviews, then the admin dashboard.
>
> ### Required environment variables (Lovable will prompt)
> - `GOOGLE_PLACES_API_KEY` — get one at https://console.cloud.google.com/apis (enable "Places API"). Free $200/month credit covers far more than this site will use. **This powers the live Google reviews — the most important authenticity feature.**
> - `RESEND_API_KEY` — get one at https://resend.com (3K emails/month free). Powers the booking/contact email notifications.
