# Professional Personal Portfolio Website for Students & Developers

An ultra-modern, responsive, high-performance Personal Portfolio Website built with **React 19**, **JavaScript (ES6+)**, **HTML5**, and **Vanilla CSS3**. Specially crafted for college students, freshers, and professional software engineering candidates looking to showcase their projects, technical skills, education, verified certifications, interactive resume, and leadership experience for internship and job placement interviews.

---

## 🌟 Key Features

1. **Stunning Modern Design & Aesthetics**
   - Deep navy / midnight slate background with electric blue & violet gradients.
   - Glassmorphic card backdrops (`backdrop-filter: blur(16px)`).
   - Dynamic rotating specializations tagline in the Hero section.
   - Framed profile avatar with glowing animated gradient rings.
   - Responsive cross-device layout (Mobile, Tablet, Laptop, Ultra-wide).

2. **Dark Mode & Light Mode**
   - Seamless instant theme switching using CSS custom variables.
   - Theme preference persisted in `localStorage` and respects system preferences.

3. **Global Command Palette (Quick Search)**
   - Press <kbd>Ctrl</kbd> + <kbd>K</kbd> (or <kbd>Cmd</kbd> + <kbd>K</kbd>) or click the search bar in the navbar.
   - Instant search across projects, technical skills, documents, and navigation sections with keyboard arrow navigation.

4. **Projects Catalog & Details Modal**
   - Search by project title, keyword, or technologies.
   - Category filtering (All, Full-Stack, Frontend).
   - Problem statement & solution architecture breakdown.
   - Interactive Quick View modal and dedicated `/projects/:id` specification pages.
   - Real working links to source code, live demonstrations, and downloadable capstone reports.

5. **Skills & Proficiency Cards**
   - Categorized under **Programming Languages**, **Frontend Development**, **Tools & DevOps**, and **Soft Skills**.
   - Searchable skills index with proficiency meters, experience duration, and verified tags.

6. **Education & Experience Timeline**
   - Clean dual-track timeline highlighting academic degrees, GPA, and relevant coursework.
   - Quantifiable internship experience bullets and tech club leadership.

7. **Certifications & Achievements Gallery**
   - Official credentials from AWS, Meta, and the University of Michigan.
   - Real, authentic PDF certificates located in `public/assets/certificates/` that can be downloaded or previewed directly.
   - Credential ID verification badges.

8. **Interactive ATS-Friendly Resume Hub**
   - Clean in-browser paper resume formatted for modern ATS parsers.
   - One-click **Download Resume PDF** button.
   - **Open in New Tab** direct link.
   - **Print Resume** functionality with dedicated `@media print` styling that hides navigation and formats for letter paper.
   - Downloadable cover letters and capstone technical reports.

9. **Extracurricular Activities & Leadership**
   - Collegiate hackathon victories, Google Developer Student Club community leadership, competitive coding awards, and STEM volunteer initiatives.

10. **Interactive Contact Form with Demo Simulation**
    - Real-time client-side input validation with accessible error alerts.
    - Simulates message delivery with loading states and celebration confetti.
    - Saves recent test messages to browser `localStorage` for evaluator review.
    - 1-click **Copy Email** button with clipboard feedback.

11. **Demonstration Authentication (Login & Signup)**
    - Client-side demo auth flow with React state and `localStorage`.
    - Real-time password strength meter (Fair, Good, Strong) and security criteria checklist.
    - Show/hide password visibility toggle.
    - **1-Click Quick Demo Sign In** buttons for recruiters and evaluators.

---

## 🛠️ Technology Stack

