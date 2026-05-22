# Lovable Prompt — Phoenix Appliance Services

Paste everything below the line into Lovable as one message. When Lovable asks to connect Supabase, say yes — that powers the booking + owner dashboard. Then add a Resend API key for email notifications.

---

Build a modern, fully functional website for a local business — real backend with Supabase, not a static page. Use React, Tailwind, and shadcn/ui.

## The business
- Name: Phoenix Appliance Services
- Type: appliance repair experts
- Location: Phoenix, AZ
- Phone: (623) 292-7152
- Hours:
  - Mon – Fri: 8:00 AM – 6:00 PM
  - Saturday: 9:00 AM – 4:00 PM
  - Sunday: Emergency only

## Services — use these exact items and prices
  - Refrigerator Repair (From $120) — Cooling, leaks, ice maker — all major brands.
  - Washer & Dryer Repair (From $110) — Won't spin, drain, or heat — same-day fix.
  - Oven & Stove Repair (From $115) — Heating elements, igniters, control boards.
  - Dishwasher Repair (From $105) — Drainage, leaks, cleaning performance.
  - Diagnostic Visit ($70) — Full inspection — fee waived with any repair.
  - Same-Day Service (Available) — Most repairs done in one visit. Call early.

## Real customer reviews — display these VERBATIM as testimonial cards
These are real reviews from this business's Yelp page. Do not alter the wording.
  - "I've used Phoenix Appliance for a stove, dishwasher, and dryer, and will never call anyone else!" — Verified Customer
  - "Vladimir is a good, honest person who can fix anything fairly." — Verified Customer
  - "The technician was kind, responsive, respectful, and educational. Highly recommend." — Verified Customer
Overall rating: 4.5 stars from 367 reviews on Yelp. Add a "Read all 367 reviews on Yelp" button linking to https://www.yelp.com/biz/phoenix-appliance-services-phoenix-3.

## Page layout (single page, sticky nav, smooth scroll)
1. Hero — business name, a strong tagline, and two buttons: "Get a Free Quote" and "Call (623) 292-7152".
2. Services — cards showing the items and prices above.
3. Gallery — 8 tasteful images fitting a appliance repair experts, with a click-to-enlarge lightbox.
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
- Brand feel: trustworthy and professional — navy blue with white.
- Serif headings, clean sans-serif body. Fully mobile-responsive. A floating "Get a Free Quote" button on mobile. Subtle, tasteful scroll animations. Fast and accessible.

## SEO
- Proper page title and meta description, Open Graph tags, and LocalBusiness JSON-LD structured data with the name, address, phone, hours, and 4.5 rating.

Build the complete site now — the full single-page layout and the online booking system first, then the admin dashboard.
