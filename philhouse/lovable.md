# Lovable Prompt — PhilHouse

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: PhilHouse
- Type: authentic Filipino kitchen
- Location: 2110 Spring Rd Ste 24A, Vallejo, CA
- Phone: (707) 645-8971
- Hours:
  - Mon – Thu: 11:00 AM – 9:00 PM
  - Fri – Sat: 11:00 AM – 10:00 PM
  - Sunday: 11:00 AM – 9:00 PM

## Menu — use these exact items and prices
  - Chicken Adobo Plate ($14) — Slow-braised in soy-vinegar with garlic & peppercorn.
  - Pork Sisig ($13) — Crispy chopped pork with onion, chili, calamansi.
  - Lumpia Shanghai (5 pcs) ($7) — Crispy pork & vegetable rolls, sweet chili dip.
  - Pancit Bihon ($11) — Stir-fried rice noodles with veg & meat.
  - Lechon Kawali ($16) — Deep-fried crispy pork belly, vinegar dip.
  - Halo-Halo ($8) — Shaved ice w/ ube, leche flan, sweet beans.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Sarap — delicious!" — Verified Customer
  - "The area always looks clean and the food seems fresh every time." — Verified Customer
Overall rating: 4.3 stars from 158 reviews on Yelp. Add a "Read all 158 reviews on Yelp" button linking to https://www.yelp.com/biz/philhouse-vallejo.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Order Online" and "Call (707) 645-8971".
2. Menu — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a authentic Filipino kitchen, with a click-to-enlarge lightbox.
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
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.3 rating.

Build the complete site now — the full single-page layout and the reservation request system first, then the admin dashboard.
