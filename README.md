# The Plane Street Coffee House & Cafe — Spec Site

Unsolicited demo site for The Plane Street Coffee House & Cafe, a family-operated coffee house and cafe in Bethel, Ohio (Clermont County). Built as part of Kyle's spec-site lead-gen pipeline — this is the first coffee shop in the pipeline (everything prior was trades, pet-care, or auto).

## Confirmed facts (safe to state on the call)
- Address: 125 W Plane St, Bethel, OH 45106
- Phone: (513) 734-0079 — confirmed directly from their own Square Online listing (resolves the earlier conflicting (513) 310-1258 seen on a BBB category scrape; 734-0079 is correct)
- Email: planestreetcoffee@gmail.com — from their own Square listing
- Family-operated; described as a community gathering place
- Hours, from their own Square listing (overrides the extended evening hours shown on third-party sites like Yelp, which were wrong): Mon–Fri 6:00am–4:00pm, Sat–Sun 8:00am–4:00pm
- Real named menu items with prices, pulled directly from their Square Online menu: The Coffee House Egg & Cheese ($4.99), The Union Street Croissant ($5.99), The BELT ($5.99), The Plane Street Panini ($5.99), Monte Cristo ($8.50), The Ryan's Sandwich ($6.99, "Built by Ryan — loved by everyone!"), Wheatberry Toast @ PS ($4.00); lunch: The Burke, The Clucker, The Eleanor, The Five & Dime Ham & Cheese Panini, The BT BLT, The Ham and Jam, Gliers Goetta Grilled Cheese, The Abbie, Soup and Salad Combo; sweets: Scone, Gourmet Muffin, Mimi's Cheesecake, Affogato, Cake Pop, Lemon Bar, Chocolate Croissant, Pumpkin Roll
- Facebook page has 3,746 likes — real, verified social proof
- Two Instagram accounts found: @planestreetcoffee and @planestreetcoffeehouse (unclear which is current/primary — worth asking)

## Correction (2026-09-12) — the original "hook" below was wrong
The first pass of this README claimed their Square Online link (`plane-street-coffeehouse-and-cafe.square.site`) was an abandoned, unconfigured empty shell, based on a `curl` fetch that only caught the page's pre-JavaScript loading scaffold (empty `<title>`, no content) before the SPA rendered. **That was a verification mistake, not a fact** — the SEO title genuinely is empty, but the actual site is a full, real, actively-maintained online menu with real prices, item photos, "Out of stock" flags being kept current, and the real hours/phone/email above. Kyle found the live link through their Facebook page, which is what surfaced the mistake. Confirmed by actually loading the page in a browser and reading its rendered content — not by curl alone. **Lesson: JS-rendered storefronts (Square, Wix, Squarespace) will falsely look empty/abandoned via curl or a raw HTTP fetch; always render in an actual browser before concluding a page is broken or dead.**

## The corrected hook for the call
Don't say "your website is broken" — it isn't, and saying so would undercut the pitch immediately. The real gap: they've clearly put real effort into a detailed Square Online ordering menu (accurate prices, photos, keeping stock status current), but there's no actual *website* — nothing that tells their story, shows the actual space, explains what makes them Bethel's gathering spot, or gives people a reason to visit beyond "here's a menu." The pitch is "you've built a great order form — let's build the home page that should sit in front of it," not "you have no online presence."

## Not yet confirmed
- Owner name
- Founding year
- Real logo — no matching image file found in Downloads/Desktop, so `assets/logo.svg` is a hand-built paper-airplane + coffee-cup mark (a visual pun on "Plane Street") rather than a recreation of a real logo
- Whether they take catering/large group orders (assumed yes, worth confirming)
- Whether the bar/alcohol categories visible in the Square menu's navigation (cocktails, craft beer, wine, spirits) are real current offerings or leftover unused categories from a template — none had visible items, so they're intentionally left off this site

## Build notes
- Palette: terracotta/rust (`--rust #c1502e`) + espresso brown (`--espresso #3b2820`) + warm cream (`--cream #f7ede1`), chosen to be distinct from every other sibling site and to fit a cozy small-town coffeehouse feel.
- Typography: Lora (serif, headings) + Nunito Sans (body) — first sibling site to use this pairing.
- Hero background includes a dashed "flight path" SVG arc with a paper-airplane arrowhead, a literal nod to "Plane Street."
- Menu section uses 4 numbered cards (Coffee & Espresso, Breakfast, Lunch, Sweets) instead of the usual trade "services" rows, now naming real signature items instead of generic categories.
- Contact form posts to Formspree with a `YOUR_FORM_ID` placeholder — needs a real form ID before it'll send.
- Local preview: `python3 -m http.server 8968 --directory plane-street-coffee-house-cafe` (registered in `.claude/launch.json`).

## Pricing to pitch (standard, per the pipeline)
- Option A: $750 one-time build, they own it and handle hosting/updates.
- Option B (recommended): $250 upfront + $45/month care plan — Kyle keeps hosting, domain, content updates.
- Domain registration ~$12–15/yr passed through at cost if they don't already have one.

## Not yet done
- Not git-initialized or pushed to GitHub yet — do that when asked to publish, per the pipeline convention (`gh repo create SMCtippa/plane-street-coffee-house-cafe --public --source=. --remote=origin --push`, then enable GitHub Pages).
- No call script built yet.
