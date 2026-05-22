# Lovable Prompt — Hasumi Sushi

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Hasumi Sushi
- Type: authentic Japanese restaurant
- Location: 3116 Oak Rd Ste A, Walnut Creek, CA
- Phone: (925) 949-8041
- Hours:
  - Mon – Thu: 11:00 AM – 9:00 PM
  - Fri – Sat: 11:00 AM – 10:00 PM
  - Sunday: 11:00 AM – 9:00 PM

## Menu — use these exact items and prices
  - Spicy Tuna Roll ($8) — Fresh tuna, spicy mayo, tobiko.
  - Salmon Sashimi (8 pc) ($16) — Premium salmon, ginger, wasabi.
  - Tonkatsu Bento ($15) — Crispy pork cutlet, rice, miso, salad.
  - Tempura Udon ($13) — Hand-cut noodles, shrimp & vegetable tempura.
  - Chirashi Don ($22) — 12 pieces sashimi over sushi rice.
  - Mochi Ice Cream (3 pc) ($7) — Green tea, mango, strawberry.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Hasumi is such a gem in Walnut Creek!" — Verified Customer
  - "It's consistently the most fresh sushi and always tasty." — Verified Customer
  - "I thought the fish was very fresh!" — Verified Customer
Overall rating: 4.2 stars from 379 reviews on Yelp. Add a "Read all 379 reviews on Yelp" button linking to https://www.yelp.com/biz/hasumi-sushi-walnut-creek.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Order Online" and "Call (925) 949-8041".
2. Menu — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a authentic Japanese restaurant, with a click-to-enlarge lightbox.
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
- Brand feel: refined and masculine — charcoal with bronze accents.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Order Online" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.2 rating.

Build the complete site now — the full single-page layout and the reservation request system first, then the admin dashboard.
