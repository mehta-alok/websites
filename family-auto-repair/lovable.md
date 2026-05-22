# Lovable Prompt — Family Auto Repair

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Family Auto Repair
- Type: trusted local auto shop
- Location: 4299 Peralta Blvd, Fremont, CA
- Phone: (510) 894-4601
- Hours:
  - Mon – Fri: 8:00 AM – 5:00 PM
  - Saturday: 8:00 AM – 1:00 PM
  - Sunday: Closed

## Services — use these exact items and prices
  - Oil Change (From $40) — Synthetic blend, filter, top-off all fluids.
  - Brake Service (From $200) — Pads, rotors, fluid flush — safety first.
  - Engine Diagnostic ($90) — Full computer scan, expert diagnosis.
  - Tune-Up (From $150) — Plugs, filters, fluids — full performance check.
  - Transmission Service (From $250) — Fluid + filter for automatic & manual.
  - Tire Rotation ($30) — Even wear, longer tire life, alignment check.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Great service — communicated and updated me on every step. They were very trustworthy." — Verified Customer
  - "My family has been coming to Dave for years. He is always fair and honest." — Verified Customer
Overall rating: 4.7 stars from 45 reviews on Yelp. Add a "Read all 45 reviews on Yelp" button linking to https://www.yelp.com/biz/family-auto-repair-fremont-2.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Schedule Service" and "Call (510) 894-4601".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a trusted local auto shop, with a click-to-enlarge lightbox.
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
- Brand feel: bold and dependable — strong red with steel and black.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Schedule Service" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.7 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
