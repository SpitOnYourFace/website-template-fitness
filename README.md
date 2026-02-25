# FitZone Gym — Website Template

A professional, mobile-responsive fitness gym website template built with vanilla HTML, CSS, and JavaScript. All text is in Bulgarian.

## Features

- **Single-page layout** with 5 sections: Hero, Memberships, Classes, Trainers, Contact
- **Dark energetic theme** with red accent (#e94560)
- **Fully responsive** — desktop, tablet, mobile with hamburger menu
- **Scroll animations** via IntersectionObserver (no dependencies)
- **Sticky header** with blur backdrop on scroll
- **Diagonal section dividers** for dynamic visual flow
- **Grain texture overlay** for raw gym aesthetic
- **Zero dependencies** — pure HTML/CSS/JS

## Quick Start

Open `index.html` in your browser. That's it — no build step required.

```bash
# Or use a local server
npx serve .
```

## Customization

### Gym Name & Text

All text is in `index.html`. Search and replace:

| Find               | Replace with          |
| ------------------- | --------------------- |
| `FitZone`           | Your gym name         |
| `FitZone Gym`       | Your full gym name    |
| `бул. Витоша 120`   | Your address          |
| `+359 2 888 1234`   | Your phone number     |
| `+359 888 123 456`  | Your mobile number    |

### Colors

Edit CSS variables at the top of `style.css`:

```css
:root {
  --bg-primary: #1a1a2e;    /* Main background */
  --bg-secondary: #16213e;  /* Section backgrounds */
  --bg-card: #0f3460;       /* Card backgrounds */
  --accent: #e94560;        /* Red accent color */
  --accent-glow: rgba(233, 69, 96, 0.4);
  --accent-hover: #ff6b81;  /* Accent hover state */
  --text-primary: #f0f0f0;  /* Headings */
  --text-secondary: #a0a0b8; /* Body text */
}
```

### Fonts

The template uses Google Fonts loaded in `index.html`:

- **Headings:** Bebas Neue
- **Body:** Open Sans

To change fonts, update the `<link>` tag in `index.html` and the CSS variables:

```css
--font-heading: 'Your Heading Font', sans-serif;
--font-body: 'Your Body Font', sans-serif;
```

### Pricing

Edit the pricing cards in the Memberships section of `index.html`. Each card follows this structure:

```html
<div class="pricing-card">
  <div class="pricing-card__header">
    <span class="pricing-card__tier">Plan Name</span>
    <div class="pricing-card__price">
      <span class="pricing-card__amount">39</span>
      <div class="pricing-card__currency">
        <span>лв</span>
        <span>/мес</span>
      </div>
    </div>
  </div>
  <ul class="pricing-card__features">
    <li><!-- feature items --></li>
  </ul>
</div>
```

Add `pricing-card--featured` class to highlight a plan.

### Schedule

The schedule grid is in the Classes section. Each row represents a class. On mobile, card-based layout is shown instead — update both the grid and the `.classes-cards` section to keep them in sync.

### Trainers

Replace the SVG placeholders in trainer cards with actual images:

```html
<div class="trainer-card__avatar">
  <img src="images/trainer-name.jpg" alt="Trainer Name" />
</div>
```

### Social Links

Update the `href` attributes in the footer social icons to point to your actual Instagram and Facebook pages.

## Deployment on Vercel

### Option 1: Vercel CLI

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy from the project directory
vercel

# For production deployment
vercel --prod
```

### Option 2: GitHub + Vercel Dashboard

1. Push this project to a GitHub repository
2. Go to [vercel.com](https://vercel.com) and sign in
3. Click **"Add New Project"**
4. Import your GitHub repository
5. Framework Preset: **Other** (no framework needed)
6. Click **Deploy**

Every push to `main` will auto-deploy.

### Option 3: Drag & Drop

1. Go to [vercel.com/new](https://vercel.com/new)
2. Drag the project folder onto the page
3. Done

### Custom Domain

After deployment, go to your project's **Settings > Domains** in the Vercel dashboard and add your custom domain.

## File Structure

```
├── index.html    # Complete single-page site
├── style.css     # All styles with CSS variables
└── README.md     # This file
```

## Browser Support

Tested on modern browsers (last 2 versions):
- Chrome / Edge
- Firefox
- Safari
- Mobile Safari / Chrome

## License

Free to use for personal and commercial projects. Attribution appreciated but not required.
