# Shining-Light Investments CC — Website

## Project Structure

```
shining-light/
├── index.html          ← Main website (single file, no build step needed)
├── assets/
│   ├── logo.png        ← Place your company logo here
│   └── gallery/        ← Place all product/service photos here
│       ├── catering-1.jpg
│       ├── cleaning-1.jpg
│       ├── tailoring-1.jpg
│       ├── eartags-1.jpg
│       ├── marula-1.jpg
│       ├── marula-bottle.jpg
│       └── photo-1.jpg ... photo-8.jpg   (gallery section)
└── README.md
```

## Quick Start

1. **Open `index.html`** directly in a browser — no server needed for basic viewing.
2. For local development with a dev server: `npx serve .` or `python3 -m http.server 8080`

## Adding Your Logo

Place your logo file at `./assets/logo.png`. It will appear in:
- The navbar (top left)
- The hero section (right side, floating)

Recommended: PNG with transparent background, minimum 400×400px.

## Adding Gallery Photos

All placeholder slots have HTML comments like:
```html
<!-- REPLACE: <img src="./assets/gallery/catering-1.jpg" ...> -->
```

Simply uncomment the `<img>` tag and delete the placeholder `<div>` above it.

### Service Card Photos (in #services section)
| Slot | Recommended file | Size |
|------|-----------------|------|
| Catering | `./assets/gallery/catering-1.jpg` | Any, cropped to 16:9 |
| Cleaning | `./assets/gallery/cleaning-1.jpg` | Any, cropped to 16:9 |
| Tailoring | `./assets/gallery/tailoring-1.jpg` | Any, cropped to 16:9 |
| Animal Ear Tags | `./assets/gallery/eartags-1.jpg` | Any, cropped to 16:9 |
| Marula Oil | `./assets/gallery/marula-1.jpg` | Any, cropped to 16:9 |

### Gallery Section (Photo 1–8)
| Slot | Recommended file |
|------|-----------------|
| 01 (large feature) | Your best/most impressive photo |
| 02–08 | Mix of products, events, team work |

### Marula Oil Spotlight
Replace the placeholder with: `./assets/gallery/marula-bottle.jpg`

## Contact Form

The form currently uses a `mailto:` link (opens the user's email client).

For a proper form backend, replace the `handleSubmit()` function in index.html with:
- **Formspree** (free): https://formspree.io
- **EmailJS** (free tier): https://www.emailjs.com

## Color Palette (CSS Variables)

```css
--green-deep:   #1a5c2a   /* Primary brand green (from logo) */
--green-mid:    #2d7a3a   /* Mid green */
--green-light:  #4a9e5c   /* Light green accents */
--green-pale:   #e8f5eb   /* Background tints */
--gold:         #f0c419   /* Sunburst gold (from logo) */
--gold-deep:    #c99a00   /* Deep gold for text */
--cream:        #faf8f3   /* Page background */
```

## Fonts Used

- **Playfair Display** — headings (Google Fonts, loaded via CDN)
- **DM Sans** — body text (Google Fonts, loaded via CDN)

Both load automatically. No installation needed.

## Sections

1. **Hero** — Headline, stats, CTA buttons, logo display
2. **Marquee Band** — Scrolling services ticker
3. **About** — Company history, mission, values
4. **Services** — 5 service cards (Catering, Cleaning, Tailoring, Ear Tags, Marula Oil)
5. **Gallery** — 8-slot masonry photo grid
6. **Marula Oil Spotlight** — Dedicated feature section with use cases
7. **References/Clients** — Grid of past clients
8. **Contact** — Contact info + enquiry form
9. **Footer** — Links, company info, registration details

## Deployment

Works with any static host:
- **Netlify**: Drag and drop the `shining-light/` folder
- **Vercel**: `vercel --prod` from the project directory
- **GitHub Pages**: Push to a repo, enable Pages in Settings
- **Any web host**: Upload via FTP/cPanel

No backend required — it's a pure HTML/CSS/JS site.
