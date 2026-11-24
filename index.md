---
title: Kouture theme documentation
---

Kouture is a Shopify theme for independent fashion designers and artisan labels: brands that sell a small catalog and want every piece to carry its maker, its material and its making. It has three presets, Kouture, Zari and Khadi.

## 1. Getting started

1. Add the theme from the Shopify Theme Store and pick a preset:
   - **Kouture**: quiet luxury and tailoring. Ivory and ink, Cormorant headings, centered logo.
   - **Zari**: bridal and festive handloom. Emerald, gold and ruby, Playfair Display headings, logo on the left, framed product cards.
   - **Khadi**: everyday natural fiber. Linen tones, Lora and Work Sans, sentence case buttons, rounded corners.
2. In **Online Store, Themes, Customize**, open **Theme settings** to set your logo, colors, fonts and style.
3. Create the menus `main-menu` (header) and `footer` in **Content, Menus**. Menu items with a second level open a dropdown; items with a third level open a full-width mega menu.
4. Optional: add the custom data in section 4 to show makers, provenance and lead times.

## 2. Theme settings

| Group | What it controls |
|---|---|
| Logo and favicon | Logo image and desktop width, favicon |
| Colors | Four color schemes. Each has background, surface, text, muted text, dividers, accent (primary button), primary button text, focus ring, error and success colors |
| Typography | Heading and body fonts, heading size |
| Style | Style family (Classic, Framed or Relaxed), corner radius, hover and transition effects |
| Layout | Page width |
| Product cards | Image ratio, second image on hover, vendor, color swatches, lead time |
| Cart | Drawer or page, order note |
| Search | Search suggestions |
| Currency | Currency codes |
| Social media | Links shown as icons in the footer |

**Style family** changes character without changing your content:

- Classic: centered logo with the menu below, open product cards, uppercase buttons.
- Framed: logo on the left with the menu beside it, product cards in a thin frame, uppercase buttons.
- Relaxed: logo on the left, open cards, sentence case buttons.

**Accessibility of colors.** Keep text and muted text at a contrast of at least 4.5:1 against the background of the same scheme. The focus ring color must stand out from the background (3:1 or more). The preset schemes already meet these levels.

## 3. Sections

### Header and footer
- **Announcement bar**: one or more messages that rotate, with a pause button. Rotation is off for visitors who prefer reduced motion.
- **Header**: menu, mega menu image (from the collection a menu item links to), customer account menu, sticky header, color scheme. The account icon is Shopify's account component and appears on desktop and mobile.
- **Footer**: text, menu and newsletter blocks; social icons, Follow on Shop, country and language selectors, payment icons.

### Home and story sections
| Section | Use it for |
|---|---|
| Hero fade | Up to three full-screen images that cross-fade behind a heading and two buttons. Includes a pause button |
| Featured collection | A grid of product cards from one collection |
| Craft story | A large image beside the story of a technique, with up to four facts |
| Artisan spotlight | A maker's portrait, a quote and up to four of their products |
| Editorial grid | A mosaic of captioned images (square, tall or wide tiles) |
| Newsletter | Email sign-up; subscribers are tagged `newsletter` |
| Rich text | Heading, text and button blocks |
| Custom Liquid | Your own Liquid, HTML or app snippets |
| Apps | App blocks anywhere on a page |

### Product page
The product information section is built from blocks you can reorder: title, price, lead time, provenance passport, variant picker, quantity, buy buttons, restock request, installments, pickup availability, description, collapsible rows, complementary products, text, Custom Liquid and app blocks.

- **Variant picker**: buttons or dropdowns. Color swatches come from the swatch color or image of each option value (set in the product's category metafields).
- **Buy buttons**: dynamic checkout buttons (on by default), purchase options for subscriptions, and the gift card recipient form for gift card products.
- **Restock request**: appears only when the selected variant is sold out. It sends you a contact form email with the product and variant. It does not send automatic alerts.
- **Media**: images, videos, YouTube and Vimeo videos and 3D models, with zoom. Selecting a variant shows its image first.
- Below the product: **Provenance** (the maker and authenticity note), **Fabric close-up** (an image with numbered details) and **Related products**.

### Collection, search and cart
- **Collection banner** and **Product grid**: filters (from the Search and Discovery app), sort, removable filter chips, pagination and an option to show every Nth product wide.
- **Search results**: tabs for all results, products, journal articles and pages; product filters.
- **Cart**: drawer or page, order note, discounts, unit prices, subscriptions, dynamic checkout buttons.

### Maker, lookbook and journal pages
| Page template | Sections |
|---|---|
| `page.artisan` | Artisan hero, Making timeline, Pull quote, Artisan products |
| `page.makers` | Makers grid (every artisan entry) |
| `page.lookbook` | Lookbook intro, Lookbook scenes with product pins (layouts: image left, image right, full width) |
| `page.contact` | Page content and Contact form |
| Blog | Journal posts with a featured article and topic filters |
| Article | Article with "Made with" products, previous and next links and comments |

## 4. Custom data (optional)

Everything is optional; each section falls back to its own settings. Create these in **Settings, Custom data** with the namespace `custom`.

**Product metafields**: `weave`, `origin`, `fabric` (single line text), `care`, `authenticity_note` (multi-line text), `lead_time_text` (single line text, for example "Made to order, ships in 4 weeks"), `artisan` (metaobject reference to Artisan).

**Artisan metaobject** (type `artisan`): `name`, `portrait` (image), `craft`, `location`, `bio` (rich text), `quote`, `process_steps` (list of Process step entries), `collection` (collection reference), `products` (product list).

**Process step metaobject** (type `process_step`): `title`, `text`, `duration`, `image`.

**Page metafield**: `custom.artisan` (Artisan reference). Assign the `page.artisan` template to a page and set this metafield; the page then fills itself from the entry.

**Article metafield**: `custom.products` (product list) for the "Made with" block.

To link a maker in the Makers grid and Provenance section, give the page the same handle as the artisan entry.

## 5. Customer accounts

Kouture uses Shopify customer accounts through the account component in the header. Order history and profile pages are hosted by Shopify.

## 6. Accessibility and performance

- Every control works with a keyboard, with a visible focus ring in each color scheme.
- Motion (hero fade, announcement rotation, transitions) stops for visitors who prefer reduced motion. The hero and announcement bar have pause buttons.
- Forms have labels and announce errors.
- Images load at the right size, and only the first image on a page loads eagerly.
- JavaScript only enhances the page: menus, filters, cart and product forms work without it.

## 7. Support

Support requests are answered within two business days. The support contact form is linked from the Kouture listing on the Shopify Theme Store.
