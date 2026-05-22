# Lovable Prompt — One Hour Alterations

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: One Hour Alterations
- Type: alterations & tailoring
- Location: 2242 S King Road, San Jose, CA
- Phone: (408) 259-4113
- Hours:
  - Mon – Fri: 10:00 AM – 7:00 PM
  - Saturday: 10:00 AM – 5:00 PM
  - Sunday: Closed

## Services — use these exact items and prices
  - Hem Pants ($15) — Same-day on most pants. Original or blind stitch.
  - Hem Dress / Skirt ($25) — Length adjustment with original detailing.
  - Resize Suit (From $80) — Jacket + pants, shoulders to inseam.
  - Wedding Dress Alteration (From $200) — Fitting, hem, bustle, sleeves — every detail.
  - Zipper Replacement (From $30) — Pants, dress, jacket, bag — exact match.
  - Custom Tailoring (From $100) — Restyle, restructure, repair vintage pieces.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Super fast alterations, same day, cheap, and awesome service!" — Verified Customer
  - "The craftsmanship was flawless. Excellent service, exceptional quality, and a truly thoughtful business owner." — Verified Customer
  - "Same-day alteration, on time, professional." — Verified Customer
Overall rating: 4.6 stars from 130 reviews on Yelp. Add a "Read all 130 reviews on Yelp" button linking to https://www.yelp.com/biz/one-hour-alterations-san-jose.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Drop In Today" and "Call (408) 259-4113".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a alterations & tailoring, with a click-to-enlarge lightbox.
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
- Brand feel: refined and craft-focused — sage green with cream.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Drop In Today" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.6 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
