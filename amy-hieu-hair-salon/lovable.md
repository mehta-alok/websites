# Lovable Prompt — Amy Hieu Hair Salon

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Amy Hieu Hair Salon
- Type: hair salon
- Location: Houston, TX
- Phone: (281) 561-8066
- Hours:
  - Mon – Sat: 9:30 AM – 7:30 PM
  - Sunday: 10:00 AM – 6:00 PM

## Services — use these exact items and prices
  - Haircut ($50+) — Consultation + precision cut + styling.
  - Single Process Color ($120+) — Roots and all-over color, gloss finish.
  - Highlights ($180+) — Foil highlights, tone correction, gloss.
  - Balayage ($250+) — Hand-painted balayage, custom blend, toner included.
  - Blowout ($45) — Wash + blow-dry style. Salon-finish hair in 30 min.
  - Keratin Smoothing ($300+) — Frizz-free, smooth hair lasting 3–4 months.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "Highly recommend Amy's balayage. Very natural and it lasts me half a year." — Verified Customer
  - "Amy fixed my hair and gave me great advice on how to take care of it." — Verified Customer
  - "She and her staff are very friendly and efficient, on top of having great coloring skills." — Verified Customer
Overall rating: 4.5 stars from 1,067 reviews on Yelp. Add a "Read all 1,067 reviews on Yelp" button linking to https://www.yelp.com/biz/amy-hieu-hair-salon-houston-2.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Book Appointment" and "Call (281) 561-8066".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a hair salon, with a click-to-enlarge lightbox.
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
- Brand feel: elegant and modern — lavender and deep purple.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Book Appointment" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.5 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
