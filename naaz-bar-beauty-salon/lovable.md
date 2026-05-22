# Lovable Prompt — Naaz Bar Beauty Salon

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Naaz Bar Beauty Salon
- Type: eyebrow threading studio
- Location: San Jose, CA
- Phone: (408) 226-2264
- Hours:
  - Mon – Sat: 9:30 AM – 7:30 PM
  - Sunday: 10:00 AM – 6:00 PM

## Services — use these exact items and prices
  - Eyebrow Threading ($12) — Precise brow shaping — quick, clean, gentle.
  - Full Face Threading ($45) — Brows, lip, chin, cheeks, forehead — the works.
  - Brow Tint ($18) — Custom-blended tint for fuller-looking brows.
  - Henna Brows ($35) — Natural henna stain — lasts up to two weeks.
  - Lash Lift & Tint ($75) — Lifted, darkened lashes — no extensions needed.
  - Lip & Chin Threading ($10) — Fast, gentle facial hair removal.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Ilana did an excellent job on my eyebrows; the process was quick and painless." — Verified Customer
  - "They always do an amazing job. Ilana and Niki are the best — I've been going to them for 8 years!" — Verified Customer
  - "They shaped my eyebrows perfectly and they look better than ever." — Verified Customer
Overall rating: 4.5 stars from 342 reviews on Yelp. Add a "Read all 342 reviews on Yelp" button linking to https://www.yelp.com/biz/naaz-bar-beauty-salon-san-jose.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Book Appointment" and "Call (408) 226-2264".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a eyebrow threading studio, with a click-to-enlarge lightbox.
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
- Brand feel: warm and feminine — soft dusty rose with gold accents.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Book Appointment" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.5 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
