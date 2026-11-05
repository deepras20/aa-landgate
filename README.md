# A&A Landgate Website

Premium real estate consultancy website for A&A Landgate, Maharashtra.

## Tech Stack
- Pure HTML5 / CSS3 / vanilla JavaScript (single-file SPA)
- Chart.js 4.4.1 (property price trends)
- Google Fonts: Cinzel, Cormorant Garamond, Inter

## Pages
- **Home** — Hero, Why Us, Services, Tech (price chart), Testimonials
- **Listings** — Property listing cards with filter by type (1BHK–4BHK, Commercial, Plot)
- **About Us** — Mission, Vision, Team
- **Sell Property** — Sellers' landing page with enquiry form
- **Blog** — 6 SEO-optimised articles with weekly additions
- **FAQ** — Accordion FAQ
- **Contact Us** — Lead capture form

## Deployment
Hosted on Hostinger. GitHub Actions auto-deploys `index.html` to `public_html/` on push to `main`.

## Adding Property Listings
To add or update a property listing, edit `index.html` — look for the `<!-- LISTINGS PAGE -->` section. Each listing card uses `data-type="1bhk|2bhk|3bhk|4bhk|commercial|plot"` for the filter to work.

**To replace placeholder images:** swap the SVG in `.listing-media-placeholder` with an `<img>` tag pointing to your image URL.

## Weekly Blog
Blog articles are added every Sunday automatically via a Claude scheduled task.

## SEO
- Full meta tags (og, twitter, schema.org RealEstateAgent JSON-LD)
- Dynamic title + description per page (SPA routing)
- Primary keywords: real estate Mumbai, property Thane, flats Navi Mumbai, RERA registered broker Maharashtra
