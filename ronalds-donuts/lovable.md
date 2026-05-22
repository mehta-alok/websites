# Lovable Prompt — Ronald's Donuts

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Ronald's Donuts
- Type: beloved local donut shop
- Location: Las Vegas, NV
- Phone: (702) 873-1032
- Hours:
  - Mon – Fri: 5:30 AM – 1:00 PM
  - Sat – Sun: 6:00 AM – 1:00 PM

## Menu — use these exact items and prices
  - Classic Glazed ($1.50) — The original — light, airy, glazed fresh hourly.
  - Old-Fashioned ($2.00) — Cake donut, crisp edges, dipped in glaze.
  - Apple Fritter ($3.75) — Hand-folded, loaded with cinnamon apples.
  - Filled Donuts ($2.50) — Bavarian cream, raspberry, lemon, custard.
  - Dozen Box ($15) — Mix & match any flavors — feeds the whole office.
  - Coffee & Donut ($4) — Fresh-brewed coffee plus any classic donut.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "They have the best donuts in Vegas, hands down." — Verified Customer
  - "Easily the best vegan donuts I've tried." — Verified Customer
Overall rating: 4.7 stars from 1,214 reviews on Yelp. Add a "Read all 1,214 reviews on Yelp" button linking to https://www.yelp.com/biz/ronalds-donuts-las-vegas.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "See the Menu" and "Call (702) 873-1032".
2. Menu — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a beloved local donut shop, with a click-to-enlarge lightbox.
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
- Brand feel: warm and feminine — soft dusty rose with gold accents.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "See the Menu" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.7 rating.

Build the complete site now — the full single-page layout and the reservation request system first, then the admin dashboard.
