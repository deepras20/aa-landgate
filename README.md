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

**Categories & property codes:** the Listings page has two tabs — **New Projects** (`#cat-new`, codes `AAL-NP-###`; each project is one entry in the `NEW_PROJECTS` array in `index.html`, which builds its tile on the Listings page and its full detail page at `/#project/<CODE>`) and **Resale** (`#cat-resale`, `.listing-card`, codes `AAL-RS-###`). Update the tab counts when adding a listing. Media for each listing lives in `assets/listings/<CODE>/` and is shown in a 9:16 reel frame (photos 1080×1920, videos vertical 9:16). Every **Enquire Now** button calls `openEnquiry('<CODE>','<Property name>')`, which opens the form (code, name, contact number, email) and sends it to WhatsApp 9653236410 (and to the Google Sheet once `LEAD_ENDPOINT` is set).

## Weekly Blog
Blog articles are added every Sunday automatically via a Claude scheduled task.

## SEO
- Full meta tags (og, twitter, schema.org RealEstateAgent JSON-LD)
- Dynamic title + description per page (SPA routing)
- Primary keywords: real estate Mumbai, property Thane, flats Navi Mumbai, RERA registered broker Maharashtra
