# Lovable Prompt — Monet Spa & Nails

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Monet Spa & Nails
- Type: premier nail salon
- Location: Sacramento, CA
- Phone: (916) 457-7018
- Hours:
  - Mon – Sat: 9:30 AM – 7:30 PM
  - Sunday: 10:00 AM – 6:00 PM

## Services — use these exact items and prices
  - Classic Manicure ($30) — Shape, cuticle care, hand massage, polish.
  - Gel Manicure ($45) — Long-lasting gel polish — chip-resistant 2–3 weeks.
  - Spa Pedicure ($40) — Soak, exfoliation, callus removal, leg massage.
  - Gel Pedicure ($55) — Spa pedicure with chip-resistant gel finish.
  - Acrylic Full Set ($65) — Custom-length extensions, shaped to your style.
  - Custom Nail Art ($10+) — Hand-painted designs, chrome, glitter, French.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "By far the best nail salon I've been to in Sacramento." — Verified Customer
  - "Technicians are thorough and detailed, not concerned about turning over clients." — Verified Customer
  - "Literally the best nails I've gotten in Sac." — Verified Customer
Overall rating: 4.5 stars from 394 reviews on Yelp. Add a "Read all 394 reviews on Yelp" button linking to https://www.yelp.com/biz/monet-spa-and-nails-sacramento-2.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Book Appointment" and "Call (916) 457-7018".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a premier nail salon, with a click-to-enlarge lightbox.
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
