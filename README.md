# SkillShala — Education & Course Website Template

A bright, responsive multi-page online course platform starter built with React, Vite and Tailwind CSS. SkillShala is fictional; authentication, enrolment and contact submission are UI demonstrations and are not connected to a backend or payment provider.

## Features
- Responsive home page with hero search, categories, popular courses, learning steps, reviews and pricing CTA
- Course catalogue with search, category, level and price filters, sorting and pagination
- Course detail pages with calculated curriculum duration, outcomes, instructor details, accordion curriculum and YouTube preview modal
- Desktop sticky enrol card and mobile bottom enrol bar
- Instructor directory and individual profiles
- Monthly/yearly pricing toggle, About, Contact, Login, Sign Up and 404 pages
- Reusable components, accessible labels, visible focus states and page-specific title/description
- Original lightweight SVG course illustrations (no stock image assets or external image credits required)

## Pages
`/` Home · `/courses` Catalogue · `/courses/:slug` Course detail · `/instructors` Directory · `/instructors/:slug` Profile · `/plans` Plans · `/about` About · `/contact` Contact · `/login` Login · `/signup` Sign Up · `*` 404

## Tech stack
- React 19, Vite 7, JavaScript
- React Router 7
- Tailwind CSS 4 with the official Vite plugin
- lucide-react, framer-motion
- Google Fonts: Outfit

## Quick start
Install Node.js (LTS), open this folder in VS Code, then run:

```bash
npm install
npm run dev
```

Open the local URL printed by Vite (usually http://localhost:5173). For a production build:

```bash
npm run build
npm run preview
```

On Windows PowerShell with script execution restricted, use `npm.cmd install` and `npm.cmd run dev`.

## Customization guide
- **Brand name, tagline and contact:** edit `src/data/site.js`.
- **Courses, curriculum, lesson durations, prices and instructors:** edit `src/data/courses.js`. Total duration is calculated from lesson durations automatically.
- **Categories, levels and plans:** edit `src/data/site.js`.
- **Colours and typography:** edit the `@theme` block in `src/index.css`; Outfit is loaded from Google Fonts in `index.html`.
- **Logo/favicon:** replace `public/favicon.svg` and update the brand mark in `src/components/layout/Navbar.jsx`.
- **Navigation and footer:** edit `src/components/layout/Navbar.jsx` and `Footer.jsx`.

## Deploy
Build command: `npm run build`  
Publish directory: `dist`  
Netlify SPA redirects are included in `public/_redirects`. Vercel can use the same build command and `dist` output directory.

## GitHub
Create a public repository named `msg-skillshala-course-template`, commit these files (do not upload `node_modules` or `dist`), then use:
`https://github.com/<your-username>/msg-skillshala-course-template/archive/refs/heads/main.zip`

## Image credits
Course thumbnails are original inline SVG illustrations created for this template. No third-party stock images are bundled.

## FAQ
**How do I add a course and its lessons?**  
Add a course object to `src/data/courses.js`. Include a unique `slug`, title, category, level, price, instructor, and a `curriculum` array. Each lesson needs a `duration` in `MM:SS` format. Total course duration is calculated automatically.

**Can I connect real payments?**  
Yes. Connect a secure backend and a payment provider such as Stripe or Razorpay. The current enrol buttons are UI-only and do not collect payments.

**How do I change the categories?**  
Edit the `categories` array in `src/data/site.js`. Use matching category names in course objects in `src/data/courses.js`.

**Does login work with real accounts?**  
No. Login and Sign Up are frontend demonstrations. Add authentication and secure server-side session handling before production use.

## License
Use and adapt this template for personal or commercial projects. Replace demo content and configure your own services before production deployment.
