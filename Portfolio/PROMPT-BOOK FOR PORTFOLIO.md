# Custom Category: Personal Portfolio (Frontend Only)

This category focuses purely on **frontend-only personal portfolio websites** — no backend, no database, no authentication. It focuses on **content, brand identity, design, and deployment** — everything a developer, designer, or creative needs to build a portfolio that gets them hired.

Here is the exact list of documents we will prepare for the **Personal Portfolio** category, organized into our 4 Phases:

### Phase 1: Content & Identity
1. **`CONTENT_INVENTORY.md`** — Audits all content: bio, projects, skills, experience, testimonials, resume, contact, social links.
2. **`BRAND_KIT.md`** — Defines colors, fonts, logo, tone of voice, and personal brand personality.
3. **`PERSONA_POSITIONING.md`** — Defines who you are, what you do, who you serve, and your unique angle.
4. **`PORTFOLIO_PRD.md`** — Product Requirements Document: goals, target audience, sections, MVP scope.
5. **`SITEMAP.md`** — Page structure, navigation flow, and section hierarchy.

### Phase 2: Design Blueprint
6. **`WIREFRAME_SPEC.md`** — Layout of each section (Hero, About, Projects, Contact).
7. **`DESIGN_SYSTEM.md`** — Components, buttons, cards, typography scale, spacing system.
8. **`RESPONSIVE_SPEC.md`** — Breakpoints, mobile-first rules, and layout behavior.
9. **`ANIMATION_SPEC.md`** — Micro-interactions, scroll animations, hover states, page transitions.
10. **`ASSET_CHECKLIST.md`** — Images, icons, fonts, illustrations, screenshots needed.

### Phase 3: Build & Quality
11. **`TECH_STACK.md`** — Framework (React/Next.js/Astro), styling (Tailwind), hosting choice.
12. **`SEO_META.md`** — Meta tags, Open Graph, Twitter cards, sitemap.xml, robots.txt.
13. **`ACCESSIBILITY.md`** — WCAG compliance, contrast, keyboard nav, screen readers.
14. **`PERFORMANCE.md`** — Lighthouse scores, image optimization, lazy loading, bundle size.
15. **`TESTING_CHECKLIST.md`** — Cross-browser, devices, forms, links, broken assets.

### Phase 4: Launch & Maintain
16. **`DEPLOYMENT.md`** — Vercel/Netlify/GitHub Pages, custom domain, SSL, DNS.
17. **`ANALYTICS.md`** — What to track, privacy-friendly tools, conversion goals.
18. **`CASE_STUDY_TEMPLATE.md`** — How to write each project case study consistently.
19. **`CONTENT_UPDATE_GUIDE.md`** — How to add new projects, update resume, refresh content.
20. **`GLOSSARY.md`** — Definitions of portfolio and web terms.

---

## Phase 1: Content & Identity — Prompt Pack

### 1. CONTENT_INVENTORY.md
**Purpose:** To audit every piece of content you have (and need) before designing anything.
```text
You are a personal branding strategist helping a developer/designer build their portfolio website.

I am building a personal portfolio website. Help me create a complete Content Inventory document.

MY BACKGROUND:
[PASTE: Your name, role, years of experience, field]
[PASTE: What you want to showcase]

Create the Content Inventory with these sections:
1. Personal bio (Short 50-word, Medium 150-word, Long 300-word versions)
2. Professional headline (One-liner for hero section)
3. Skills list (Technical, Soft, Tools)
4. Work experience (Role, Company, Duration, Key achievements)
5. Projects (Name, Description, Tech stack, Links, Screenshots needed)
6. Testimonials (Client or colleague quotes)
7. Education and certifications
8. Resume/CV file (PDF link)
9. Contact information (Email, Phone, Location, Availability)
10. Social links (GitHub, LinkedIn, Twitter/X, Dribbble, etc.)
11. Blog or writing samples (If applicable)
12. Awards and recognitions
13. Services offered (If freelancing)
14. Content gaps (What is missing and must be created)
15. Content priority (Must-have vs nice-to-have)

For each section, mark it as:
- ✅ Available (I have this content)
- ⚠️ Needs improvement
- ❌ Missing (Must be created)

Keep the inventory practical and actionable. Do not assume I have professional photos or a designer.
Explain what makes strong portfolio content vs weak content.
```

## NOTE ALWAYS CRETE YOU FULLY TAILORED CONTENT INVENTORY 
---

