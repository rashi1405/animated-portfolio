# Animated Portfolio

A single-page animated portfolio built with React, Vite, Sass, and Framer Motion. The site showcases a developer/designer profile with scroll-driven parallax sections, a custom cursor, animated navigation, and a contact form powered by EmailJS.

## Features

- **Hero** — Intro section with staggered text animations and a sliding headline
- **Services** — Animated service cards with hover effects
- **Parallax** — Scroll-linked background and text motion between sections
- **Portfolio** — Featured projects with scroll progress bar and parallax image/text
- **Contact** — Animated contact form with SVG path drawing and EmailJS integration
- **Custom cursor** — Mouse-following cursor overlay
- **Sidebar navigation** — Circular clip-path menu with spring animations

## Tech Stack

| Category | Tools |
|----------|-------|
| Framework | React 18 |
| Build tool | Vite 4 |
| Styling | Sass (SCSS) |
| Animation | Framer Motion 10 |
| Email | EmailJS |
| Font | [DM Sans](https://fonts.google.com/specimen/DM+Sans) (Google Fonts) |

## Prerequisites

- [Node.js](https://nodejs.org/) 18+ (20 recommended)
- npm (comes with Node.js)

## Getting Started

```bash
# Clone the repository
git clone <repository-url>
cd animated-portfolio

# Install dependencies
npm install

# Start the development server
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser. Vite will hot-reload as you edit files.

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start the Vite dev server |
| `npm run build` | Build for production (output in `dist/`) |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint on `.js` and `.jsx` files |

## Project Structure

```
animated-portfolio/
├── public/                 # Static assets (images, icons)
├── src/
│   ├── components/
│   │   ├── contact/        # Contact form and info
│   │   ├── cursor/         # Custom mouse cursor
│   │   ├── hero/           # Landing / intro section
│   │   ├── navbar/         # Top bar with social links
│   │   ├── parallax/       # Scroll parallax dividers
│   │   ├── portfolio/      # Featured works showcase
│   │   ├── services/       # Services grid
│   │   └── sidebar/        # Animated slide-out menu
│   ├── App.jsx             # Page layout and section order
│   ├── app.scss            # Global styles
│   └── main.jsx            # React entry point
├── index.html
├── package.json
└── vite.config.js
```

## Customization

### Personal info

Update content in the component files:

- **Name & title** — `src/components/hero/Hero.jsx`
- **Services** — `src/components/services/Services.jsx`
- **Portfolio projects** — `src/components/portfolio/Portfolio.jsx` (`items` array)
- **Contact details** — `src/components/contact/Contact.jsx`
- **Page title** — `index.html`

### Images

Replace files in `public/` or update image paths in the relevant components. Portfolio project images are currently loaded from external URLs (Pexels).

### Contact form (EmailJS)

The contact form uses [EmailJS](https://www.emailjs.com/) to send messages without a backend. To use your own account:

1. Create a free account at [emailjs.com](https://www.emailjs.com/)
2. Add an email service and create a template with `name`, `email`, and `message` fields
3. Replace the credentials in `src/components/contact/Contact.jsx`:

```js
emailjs.sendForm(
  "YOUR_SERVICE_ID",
  "YOUR_TEMPLATE_ID",
  formRef.current,
  "YOUR_PUBLIC_KEY"
);
```

## Deployment

Build the site for production:

```bash
npm run build
```

Deploy the `dist/` folder to any static host (Vercel, Netlify, GitHub Pages, etc.).

## License

This project is private. All rights reserved.
