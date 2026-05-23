# Lovable Prompt — Naaz Bar Beauty Salon (San Jose)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **Naaz Bar Beauty Salon**. Real data, real Yelp reviews, real address — already filled in.
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
BUSINESS NAME:   Naaz Bar Beauty Salon
BUSINESS TYPE:   eyebrow threading studio
LOCATION:        San Jose, CA
FULL ADDRESS:    San Jose, CA
PHONE:           (408) 226-2264
RATING / VOLUME: 4.5★ from 342 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/naaz-bar-beauty-salon-san-jose
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Mon – Sat: 9:30 AM – 7:30 PM
  - Sunday: 10:00 AM – 6:00 PM
TODAY'S HOURS:   10:00 AM – 8:00 PM

MENU / SERVICES (display each as a card with price + description):
  - Eyebrow Threading — $12 — Precise brow shaping — quick, clean, gentle.
  - Full Face Threading — $45 — Brows, lip, chin, cheeks, forehead — the works.
  - Brow Tint — $18 — Custom-blended tint for fuller-looking brows.
  - Henna Brows — $35 — Natural henna stain — lasts up to two weeks.
  - Lash Lift & Tint — $75 — Lifted, darkened lashes — no extensions needed.
  - Lip & Chin Threading — $10 — Fast, gentle facial hair removal.

BRAND FEEL:      clean, feminine, modern — rose + gold accents

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "Ilana did an excellent job on my eyebrows; the process was quick and painless." — Verified Customer
  - "They always do an amazing job. Ilana and Niki are the best — I've been going to them for 8 years!" — Verified Customer
  - "They shaped my eyebrows perfectly and they look better than ever." — Verified Customer
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
> 5. **Reviews** — three testimonial cards using the verbatim Yelp reviews provided in STEP 1.
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
> Build the complete site now. Start with the full layout + booking system, then the admin dashboard.
