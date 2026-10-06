# Błogostan

Premium editorial website for **Błogostan**, a restaurant at Rynek 20 in Gniezno.

## Stack
Next.js App Router, React, TypeScript, responsive CSS, Vercel-ready.

## Run locally
npm install
npm run dev

## Owner panel
Open **/owner**. The panel has three independent areas:
- Gallery: multi-image upload, preview and delete.
- Menu / offer: add, edit and remove items, descriptions, categories, prices and image URLs.
- Full menu card: upload and remove complete menu-page images.

The demo stores content in browser localStorage under `blogostan-site`. This is intentionally a local prototype, not production authentication or shared storage. Uploaded files become browser data URLs.

## Production migration to Supabase
The UI is separated from persistence in `lib/storage.ts`. Replace that adapter with Supabase reads/writes and Supabase Storage uploads. Recommended tables are `gallery_items`, `menu_items` and `menu_photos`. Add Supabase Auth plus Row Level Security for the owner area.

## Content rules
Only supplied business facts are presented as factual data: Błogostan, Rynek 20, 62-200 Gniezno, phone 511 642 643, 40–60 zł per person, 4.9/115 Google rating and the menu names visible in the supplied listing. No opening hours, prices or social profiles were invented.

## SEO
The app includes title/description, Open Graph basics, canonical intent, Restaurant JSON-LD, sitemap and robots. Replace the placeholder production host in app/sitemap.ts and app/robots.ts when the final domain is known.

## Design direction
The visual language is intentionally original: dark moss/ink, warm paper, acid-lime accent, oversized editorial typography, asymmetric grids and restrained motion/hover behavior. It is not a copy of any reference restaurant site.

## Deployment
The repo is standard Next.js and can be imported into Vercel. No custom server is required.