# Fluency Education Website

A single-page, mobile-first site built with HTML + Tailwind (CDN) + vanilla JS — no build step required. Three files: `index.html`, `privacy.html`, `terms.html`, plus `logo.png`.

## Before you go live — 15-minute checklist

1. **Contact form email** — the contact and newsletter forms already POST to `https://formsubmit.co/joni@fluencyeducation.ca` via [FormSubmit](https://formsubmit.co), a free service, no account needed. The very first submission will send a confirmation email to that inbox — click the link inside it once, and every submission after that lands directly in your email. If you want a different address, change `joni@fluencyeducation.ca` in the two `action="..."` attributes in `index.html`.

2. **Payments (card + PayPal)** — open `index.html`, find `PAYPAL_CLIENT_ID` near the bottom of the file, and replace `"YOUR_PAYPAL_CLIENT_ID"` with your real Client ID from the [PayPal Developer Dashboard](https://developer.paypal.com/dashboard/applications) (free, takes ~5 minutes). PayPal's checkout button automatically offers both "Pay with PayPal" and "Debit or Credit Card" — you don't need a separate Stripe integration. Until you add the Client ID, the buy buttons fall back to "Order via contact form" so nothing looks broken.

3. **Booking calendar** — sign up for a free [Calendly](https://calendly.com) account, create an "Assessment Call" event type, then follow the comment inside the `#book-assessment` section of `index.html` to swap the placeholder for the live embed code.

4. **Pricing** — the $65/hr private and $25/session group rates are placeholders, clearly labeled "illustrative rate" on the page. Update both figures once you've set real pricing, and remove the "illustrative rate" caption line.

5. **Testimonials & stats** — the testimonial cards are marked "[Sample]" on purpose. Replace with real student quotes (with permission) before publishing — don't leave placeholder quotes live.

6. **Book cover art** — the three study guide cards currently use color placeholders instead of real cover images. Replace the `<div class="aspect-[4/3] bg-gradient...">` blocks with `<img>` tags once you have cover designs.

## Deployment

This is a static site — no server required. Easiest options:

- **Netlify / Vercel**: drag the folder into their dashboard, or connect a GitHub repo. Free tier is enough.
- **GitHub Pages**: push this folder to a repo and enable Pages in settings.
- Point your domain `www.fluencyeducation.ca` at whichever host you choose (each has simple DNS instructions).

## What's included vs. what would need a real backend

Included and working out of the box: responsive layout, navigation, FAQ accordion, scroll animations, contact + newsletter forms (via FormSubmit), PayPal card/PayPal checkout (once you add your Client ID), Privacy/Terms pages, SEO meta tags and schema markup.

Not included (would need a CMS or backend, out of scope for a static site): a blog with a database, user accounts/login, a shopping cart across multiple items, and inventory tracking. If you outgrow the static version, tools like Shopify (for the book store) or a headless CMS like Sanity/Strapi (for a blog) can plug into a redesign later.
