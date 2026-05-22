# Lovable Prompt — La Piñata Taqueria

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: La Piñata Taqueria
- Type: authentic Mexican kitchen
- Location: 809 Broadway St, Vallejo, CA
- Phone: (707) 334-8381
- Hours:
  - Mon – Fri: 11:00 AM – 9:00 PM
  - Sat – Sun: Closed

## Menu — use these exact items and prices
  - Tacos al Pastor ($3.50) — Marinated pork, pineapple, onion, cilantro.
  - Carne Asada Burrito ($11.50) — Grilled steak, beans, rice, salsa, guac.
  - Carnitas Plate ($14.95) — Slow-braised pork, rice, beans, tortillas.
  - Cheese Quesadilla ($8.50) — Three-cheese, grilled flour tortilla.
  - Enchiladas (3) ($13.95) — Cheese or chicken, red or green sauce.
  - Family Combo ($26.95) — 4 burritos + chips & salsa. Feeds 4.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "The pastor is probably the best I've had anywhere!" — Verified Customer
  - "Always a good day when you can indulge in the best burrito in the Bay Area." — Verified Customer
Overall rating: 4.5 stars from 396 reviews on Yelp. Add a "Read all 396 reviews on Yelp" button linking to https://www.yelp.com/biz/la-pi%C3%B1ata-taqueria-vallejo.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Order Online" and "Call (707) 334-8381".
2. Menu — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a authentic Mexican kitchen, with a click-to-enlarge lightbox.
4. About — a warm two-paragraph section.
5. Reviews — the real reviews above as cards, plus the overall rating, plus the "Read all reviews on Yelp" button.
6. Visit — an embedded Google Map of the address, the hours, and a click-to-call phone link.
7. Footer — name, address, phone, hours, social icons.

## Functional features (the real backend)
1. Reservation request system — the customer picks a party size and time, enters name/phone/email, and confirms. Save each request to a Supabase `bookings` table and email the owner via a Supabase edge function (Resend). Generate time slots from the hours above; hide slots already taken; block past dates and closed days.
2. Contact form — name, email, phone, message → save to a Supabase `messages` table and email the owner.
3. Owner admin dashboard at /admin — protected by Supabase Auth login. A Bookings tab (mark each Confirmed / Completed / Cancelled) and a Messages tab (mark as read). Clean and mobile-usable.

## Design
- Premium and modern — it should look like a website that cost $2,000+.
- Brand feel: warm and appetizing — terracotta with fresh green.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Order Online" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.5 rating.

Build the complete site now — the full single-page layout and the reservation request system first, then the admin dashboard.
