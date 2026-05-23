# Lovable Prompt — Monet Spa & Nails (Sacramento)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **Monet Spa & Nails**. Real data, real Yelp reviews, real address — already filled in.
>
> **How to use.**
> 1. Open https://lovable.dev/ and start a new project.
> 2. Copy everything below (both STEP 1 and STEP 2) and paste it into the chat.
> 3. When Lovable asks to connect Supabase, say yes.
> 4. Add a Resend API key (free 3K emails/mo) when prompted — that powers booking/quote notifications.
> 5. In Supabase Auth, add one user with **Tracy**'s email + a password. That's their admin login.
> 6. Publish → get the live URL → send it to the owner.

---

## STEP 1 — Business details (copy this block as-is)

```
BUSINESS NAME:   Monet Spa & Nails
BUSINESS TYPE:   nail salon
LOCATION:        Sacramento, CA
FULL ADDRESS:    Sacramento, CA
PHONE:           (916) 457-7018
RATING / VOLUME: 4.5★ from 394 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/monet-spa-and-nails-sacramento-2
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Mon – Sat: 9:30 AM – 7:30 PM
  - Sunday: 10:00 AM – 6:00 PM
TODAY'S HOURS:   9:30 AM – 7:30 PM

MENU / SERVICES (display each as a card with price + description):
  - Classic Manicure — $30 — Shape, cuticle care, hand massage, polish.
  - Gel Manicure — $45 — Long-lasting gel polish — chip-resistant 2–3 weeks.
  - Spa Pedicure — $40 — Soak, exfoliation, callus removal, leg massage.
  - Gel Pedicure — $55 — Spa pedicure with chip-resistant gel finish.
  - Acrylic Full Set — $65 — Custom-length extensions, shaped to your style.
  - Custom Nail Art — $10+ — Hand-painted designs, chrome, glitter, French.

BRAND FEEL:      warm, feminine, premium — dusty rose + soft gold accents

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "By far the best nail salon I've been to in Sacramento." — Verified Customer
  - "Technicians are thorough and detailed, not concerned about turning over clients." — Verified Customer
  - "Literally the best nails I've gotten in Sac." — Verified Customer
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
