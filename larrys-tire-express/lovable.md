# Lovable Prompt — Larry's Tire Express

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Larry's Tire Express
- Type: local tire shop
- Location: 750 A Street, Hayward, CA
- Phone: (510) 581-6020
- Hours:
  - Mon – Fri: 8:30 AM – 5:30 PM
  - Saturday: 9:00 AM – 3:00 PM
  - Sunday: Closed

## Services — use these exact items and prices
  - New Tire Mount ($25/tire) — Mount, balance, valve stem, disposal included.
  - Wheel Alignment (From $90) — 4-wheel alignment, computer-precise.
  - Tire Rotation ($30) — Recommended every 5–7K miles. Walk-ins welcome.
  - Flat Repair ($25) — Patch + plug repair — most flats fixable.
  - Used Tires (From $40) — Inspected used tires — major brands.
  - Wheel Balancing (From $60) — Smooth ride, longer tire life, no vibration.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Sal's the best and most knowledgeable guy." — Verified Customer
  - "Great customer service and best price in town!" — Verified Customer
  - "They were quick and made it so easy." — Verified Customer
Overall rating: 4.6 stars from 564 reviews on Yelp. Add a "Read all 564 reviews on Yelp" button linking to https://www.yelp.com/biz/larrys-tire-express-hayward.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Get a Tire Quote" and "Call (510) 581-6020".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a local tire shop, with a click-to-enlarge lightbox.
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
- Brand feel: bold and dependable — strong red with steel and black.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Get a Tire Quote" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.6 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
