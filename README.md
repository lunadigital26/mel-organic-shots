# Mel Organic Shots — website

Client: **Melissa ("Mel")**, organic cold-pressed juice shots, Methuen, MA. Built by **Luna Digital**.
Live preview: https://lunadigital26.github.io/mel-organic-shots/ (GitHub Pages, branch `main`, root).

## Status (Nov 2026)
Preview site done and sent to the client for review. Not on her own domain yet. Checkout is a demo.

## What's in `index.html` (single file, no build step)
- **Data** at the top of the main script: `SHOTS` (15 flavors: name, color, tint, ingredients, perks, goals), `BUNDLES`, `BENEFITS`, `GOALS`, `FEATURED`, and the ingredient illustrations `ING` / `BEN_ING`. Change prices or flavors here and every section updates.
- **Look:** "Garden Fresh" palette: deep green header and footer, leaf-green Meet Mel section, mint bundles, orange only for buttons, cart and logo. Each flavor keeps its own color. Fonts: Bricolage Grotesque, Figtree, Caveat.
- **Sections:** announcement bar, hero flavor switcher, shot menu with goal filters, benefits tabs with jumping ingredients, bundles plus build-your-own crate, Meet Mel, ordering steps, reviews (placeholders), FAQ, call to action, footer.
- **3D bottles:** Three.js r128 from cdnjs. One WebGL canvas draws a glass bottle into every `.b3d` element. Labels with the logo are drawn from `SHOTS`. Falls back to SVG bottles if WebGL isn't available.
- **Chef Mel:** an illustrated SVG character, bottom-left. She talks about any bottle that's clicked, cheers on add-to-cart, introduces sections, follows the cursor and leans while scrolling. She can be minimized.
- **Cart:** saved in localStorage. Pickup or delivery, free delivery over $40, demo confirmation.
- **Logo:** `logo.svg` (orange drop with a leaf, "Mel" in script).

## Still to do
- Real photo of Mel, her real prices, and 2–3 genuine customer reviews (current ones are placeholders).
- Confirm with Melissa that Chef Mel's look matches her, or turn the character into a separate mascot.
- Real ordering: a Google Sheets order log (free, recommended first), then Square or WooCommerce on Hostinger.
- Her own domain (e.g. melorganicshots.com) on Hostinger, then Google Search Console.

## Editing tips
- Edit `index.html` and push to `main`. Pages redeploys in about a minute.
- The ingredient code (`ING`, `BEN_ING`, `ingStage`) must stay inside the `<script>`, right after the `/* benefits */` comment in the script. There's also a `/* benefits */` comment in the CSS, so don't confuse the two.