### 2. BRAND_KIT.md
**Purpose:** To define your visual and verbal identity before touching any design tool.
```text
You are a senior brand designer helping a developer/designer create a personal brand kit for their portfolio website.

MY BACKGROUND:
[PASTE: Your name, role, industry, personality traits]
[PASTE: Any colors, fonts, or styles you already like]

Create a complete Brand Kit with these sections:
1. Brand personality (3-5 adjectives that describe you)
2. Brand voice and tone (How you write: friendly, professional, bold, minimal)
3. Logo (Primary, Secondary, Favicon — description or concept)
4. Color palette (Primary, Secondary, Accent, Background, Text, Success, Error)
   - Include HEX codes and usage rules
   - Ensure WCAG AA contrast compliance
5. Typography (Heading font, Body font, Code font — with fallbacks)
6. Spacing and layout principles
7. Iconography style (Outline, Filled, Rounded, Sharp)
8. Imagery style (Photography, Illustration, Abstract, Minimal)
9. Button and interaction styles
10. Do's and Don'ts for the brand
11. Brand inspiration references (3-5 websites you admire)

Explain each choice in beginner-friendly language.
Provide 3 color palette options (Light, Dark, Bold) with HEX codes ready to copy.
Recommend free Google Fonts only — no paid fonts.
Keep the brand simple, modern, and achievable for a solo developer.
```

---

### 3. PERSONA_POSITIONING.md
**Purpose:** To define who you are, who you serve, and why someone should hire you.
```text
You are a career positioning coach helping a developer/designer build their personal portfolio.

MY BACKGROUND:
[PASTE: Your name, role, experience, skills, target audience]

Create a Persona and Positioning document with these sections:
1. Who I am (One-paragraph identity statement)
2. What I do (Specific, not vague: "I build X for Y")
3. Who I serve (Target audience: Recruiters, Clients, Collaborators)
4. My niche (Frontend, Full-stack, AI, Design, etc.)
5. My unique angle (What makes me different from 1000 other portfolios?)
6. My value proposition (One sentence: "I help X achieve Y through Z")
7. My proof (Projects, metrics, testimonials that back up the claim)
8. My personality (How I want to come across: Confident, Humble, Bold, Playful)
9. My career goal (Job, Freelance, Personal brand)
10. My elevator pitch (30-second version)
11. Keywords for SEO (What recruiters search for)
12. Anti-positioning (What I am NOT — helps clarity)

Explain why positioning matters.
Give 3 alternative positioning angles to choose from.
Keep it honest and grounded — no overhyped claims.
```

---

### 4. PORTFOLIO_PRD.md
**Purpose:** To define the goals, audience, sections, and MVP scope of the portfolio.
```text
You are a senior product manager helping a developer/designer plan their personal portfolio website.

INPUTS:
Content Inventory: [PASTE CONTENT_INVENTORY]
Brand Kit: [PASTE BRAND_KIT]
Persona & Positioning: [PASTE PERSONA_POSITIONING]

Create a Portfolio PRD with these sections:
1. Site name and tagline
2. One-line description
3. Purpose of the portfolio (Job, Freelance, Personal brand)
4. Target audience
5. Success metrics (Job offers, Inquiries, Interviews, Resume downloads)
6. Core sections (Hero, About, Projects, Skills, Contact)
7. Nice-to-have sections (Blog, Testimonials, Services, Playground)
8. User journeys (Visitor lands → Explores → Contacts)
9. Functional requirements (Contact form, Dark mode, Resume download)
10. Non-functional requirements (Fast load, Mobile-first, Accessible)
11. MVP scope (What must exist at launch?)
12. Out-of-scope (What we skip for v1)
13. Content requirements (What content must be ready?)
14. Design requirements (What design assets must be ready?)
15. Success criteria for v1 launch
16. Future roadmap (v2, v3 ideas)

Keep the MVP realistic for a solo developer.
Do not add unnecessary sections that won't be maintained.
Prioritize a small, polished site over a large, incomplete one.
```

---

