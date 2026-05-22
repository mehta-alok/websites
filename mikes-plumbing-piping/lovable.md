# Lovable Prompt — Mike's Plumbing and Piping

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Mike's Plumbing and Piping
- Type: trusted local plumbers
- Location: San Jose, CA, San Jose, CA
- Phone: (408) 960-9313
- Hours:
  - Mon – Sun: 24/7 Emergency Service Available

## Services — use these exact items and prices
  - Drain Cleaning (From $99) — Hydro-jet & cable for kitchen, bath, sewer lines.
  - Water Heater Repair (From $200) — Tank or tankless — diagnose and fix same-day.
  - Leak Detection (From $150) — Non-invasive locate, full repair, no guesswork.
  - Faucet & Fixture Install (From $125) — Sinks, faucets, garbage disposals, toilets.
  - Repipe (From $1,500) — Whole-home copper or PEX repipe with warranty.
  - 24/7 Emergency (Same-Day) — Burst pipe? Backed-up sewer? We're on the way.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Mike is the best plumber I have ever worked with. He is very meticulous, honest, and excellent in his work." — Verified Customer
Overall rating: 4.5 stars from 50 reviews on Yelp. Add a "Read all 50 reviews on Yelp" button linking to https://www.yelp.com/biz/mikes-plumbing-and-piping-san-jose.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Get a Free Quote" and "Call (408) 960-9313".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a trusted local plumbers, with a click-to-enlarge lightbox.
4. About — a warm two-paragraph section.
5. Reviews — the real reviews above as cards, plus the overall rating, plus the "Read all reviews on Yelp" button.
6. Visit — an embedded Google Map of the address, the hours, and a click-to-call phone link.
7. Footer — name, address, phone, hours, social icons.

## Functional features (the real backend)
1. Online booking system — the customer picks a service, date, and available time slot, enters name/phone/email, and confirms. Save each request to a Supabase `bookings` table and email the owner via a Supabase edge function (Resend). Generate time slots from the hours above; hide slots already taken; block past dates and closed days.
2. Contact form — name, email, phone, message → save to a Supabase `messages` table and email the owner.
3. Owner admin dashboard at /admin — protected by Supabase Auth login. A Bookings tab (mark each Confirmed / Completed / Cancelled) and a Messages tab (mark as read). Clean and mobile-usable.

## Design
- Premium and modern — it should look like a website that cost $2,000+.
- Brand feel: trustworthy and professional — navy blue with white.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Get a Free Quote" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.5 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
