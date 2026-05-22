# Lovable Prompt — Ha VL

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Ha VL
- Type: authentic Vietnamese kitchen
- Location: Portland, OR
- Phone: (503) 772-0103
- Hours:
  - Mon – Thu: 11:00 AM – 9:00 PM
  - Fri – Sat: 11:00 AM – 10:00 PM
  - Sunday: 11:00 AM – 9:00 PM

## Menu — use these exact items and prices
  - Pho Tai (Rare Beef) ($13.95) — Classic rice noodle soup, rare beef slices.
  - Pho Dac Biet (Special) ($15.95) — All cuts: rare beef, brisket, tendon, tripe.
  - Bun Bo Hue ($14.95) — Spicy lemongrass beef vermicelli — Hue style.
  - Banh Mi (Classic) ($8.95) — Pâté, cha lua, pickled veg, cilantro, jalapeño.
  - Spring Rolls (2) ($6.95) — Fresh shrimp & pork rolls, peanut sauce.
  - Vermicelli Bowl ($12.95) — Grilled pork or chicken over cool noodles.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "The absolute best and most innovative Vietnamese soup in Portland." — Verified Customer
  - "Two different and delicious soups, different every day." — Verified Customer
  - "Pho is king and queen here!" — Verified Customer
Overall rating: 4.4 stars from 374 reviews on Yelp. Add a "Read all 374 reviews on Yelp" button linking to https://www.yelp.com/biz/ha-vl-portland-3.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Order Online" and "Call (503) 772-0103".
2. Menu — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a authentic Vietnamese kitchen, with a click-to-enlarge lightbox.
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
- Brand feel: warm and traditional — deep red with gold.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Order Online" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.4 rating.

Build the complete site now — the full single-page layout and the reservation request system first, then the admin dashboard.