### 5. SITEMAP.md
**Purpose:** To define the page structure, navigation flow, and section hierarchy.
```text
You are a UX architect helping a developer/designer structure their portfolio website.

INPUTS:
Portfolio PRD: [PASTE PORTFOLIO_PRD]

Create a Sitemap document with these sections:
1. Site map (Visual hierarchy of pages)
2. Page list (Home, About, Projects, Project Detail, Contact, etc.)
3. Navigation structure (Header nav, Footer nav)
4. Section order on each page (Hero → About → Projects → Contact)
5. Single-page vs Multi-page decision (Justify the choice)
6. URL structure (Clean, SEO-friendly)
7. Internal linking strategy (How pages connect)
8. External links (GitHub, LinkedIn, Resume PDF)
9. 404 page design
10. Mobile navigation pattern (Hamburger, Bottom nav)
11. A text-based flowchart of the user journey

Explain each structural decision.
Keep the structure simple — no more than 5-6 main sections.
Prioritize fast discovery of projects and easy contact.
```

---

## Phase 2: Design Blueprint — Prompt Pack

### 6. WIREFRAME_SPEC.md
**Purpose:** To define the layout of each section before applying visual design.
```text
You are a senior UX designer helping a developer/designer wireframe their portfolio.

INPUTS:
Sitemap: [PASTE SITEMAP]
Brand Kit: [PASTE BRAND_KIT]

Create a Wireframe Specification document with these sections:

For each section (Hero, About, Projects, Skills, Testimonials, Contact, Footer), provide:
1. Purpose of the section
2. Layout (Grid, Columns, Stack)
3. Content blocks (What appears in each block)
4. Hierarchy (What draws attention first, second, third)
5. Call-to-action placement
6. Visual weight (Large hero vs compact footer)
7. Mobile layout (How it stacks)
8. Example ASCII wireframe

Also include:
9. Above-the-fold priorities (What user sees in first 5 seconds)
10. Section transition strategy (How sections flow into each other)
11. Whitespace strategy (Breathing room)
12. A checklist to verify the wireframe covers all content

Keep the wireframes simple and text-based.
Prioritize clarity over decoration.
Do not assume the user has design experience — explain each decision.
```

---

### 7. DESIGN_SYSTEM.md
**Purpose:** To define reusable components, typography scale, and spacing rules.
```text
You are a design systems expert helping a developer/designer build a personal portfolio design system.

INPUTS:
Brand Kit: [PASTE BRAND_KIT]
Wireframes: [PASTE WIREFRAME_SPEC]

Create a Design System document with these sections:
1. Design principles (3-5 guiding rules)
2. Color tokens (Primary, Secondary, Accent, Neutral, Semantic)
   - Light mode and Dark mode variants
3. Typography scale (H1-H6, Body, Caption, Code)
   - Sizes, weights, line-heights for mobile and desktop
4. Spacing scale (4px, 8px, 16px, 24px, 32px, 48px, 64px)
5. Border radius scale (Small, Medium, Large, Full)
6. Shadow scale (Subtle, Medium, Elevated)
7. Components list:
   - Button (Primary, Secondary, Ghost, Icon)
   - Card (Project, Testimonial, Blog)
   - Input (Text, Textarea, Select)
   - Badge / Tag
   - Avatar
   - Nav bar
   - Footer
   - Modal
   - Toast
8. Component states (Default, Hover, Active, Focus, Disabled)
9. Layout grid (12-column, Container widths, Gutters)
10. Iconography rules
11. Usage examples for each component

Provide Tailwind CSS class equivalents for each token where possible.
Keep the system small enough to build in a weekend.
```

---

### 8. RESPONSIVE_SPEC.md
**Purpose:** To define breakpoints and mobile-first rules.
```text
You are a responsive design specialist.
Using the Design System below, create a Responsive Specification document for a personal portfolio.

DESIGN SYSTEM: [PASTE DESIGN_SYSTEM]

Provide:
1. Breakpoint strategy (Mobile, Tablet, Desktop, Large)
   - Recommended pixel values (e.g., 640px, 768px, 1024px, 1280px)
2. Mobile-first approach (Why mobile first?)
3. Grid behavior per breakpoint (Columns: 4 → 8 → 12)
4. Typography scaling (How font sizes change)
5. Spacing scaling (How padding and margin change)
6. Navigation behavior (Hamburger → Full nav)
7. Image behavior (Responsive images, Art direction)
8. Component behavior per breakpoint:
   - Hero section
   - Project grid
   - Contact form
   - Footer
9. Touch target sizes (Minimum 44x44px)
10. Testing checklist across devices

Explain the reasoning behind each breakpoint.
Keep the responsive rules simple and achievable with Tailwind or CSS Grid.
```

---

