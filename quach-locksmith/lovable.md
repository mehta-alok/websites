# Lovable Prompt — Quach's Locksmith

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Quach's Locksmith
- Type: trusted local locksmiths
- Location: 106 International Blvd, Oakland, CA
- Phone: (510) 839-8888
- Hours:
  - Mon – Fri: 10:30 AM – 6:00 PM
  - Saturday: 11:00 AM – 4:00 PM
  - Sunday: By appointment

## Services — use these exact items and prices
  - Re-Key Locks ($50/lock) — Same lock, new key — landlord and tenant favorite.
  - Lockout Service (From $75) — House, car, business — fast 30-min response.
  - New Lock Install (From $120) — Deadbolts, smart locks, high-security cylinders.
  - Auto Key Programming (From $80) — Transponder, smart key, fob — 99% of vehicles.
  - Master Key System (From $250) — One key for multiple doors. Commercial spec.
  - Safe Combination Reset (From $95) — Floor safes, gun safes, office safes.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "This is the best locksmith in Oakland. They copied hard-to-cut and old keys that most places could not." — Verified Customer
  - "Quach herself was there to help — really friendly, gave us some good tips." — Verified Customer
  - "Way more reasonable prices than any of the mobile services." — Verified Customer
Overall rating: 4.5 stars from 65 reviews on Yelp. Add a "Read all 65 reviews on Yelp" button linking to https://www.yelp.com/biz/quach-locksmith-oakland-4.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Call for Service" and "Call (510) 839-8888".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a trusted local locksmiths, with a click-to-enlarge lightbox.
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
- Brand feel: secure and premium — dark tones with gold accents.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Call for Service" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.5 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