- **Framework**: [React 19](https://react.dev/)
- **Bundler & Dev Server**: [Vite 8](https://vitejs.dev/)
- **Routing**: [React Router DOM (HashRouter)](https://reactrouter.com/) for reliable deep links and static host compatibility.
- **Styling**: Pure **Vanilla CSS3** with design tokens, CSS variables, and zero heavy CSS frameworks.
- **Icons**: [Lucide React](https://lucide.dev/) & custom SVG brand icons.
- **Micro-Interactions**: [canvas-confetti](https://www.npmjs.com/package/canvas-confetti) for celebratory feedback.
- **Data Store**: Centralized `src/data/portfolioData.js` data module.

---

## 🚀 Running the Project Locally

### 1. Prerequisites
- **Node.js**: v18.0.0 or higher (v25+ supported)
- **NPM**: v9.0.0 or higher

### 2. Install Dependencies
```bash
npm install
```

### 3. Start Development Server
```bash
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) in your browser.

### 4. Build for Production
```bash
npm run build
```
The optimized bundle will be generated in the `dist/` directory.

### 5. Preview Production Build
```bash
npm run preview
```

---

## 📁 Project Structure

```text
My Portfolio Website/
├── public/
│   ├── assets/
│   │   ├── documents/
│   │   │   ├── Resume_Alex_Morgan.pdf
│   │   │   ├── Cover_Letter_Alex_Morgan.pdf
│   │   │   └── Project_Report_AI_Study_Companion.pdf
│   │   ├── certificates/
│   │   │   ├── AWS_Cloud_Practitioner.pdf
│   │   │   ├── Meta_Frontend_Developer.pdf
│   │   │   └── Python_Data_Structures.pdf
│   │   └── images/
│   │       ├── avatar.svg
│   │       ├── project-devpulse.svg
│   │       ├── project-educonnect.svg
│   │       ├── project-algoviz.svg
│   │       ├── project-cloudmetrics.svg
│   │       ├── cert-aws.svg
│   │       ├── cert-meta.svg
│   │       └── cert-python.svg
│   └── favicon.svg
├── scripts/
│   ├── generate-assets.js    # Generates valid PDF documents
│   └── generate-images.js    # Generates SVG visual mockups
├── src/
│   ├── components/
│   │   ├── Navbar.jsx           # Sticky nav with search trigger & mobile drawer
│   │   ├── Footer.jsx           # Footer with social links & live status
│   │   ├── ThemeToggle.jsx      # Dark / Light mode switcher
│   │   ├── CommandPalette.jsx   # Global search (Cmd+K / Ctrl+K)
│   │   ├── BackToTop.jsx        # Circular progress scroll-to-top button
│   │   ├── BrandIcons.jsx       # SVG icons for GitHub, LinkedIn, Twitter
│   │   ├── ProjectModal.jsx     # Full project details modal
│   │   └── CertificateModal.jsx # Certificate view & download modal
│   ├── context/
│   │   ├── ThemeContext.jsx     # Dark/Light theme state
│   │   ├── AuthContext.jsx      # Demo auth & evaluator login
│   │   └── ToastContext.jsx     # Floating notifications
│   ├── data/
│   │   └── portfolioData.js     # Single source of truth for student profile
│   ├── pages/
│   │   ├── HomePage.jsx         # Hero, metrics, featured projects, teaser
│   │   ├── AboutPage.jsx        # Story, career goals, roadmap, quick facts
│   │   ├── SkillsPage.jsx       # Categorized skills & filter controls
│   │   ├── ProjectsPage.jsx     # Searchable catalog with quick view
│   │   ├── ProjectDetailPage.jsx# Dedicated project specs & architecture
│   │   ├── EducationPage.jsx    # Dual timeline for studies & internships
│   │   ├── CertificationsPage.jsx# Official certificates gallery
│   │   ├── ResumePage.jsx       # In-browser ATS paper resume & PDF downloads
│   │   ├── ActivitiesPage.jsx   # Extracurricular & leadership honors
│   │   ├── ContactPage.jsx      # Interactive validated contact form
│   │   ├── LoginPage.jsx        # Demo login with 1-click evaluator access
│   │   ├── SignupPage.jsx       # Demo signup with password strength meter
│   │   └── NotFoundPage.jsx     # 404 error page
│   ├── App.jsx                  # React Router configuration
│   ├── App.css                  # Component styling & media queries
│   ├── index.css                # Design system & CSS custom properties
│   └── main.jsx                 # Application entry point
├── index.html                   # SEO tags, OpenGraph metadata & fonts
├── package.json
└── vite.config.js
```

---

## ✏️ How to Customize for Any Student

All data is separated cleanly from the presentation layer. To customize this portfolio with your own personal details:

1. Open [`src/data/portfolioData.js`](src/data/portfolioData.js).
2. Edit:
   - `personalInfo`: Replace `fullName`, `headline`, `email`, `phone`, `location`, `github`, and `linkedin`.
   - `about`: Update your story, academic goals, and quick facts.
   - `skills`: Add or remove skills and set your own proficiency levels.
   - `projects`: Add your own projects with descriptions, screenshots, and live demo links.
   - `education` & `experience`: Add your university, high school, internships, or student clubs.
   - `certifications`: Update your credential IDs and certificates.
3. Replace the PDF documents in `public/assets/documents/` and `public/assets/certificates/` with your own PDF files.

---

## 🌐 Deployment Instructions

### Deploy to Vercel
1. Install the Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the project root directory.
3. Accept the default build settings (`npm run build` and output folder `dist`).

### Deploy to Netlify
1. Connect your repository to [Netlify](https://www.netlify.com/).
2. Set Build Command: `npm run build`
3. Set Publish Directory: `dist`

### Deploy to GitHub Pages
1. Build the production files: `npm run build`
2. Push the `dist` folder to your `gh-pages` branch. Because this project uses `HashRouter`, all sub-routes work immediately without server-side rewrite configuration.

---

## 📜 License
MIT License. Free to use and customize for student portfolios, internship applications, and personal web projects.