### 9. ANIMATION_SPEC.md
**Purpose:** To define micro-interactions, scroll animations, and hover states.
```text
You are a motion design expert specializing in web portfolios.

INPUTS:
Design System: [PASTE DESIGN_SYSTEM]
Wireframes: [PASTE WIREFRAME_SPEC]

Create an Animation Specification document with these sections:
1. Animation principles (Purposeful, Subtle, Fast, Accessible)
2. Timing and easing (Duration: 150ms-500ms, Easing: ease-out, ease-in-out)
3. Page load animations (Fade-in, Stagger reveal)
4. Scroll animations (Reveal on scroll, Parallax, Progress bar)
5. Hover animations (Buttons, Cards, Links, Images)
6. Click/tap animations (Button press, Ripple, Scale)
7. Micro-interactions (Form focus, Copy button, Theme toggle)
8. Page transitions (Route changes if multi-page)
9. Loading states (Skeletons, spinners, progress)
10. Reduced motion support (prefers-reduced-motion)
11. Library recommendations (Framer Motion, GSAP, CSS-only)
12. What NOT to animate (Distracting or slow effects)
13. Accessibility considerations (Motion sickness, Vestibular disorders)

For each animation, provide:
- Trigger
- Duration
- Easing
- Property animated
- Purpose

Keep the animations subtle and professional.
A portfolio should feel polished, not like a circus.
Prefer CSS animations over heavy JS libraries where possible.
```

---

### 10. ASSET_CHECKLIST.md
**Purpose:** To list every image, icon, font, and illustration needed before building.
```text
You are a front-end asset manager helping a developer/designer plan their portfolio assets.

INPUTS:
Content Inventory: [PASTE CONTENT_INVENTORY]
Wireframes: [PASTE WIREFRAME_SPEC]
Design System: [PASTE DESIGN_SYSTEM]

Create an Asset Checklist document with these sections:
1. Images needed:
   - Hero image or avatar
   - Project thumbnails (1 per project)
   - Project screenshots (2-4 per project)
   - About section photo
   - Background textures or patterns
2. For each image, specify:
   - Purpose
   - Recommended dimensions
   - Format (WebP, PNG, SVG, AVIF)
   - Alt text requirement
   - Source (Own, Unsplash, Custom)
3. Icons needed (GitHub, LinkedIn, Email, Resume, External link, etc.)
   - Recommended icon library (Lucide, Heroicons, Feather)
4. Fonts needed
   - Heading font, Body font, Code font
   - Free Google Fonts recommendations
5. Logo files (SVG, PNG, Favicon, Apple touch icon)
6. Illustrations (If used)
7. OG image (1200x630 for social sharing)
8. Favicon set (16x16, 32x32, 180x180, 512x512)
9. File naming conventions
10. Folder structure for assets (/public/images, /public/icons)
11. Optimization checklist (Compress, Convert to WebP, Lazy load)
12. Free resource links (Unsplash, Pexels, Undraw, Lucide, Google Fonts)

Explain why each asset matters and how to optimize it.
Keep the checklist practical for a solo developer.
```

---

## Phase 3: Build & Quality — Prompt Pack

### 11. TECH_STACK.md
**Purpose:** To choose the right tools for building a fast, modern portfolio.
```text
You are a senior front-end engineer recommending a tech stack for a personal portfolio.

INPUTS:
Portfolio PRD: [PASTE PORTFOLIO_PRD]
Design System: [PASTE DESIGN_SYSTEM]
Animation Spec: [PASTE ANIMATION_SPEC]

Create a Tech Stack document with these sections:
1. Framework choice (Next.js vs Astro vs Vite + React vs Plain HTML)
   - Justify with pros, cons, and use case fit
2. Styling approach (Tailwind CSS, CSS Modules, Styled Components)
3. Component library (Shadcn/ui, Radix, Headless UI, None)
4. Animation library (Framer Motion, GSAP, CSS-only)
5. Icon library (Lucide, Heroicons, React Icons)
6. Font loading strategy (Google Fonts, next/font, self-hosted)
7. Content management (Markdown, MDX, JSON, CMS)
8. Image optimization (next/image, sharp, squoosh)
9. Form handling (React Hook Form, Formspree, EmailJS)
10. SEO tools (next-seo, built-in meta)
11. Analytics (Plausible, Umami, Google Analytics)
12. Deployment platform (Vercel, Netlify, GitHub Pages)
13. Development tools (ESLint, Prettier, TypeScript)
14. Package manager (npm, pnpm, bun)
15. Folder structure
16. Environment variables needed

For each choice, explain:
- Why this tool
- What alternatives exist
- When to pick the alternative

Keep the stack modern but simple — a solo dev should build this in 1-2 weeks.
Recommend the simplest stack that gets the job done.
Do not recommend tools just because they are trending.
```

