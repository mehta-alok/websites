# Lovable Prompt — Fremont Smog Test Only

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Fremont Smog Test Only
- Type: STAR-certified smog station
- Location: 4299 Peralta Blvd, Ste E, Fremont, CA
- Phone: (510) 744-9955
- Hours:
  - Mon – Sat: 8:00 AM – 6:00 PM
  - Sunday: 9:00 AM – 4:00 PM

## Services — use these exact items and prices
  - Smog Test (Most Vehicles) ($50) — STAR Certified, fast in-and-out service.
  - Test Only ($40) — Renewals only — no repairs needed.
  - Smog Repair + Re-Test (From $200) — Failed? We diagnose, fix, and re-test free.
  - Diesel Smog ($80) — Trucks and diesel light vehicles welcome.
  - DMV Renewal ($30) — On-site DMV registration renewal service.
  - Trailer / Light Vehicle ($50) — Most trailers and light commercial vehicles.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Fast, thorough and professional — when someone takes less time than expected, that's a savings in itself!" — Verified Customer
  - "Super professional and efficient." — Verified Customer
  - "Service is super fast, around 10 minutes, and really friendly and nice." — Verified Customer
Overall rating: 4.8 stars from 482 reviews on Yelp. Add a "Read all 482 reviews on Yelp" button linking to https://www.yelp.com/biz/fremont-smog-test-only-fremont.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Walk In Today" and "Call (510) 744-9955".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a STAR-certified smog station, with a click-to-enlarge lightbox.
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
- Brand feel: fast and energetic — orange with charcoal.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Walk In Today" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.8 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
