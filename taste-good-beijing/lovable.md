# Lovable Prompt — Taste Good Beijing

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Taste Good Beijing
- Type: authentic Chinese kitchen
- Location: 76 S Abel Street, Milpitas, CA
- Phone: (408) 262-9439
- Hours:
  - Mon – Thu: 10:30 AM – 9:00 PM
  - Fri – Sun: 10:30 AM – 9:30 PM

## Menu — use these exact items and prices
  - Peking Duck (Whole) ($48) — 48-hour brined, signature crisp skin. Pre-order.
  - Mapo Tofu ($13.95) — Sichuan-style soft tofu in spicy bean sauce.
  - Dim Sum (5 pcs) ($8.95) — Shrimp har gow, siu mai, char siu bao.
  - Beef & Broccoli ($15.95) — Tender flank steak, broccoli, brown sauce.
  - Lo Mein ($12.95) — Egg noodles, vegetables, choice of protein.
  - Hot & Sour Soup ($6.95) — Bamboo, tofu, mushroom, egg ribbons.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Best Peking duck in the San Jose–Milpitas area." — Verified Customer
  - "As a person who lived in China for most of my life, their cuisine is authentic and tasteful." — Verified Customer
  - "The lamb skewers are flavorful, juicy, and not dry." — Verified Customer
Overall rating: 4.3 stars from 338 reviews on Yelp. Add a "Read all 338 reviews on Yelp" button linking to https://www.yelp.com/biz/taste-good-beijing-milpitas.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Order Online" and "Call (408) 262-9439".
2. Menu — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a authentic Chinese kitchen, with a click-to-enlarge lightbox.
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
- Brand feel: bold and traditional — red with gold.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Order Online" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.3 rating.

Build the complete site now — the full single-page layout and the reservation request system first, then the admin dashboard.