---

### 12. SEO_META.md
**Purpose:** To make the portfolio discoverable and shareable.
```text
You are an SEO specialist for personal websites.
Using the inputs below, create an SEO & Meta Tags document for a personal portfolio.

INPUTS:
Persona & Positioning: [PASTE PERSONA_POSITIONING]
Sitemap: [PASTE SITEMAP]
Portfolio PRD: [PASTE PORTFOLIO_PRD]

Provide:
1. Target keywords (Name, Role, Location, Niche)
2. Page titles (Under 60 chars)
3. Meta descriptions (Under 155 chars)
4. Open Graph tags (For LinkedIn, Facebook, WhatsApp)
5. Twitter/X card tags
6. OG image specification (1200x630 with name and role)
7. Structured data (JSON-LD: Person schema)
8. Sitemap.xml setup
9. robots.txt setup
10. Canonical URLs
11. Heading hierarchy (H1 per page, only one)
12. Image alt text strategy
13. Internal linking strategy
14. Blog SEO (If blogging)
15. Google Search Console setup
16. Bing Webmaster Tools setup
17. Common SEO mistakes to avoid

Provide copy-paste ready meta tag examples.
Explain each tag in beginner-friendly language.
Keep SEO simple — do not over-optimize.
```

---

### 13. ACCESSIBILITY.md
**Purpose:** To ensure the portfolio is usable by everyone, including people with disabilities.
```text
You are an accessibility expert specializing in web portfolios.
Using the inputs below, create an Accessibility document for a personal portfolio.

INPUTS:
Design System: [PASTE DESIGN_SYSTEM]
Wireframes: [PASTE WIREFRAME_SPEC]

Provide:
1. WCAG 2.1 AA compliance checklist
2. Color contrast rules (Minimum 4.5:1 for text, 3:1 for large text)
3. Focus states (Visible outlines, Keyboard navigation)
4. Keyboard navigation (Tab order, Skip links)
5. Screen reader support (ARIA labels, Semantic HTML)
6. Alt text rules (Decorative vs Informative images)
7. Form accessibility (Labels, Error messages, Required fields)
8. Heading hierarchy (H1 → H2 → H3, no skipping)
9. Link accessibility (Descriptive link text, no "click here")
10. Motion accessibility (prefers-reduced-motion support)
11. Text resize (Support 200% zoom)
12. Touch target sizes (Minimum 44x44px)
13. Dark mode accessibility
14. Testing tools (axe DevTools, WAVE, Lighthouse, VoiceOver)
15. Manual testing checklist

Explain each rule in beginner-friendly language.
Provide code examples where useful (ARIA, semantic HTML).
Keep accessibility practical — it should not slow down development.
```

---

### 14. PERFORMANCE.md
**Purpose:** To ensure the portfolio loads fast and scores high on Lighthouse.
```text
You are a web performance engineer.
Using the inputs below, create a Performance Optimization document for a personal portfolio.

INPUTS:
Tech Stack: [PASTE TECH_STACK]
Asset Checklist: [PASTE ASSET_CHECKLIST]

Provide:
1. Target metrics (Lighthouse 90+, LCP < 2.5s, CLS < 0.1, FID < 100ms)
2. Image optimization (WebP/AVIF, Compression, Responsive sizes, Lazy loading)
3. Font optimization (Preload, Subset, font-display: swap)
4. JavaScript optimization (Code splitting, Tree shaking, Dynamic imports)
5. CSS optimization (Purge unused, Critical CSS)
6. Bundle size targets (Under 200KB JS, Under 50KB CSS)
7. Caching strategy (Browser cache, CDN cache)
8. CDN setup (Vercel Edge, Cloudflare)
9. Third-party script audit (Remove or defer heavy scripts)
10. Animation performance (Transform and opacity only, GPU acceleration)
11. Preloading strategy (Preload key assets)
12. Prefetching strategy (Prefetch likely next pages)
13. Lighthouse audit workflow
14. Common performance mistakes
15. A pre-launch performance checklist

Explain each optimization in beginner-friendly language.
Prioritize the highest-impact optimizations first.
```

