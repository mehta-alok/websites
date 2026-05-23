# Lovable Prompt — Banh Mi Ba Le (Oakland)

> **What this is.** A ready-to-paste prompt that tells Lovable to build a fully functional website (real booking/reservation/quote system + owner admin dashboard) for **Banh Mi Ba Le**. Real data, real Yelp reviews, real address — already filled in.
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
BUSINESS NAME:   Banh Mi Ba Le
BUSINESS TYPE:   Vietnamese restaurant
LOCATION:        Oakland, CA
FULL ADDRESS:    1909 International Blvd, Oakland, CA 94606
PHONE:           (510) 261-9800
RATING / VOLUME: 4.5★ from 1,581 verified Yelp reviews
YELP URL:        https://www.yelp.com/biz/banh-mi-ba-le-oakland
OWNER EMAIL:     [owner's email — to be added]     ← booking + contact notifications go here
HOURS:
  - Fri – Sun: 7:30 AM – 3:00 PM
  - Mon – Thu: Closed
TODAY'S HOURS:   7:30 AM – 3:00 PM

MENU / SERVICES (display each as a card with price + description):
  - Pho Tai (Rare Beef) — $13.95 — Classic rice noodle soup, rare beef slices.
  - Pho Dac Biet (Special) — $15.95 — All cuts: rare beef, brisket, tendon, tripe.
  - Bun Bo Hue — $14.95 — Spicy lemongrass beef vermicelli — Hue style.
  - Banh Mi (Classic) — $8.95 — Pâté, cha lua, pickled veg, cilantro, jalapeño.
  - Spring Rolls (2) — $6.95 — Fresh shrimp & pork rolls, peanut sauce.
  - Vermicelli Bowl — $12.95 — Grilled pork or chicken over cool noodles.

BRAND FEEL:      authentic, traditional, refined — deep red + warm gold + cream

EXISTING BOOKING URL (optional, can keep or replace with built-in system):
  [owner's existing booking link if any — else leave as click-to-call]

VERBATIM YELP REVIEWS (display these in the Reviews section, exactly as written):
  - "Everything is so good here! Best banh mi sandwiches in the Bay!" — Verified Customer
  - "I've been to Banh Mi Ba Le in Oakland and loved their sandwiches." — Verified Customer
  - "My grilled pork banh mi was great — bread nicely toasted, good balance of veggies to meat." — Verified Customer
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
> 6. **Reviews** — three testimonial cards using the verbatim Yelp reviews provided in STEP 1.
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
> Build the complete site now. Start with the full layout + reservation system, then the admin dashboard.
