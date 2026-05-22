# Lovable Prompt — All Star Barber Shop

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: All Star Barber Shop
- Type: classic barbershop
- Location: 322 E 3rd Ave, San Mateo, CA
- Phone: (650) 579-7020
- Hours:
  - Mon – Fri: 10:00 AM – 5:00 PM
  - Saturday: 8:00 AM – 3:00 PM
  - Sunday: Closed

## Services — use these exact items and prices
  - Classic Cut ($35) — Precision cut, hot lather neck shave, style.
  - Beard Trim ($20) — Precise beard line-up, shape, trim, oil.
  - Cut + Beard ($50) — Full service — haircut + beard groom.
  - Hot Towel Shave ($40) — Traditional straight razor with hot towel.
  - Kids Cut (12 & under) ($25) — Patient cuts, scared-of-clippers welcome.
  - Senior Cut ($25) — Same craft, kind price.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Gloria actually cares about your hair and is careful to cut it just the way you want." — Verified Customer
  - "Everyone is very nice and the place is always clean." — Verified Customer
  - "Gloria is a master at her trade." — Verified Customer
Overall rating: 4.5 stars from 310 reviews on Yelp. Add a "Read all 310 reviews on Yelp" button linking to https://www.yelp.com/biz/all-star-barber-shop-san-mateo.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Book a Cut" and "Call (650) 579-7020".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a classic barbershop, with a click-to-enlarge lightbox.
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
- Brand feel: refined and masculine — charcoal with bronze accents.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Book a Cut" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.5 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