---

### 15. TESTING_CHECKLIST.md
**Purpose:** To ensure nothing is broken before launch.
```text
You are a QA engineer specializing in front-end websites.
Using the inputs below, create a Testing Checklist document for a personal portfolio.

INPUTS:
Sitemap: [PASTE SITEMAP]
Tech Stack: [PASTE TECH_STACK]
Portfolio PRD: [PASTE PORTFOLIO_PRD]

Provide:
1. Cross-browser testing (Chrome, Safari, Firefox, Edge)
2. Cross-device testing (Desktop, Tablet, Mobile)
3. Responsive testing (All breakpoints)
4. Link testing (All internal and external links)
5. Form testing (Validation, Submission, Success/Error states)
6. Navigation testing (Header, Footer, Mobile menu)
7. Content testing (Typos, Broken images, Missing alt text)
8. Animation testing (Scroll, Hover, Reduced motion)
9. Dark mode testing
10. Accessibility testing (Keyboard, Screen reader, Contrast)
11. SEO testing (Meta tags, OG image, Sitemap)
12. Performance testing (Lighthouse on all pages)
13. 404 page testing
14. Contact form deliverability testing
15. Mobile gesture testing (Swipe, Tap, Scroll)
16. A final pre-launch checklist (Everything must pass)

Format as a checkbox list.
Keep the checklist practical — a solo dev should finish it in 1-2 hours.
```

---

## Phase 4: Launch & Maintain — Prompt Pack

### 16. DEPLOYMENT.md
**Purpose:** To get the portfolio live on a custom domain.
```text
You are a deployment specialist for personal websites.
Using the inputs below, create a Deployment document for a personal portfolio.

INPUTS:
Tech Stack: [PASTE TECH_STACK]

Provide:
1. Hosting platform comparison (Vercel, Netlify, GitHub Pages, Cloudflare Pages)
2. Recommended platform and why
3. Step-by-step deployment process
4. Connecting a GitHub repository
5. Custom domain setup (Buying, DNS, Nameservers)
6. DNS configuration (A records, CNAME)
7. SSL certificate (Automatic, Let's Encrypt, Cloudflare)
8. Environment variables setup in production
9. Continuous deployment (Auto-deploy on push)
10. Preview deployments (For testing before live)
11. Custom 404 page setup
12. Redirects (Old URLs to new)
13. Domain email (Custom email like hello@yourname.com)
14. Analytics integration
15. Post-deployment verification checklist
16. Rollback strategy (If something breaks)

Explain each step in beginner-friendly language.
Keep the process simple for a solo developer.
Assume no DevOps experience.
```

---

### 17. ANALYTICS.md
**Purpose:** To track visitors and understand what's working.
```text
You are an analytics specialist for personal websites.
Using the inputs below, create an Analytics document for a personal portfolio.

INPUTS:
Portfolio PRD: [PASTE PORTFOLIO_PRD]
Deployment: [PASTE DEPLOYMENT]

Provide:
1. Why track analytics (Job offers, Inquiries, Behavior)
2. Privacy-first tools (Plausible, Umami, Fathom)
3. Google Analytics setup (If required)
4. What to track:
   - Page views
   - Unique visitors
   - Traffic sources
   - Resume downloads
   - Contact form submissions
   - Project clicks
   - Time on page
   - Bounce rate
5. Custom events (Contact form, Resume click, Social click)
6. Conversion goals
7. Dashboard setup
8. Weekly review routine
9. Privacy considerations (Cookie consent, GDPR)
10. What NOT to track (Respect user privacy)
11. Interpreting the data (How to improve based on insights)
12. Recommended tools by budget

Explain each metric in beginner-friendly language.
Keep the setup simple — 15 minutes maximum.
```

---

### 18. CASE_STUDY_TEMPLATE.md
**Purpose:** To write compelling project case studies that get you hired.
```text
You are a portfolio storytelling expert helping a developer/designer write case studies.

INPUTS:
Content Inventory: [PASTE CONTENT_INVENTORY]
Persona & Positioning: [PASTE PERSONA_POSITIONING]

Create a Case Study Template with these sections:

For each project, follow this structure:
1. Project title (Clear, not clever)
2. One-line summary (What it does, who it's for)
3. My role (Solo, Team of X, Role name)
4. Duration (Timeframe)
5. Tech stack (Languages, frameworks, tools)
6. The problem (What pain existed?)
7. The goal (What did success look like?)
8. The approach (How did I solve it? Decision-making)
9. The solution (What was built? Features)
10. The result (Metrics, Impact, User feedback)
11. Challenges (What was hard? How did I overcome it?)
12. Learnings (What would I do differently?)
13. Visuals (Screenshots, GIFs, Diagrams)
14. Links (Live demo, GitHub, Video)
15. Reflection (One paragraph on growth)

Also provide:
16. Alternative shorter format (For quick-scan readers)
17. Writing tips (Active voice, Specific over vague)
18. Common mistakes (Too technical, Too long, No results)
19. 3 example case studies (One web, One mobile, One design)

Keep the tone honest, specific, and human.
Avoid buzzwords and filler.
Write like you're explaining to a smart friend.
```

---

### 19. CONTENT_UPDATE_GUIDE.md
**Purpose:** To keep the portfolio fresh without rebuilding it every time.
```text
You are a content strategist helping a developer/designer maintain their portfolio.

INPUTS:
Content Inventory: [PASTE CONTENT_INVENTORY]
Tech Stack: [PASTE TECH_STACK]

Create a Content Update Guide with these sections:
1. How often to update (Weekly, Monthly, Quarterly)
2. What to update:
   - New projects
   - New skills
   - Resume updates
   - Testimonials
   - Blog posts (If applicable)
3. How to add a new project (Step-by-step)
4. How to remove old projects (When and why)
5. How to update the resume PDF
6. How to add a testimonial
7. How to update the bio
8. How to refresh the hero section
9. Content versioning (Keep backups)
10. A quarterly portfolio audit checklist
11. Metrics to review (Analytics insights)
12. Signs the portfolio needs a redesign
13. Tools to streamline updates (Markdown, CMS, Notion)
14. Common mistakes (Letting it go stale, Over-updating)
15. A 15-minute monthly refresh routine

Explain each step in beginner-friendly language.
Keep the maintenance realistic for a busy developer.
```

---

### 20. GLOSSARY.md
**Purpose:** To define all portfolio and web terms in one place.
```text
You are a technical writer.
Using the inputs below, create a Glossary document for a personal portfolio project.

INPUTS:
Portfolio PRD: [PASTE PORTFOLIO_PRD]
Tech Stack: [PASTE TECH_STACK]

Provide definitions for all key terms used in the project, including:
1. Portfolio terms (Hero, Above-the-fold, CTA, Case Study, Persona)
2. Design terms (Design System, Wireframe, Breakpoint, Component, Token)
3. Front-end terms (SSR, SSG, CSR, Hydration, Bundle, Hydration)
4. Styling terms (Tailwind, CSS-in-JS, CSS Modules, Utility class)
5. Performance terms (LCP, CLS, FID, Lighthouse, Core Web Vitals)
6. SEO terms (Meta tags, OG image, Sitemap, Canonical, Structured data)
7. Accessibility terms (WCAG, ARIA, Screen reader, Focus state)
8. Deployment terms (CDN, DNS, SSL, Custom domain, CI/CD)
9. Analytics terms (Event, Conversion, Bounce rate, UTM)
10. Project-specific terms
11. Acronyms and abbreviations

For each term:
- Simple definition (Beginner-friendly)
- Why it matters for this project
- Example usage in context

Keep definitions concise and understandable.
This will help the portfolio owner speak confidently about their own site.
```

---

## Summary

| Phase | Documents | Count |
| :--- | :--- | :--- |
| Phase 1: Content & Identity | `CONTENT_INVENTORY`, `BRAND_KIT`, `PERSONA_POSITIONING`, `PORTFOLIO_PRD`, `SITEMAP` | 5 |
| Phase 2: Design Blueprint | `WIREFRAME_SPEC`, `DESIGN_SYSTEM`, `RESPONSIVE_SPEC`, `ANIMATION_SPEC`, `ASSET_CHECKLIST` | 5 |
| Phase 3: Build & Quality | `TECH_STACK`, `SEO_META`, `ACCESSIBILITY`, `PERFORMANCE`, `TESTING_CHECKLIST` | 5 |
| Phase 4: Launch & Maintain | `DEPLOYMENT`, `ANALYTICS`, `CASE_STUDY_TEMPLATE`, `CONTENT_UPDATE_GUIDE`, `GLOSSARY` | 5 |
| **Total** | | **20** |

---
