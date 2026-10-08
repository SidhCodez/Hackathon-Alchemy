# Category: Vibe Coding Production Gaps — Prompt Book

**A structured prompt system to catch everything AI skips when vibe-coding.**

---

## 📌 About This Category

**Parent Group:** 10 — Meta & Builder Tools
**Category:** Vibe Coding Production Gaps
**Purpose:** Catch the 20 critical production concerns AI models systematically skip.
**Audience:** Anyone shipping AI-generated code to real users.
**Structure:** 4 Phases + Bonus Master Checklist

---

## The 4 Phases

| Phase | Focus | Documents |
| :--- | :--- | :--- |
| **Phase 1** | Discovery & Audit | Find every gap in your vibe-coded project |
| **Phase 2** | Legal & Security | Fix legal exposure and vulnerabilities |
| **Phase 3** | Performance & Accessibility | Fix UX, speed, and inclusion |
| **Phase 4** | Growth & Polish | SEO, analytics, and conversion |

---

## Phase 1: Discovery & Audit

### 1. `VIBE_GAP_AUDIT.md`
**Purpose:** Systematically scan a vibe-coded project for all 20 production gaps.
```text
You are a senior production engineer auditing a vibe-coded project.

CONTEXT:
- Project description: [PASTE PROJECT DESCRIPTION]
- Tech stack: [PASTE TECH STACK]
- Deployment target: [PASTE WHERE IT WILL BE DEPLOYED]
- Audience: [Personal / Client / Public / Hackathon]

Analyze the project against these 20 production gaps:

1. Privacy Policy
2. Terms & Conditions
3. Frontend Secrets
4. HTTPS Enforcement
5. Cookie Consent Banner
6. Meta Titles & Descriptions
7. Social Preview Image (OG Image)
8. Favicon
9. Sitemap & Robots.txt
10. Image Alt Text
11. Image Compression
12. Page Load Speed
13. Color Contrast
14. Mobile Responsiveness
15. Custom 404 Page
16. Broken Link Fixes
17. Form Validation
18. Spam Protection
19. Analytics Setup
20. Single Clear CTA

For each gap, provide:
1. Status (Present, Missing, Broken, N/A)
2. Severity (Critical, High, Medium, Low)
3. Impact if not fixed
4. Estimated fix time (Minutes, Hours)
5. Priority rank (1 = highest)

Then provide:
- Top 5 most critical gaps to fix first
- Total estimated time to production-ready
- A prioritized action plan

Keep language beginner-friendly.
Do not assume the developer knows these concepts.
```

---

### 2. `PROJECT_HEALTH_REPORT.md`
**Purpose:** Generate a health score for the project across all 5 dimensions.
```text
You are a senior QA lead.
Generate a Project Health Report for this vibe-coded project.

CONTEXT:
[PASTE PROJECT DESCRIPTION AND AUDIT RESULTS]

Score the project (0-100) across these 5 dimensions:

1. LEGAL HEALTH
   - Privacy policy (25 points)
   - Terms & conditions (25 points)
   - Cookie consent (25 points)
   - GDPR/CCPA compliance (25 points)

2. SECURITY HEALTH
   - No frontend secrets (30 points)
   - HTTPS enforced (20 points)
   - Form validation (25 points)
   - Spam protection (25 points)

3. PERFORMANCE HEALTH
   - Image compression (25 points)
   - Page load speed (25 points)
   - Lighthouse score (25 points)
   - Core Web Vitals (25 points)

4. ACCESSIBILITY HEALTH
   - Image alt text (25 points)
   - Color contrast (25 points)
   - Keyboard navigation (25 points)
   - Screen reader support (25 points)

5. GROWTH HEALTH
   - SEO meta tags (20 points)
   - Sitemap & robots.txt (20 points)
   - Analytics setup (20 points)
   - Single clear CTA (20 points)
   - Social preview image (20 points)

Provide:
- Overall score (0-100)
- Grade (A+, A, B, C, D, F)
- Strengths (What's working well)
- Weaknesses (What needs urgent attention)
- Top 3 quick wins (Under 1 hour)
- Top 3 long-term fixes (Multi-day)

Format the report with clear sections and emoji indicators.
```

---

### 3. `PRIORITY_MATRIX.md`
**Purpose:** Create a priority matrix for all fixes (impact vs effort).
```text
You are a senior engineering manager.
Create a Priority Matrix for fixing vibe-coding gaps.

CONTEXT:
[PASTE GAP AUDIT RESULTS]

For each of the 20 gaps, plot against:
- Impact (1-5): How much does it matter?
- Effort (1-5): How hard is it to fix?
- Risk (1-5): How bad if ignored?

Categorize into:
1. DO NOW (High Impact, Low Effort, High Risk)
2. SCHEDULE (High Impact, High Effort)
3. DELEGATE (Low Impact, Low Effort)
4. IGNORE (Low Impact, High Effort)

Provide a quadrant chart (text-based).

Then give:
- Top 5 "Do Now" items
- Suggested 7-day sprint plan
- Weekly milestones

Explain each decision in beginner-friendly language.
```

---

## Phase 2: Legal & Security

### 4. `PRIVACY_POLICY.md`
**Purpose:** Generate a complete privacy policy.
```text
You are a legal-tech specialist.
Generate a complete Privacy Policy for this project.

CONTEXT:
- Project name: [PASTE PROJECT NAME]
- URL: [PASTE URL]
- What data is collected: [PASTE DATA TYPES]
- Third-party services: [PASTE ANALYTICS, APIS, COOKIES]
- User location: [PASTE TARGET REGION]
- Contact email: [PASTE EMAIL]

Generate the privacy policy with these sections:
1. Introduction
2. Information We Collect
3. How We Use Information
4. Cookies and Tracking
5. Third-Party Services
6. Data Storage and Security
7. User Rights (GDPR, CCPA)
8. Children's Privacy
9. International Data Transfers
10. Changes to Policy
11. Contact Information

Format as HTML with Tailwind classes ready to drop into a page.
Include placeholders like [DATE] where needed.
Use plain, readable English (Grade 8 level).
Do not use legal jargon unless necessary.
```

---

### 5. `TERMS_CONDITIONS.md`
**Purpose:** Generate complete Terms & Conditions.
```text
You are a legal-tech specialist.
Generate complete Terms & Conditions for this project.

CONTEXT:
- Project name: [PASTE PROJECT NAME]
- URL: [PASTE URL]
- What the product does: [PASTE DESCRIPTION]
- User interactions: [PASTE]
- Monetization (if any): [PASTE]
- Jurisdiction: [PASTE COUNTRY/STATE]

Generate the Terms & Conditions with these sections:
1. Acceptance of Terms
2. Description of Service
3. User Accounts (if applicable)
4. User Responsibilities
5. Prohibited Activities
6. Intellectual Property
7. Payment Terms (if applicable)
8. Refund Policy (if applicable)
9. Limitation of Liability
10. Indemnification
11. Termination
12. Governing Law
13. Changes to Terms
14. Contact Information

Format as HTML with Tailwind classes ready to drop into a page.
Use plain English where possible.
Include placeholders for jurisdiction-specific details.
```

---

### 6. `SECRET_AUDIT.md`
**Purpose:** Find and remove all frontend secrets.
```text
You are a security engineer.
Perform a Secret Audit for this vibe-coded project.

CONTEXT:
- Tech stack: [PASTE STACK]
- Repository: [PASTE REPO OR FILE LIST]

Provide:

1. SEARCH COMMANDS
List all terminal commands to find secrets in the codebase:
- grep for API keys (sk-, pk-, AIza, etc.)
- grep for Bearer tokens
- grep for .env usage in frontend
- grep for hardcoded passwords
- grep for database URLs

2. VULNERABILITY LIST
For each secret found:
- File location
- Line number
- Type of secret
- Severity (Critical, High, Medium)
- Exposure risk

3. REMEDIATION
For each secret:
- Where to move it (backend, env vault)
- How to rotate it
- How to update the code

4. PREVENTION
- Add to .gitignore
- Create .env.example
- Set up pre-commit hooks
- Enable GitHub secret scanning
- Recommended tools (git-secrets, trufflehog, gitleaks)

5. VERIFICATION CHECKLIST
- [ ] No secrets in frontend
- [ ] .env in .gitignore
- [ ] .env.example provided
- [ ] All secrets rotated
- [ ] Git history cleaned (if leaked)

Explain everything in beginner-friendly language.
Provide copy-paste terminal commands.
```

---

### 7. `HTTPS_ENFORCEMENT.md`
**Purpose:** Ensure HTTPS is enforced and secure.
```text
You are a DevOps engineer.
Create an HTTPS Enforcement guide for this project.

CONTEXT:
- Hosting platform: [PASTE PLATFORM]
- Domain: [PASTE DOMAIN]
- Current setup: [PASTE]

Provide:

1. PLATFORM-SPECIFIC SETUP
For [Vercel / Netlify / Cloudflare / AWS / Custom]:
- How to enable HTTPS
- How to force HTTPS redirect
- How to get free SSL
- How to set HSTS header

2. CONFIGURATION EXAMPLES
- Nginx redirect config
- Apache .htaccess config
- Cloudflare settings
- Vercel/Netlify dashboard steps

3. SECURITY HEADERS
Add these headers:
- Strict-Transport-Security
- X-Content-Type-Options
- X-Frame-Options
- Content-Security-Policy
- Referrer-Policy
- Permissions-Policy

4. VERIFICATION
- Test with SSL Labs
- Test with Security Headers
- Test HTTP → HTTPS redirect
- Check for mixed content

5. COMMON MISTAKES
- Mixed content warnings
- Expired certificates
- Missing redirects
- Weak ciphers

Provide copy-paste config files.
Explain in beginner-friendly language.
```

---

### 8. `COOKIE_CONSENT.md`
**Purpose:** Add a GDPR-compliant cookie consent banner.
```text
You are a privacy compliance expert.
Create a Cookie Consent implementation guide.

CONTEXT:
- Site URL: [PASTE URL]
- Cookies used: [PASTE COOKIES]
- Analytics: [PASTE TOOLS]
- Target region: [EU / US / Global]

Provide:

1. COOKIE INVENTORY
- List all cookies (name, purpose, duration)
- Essential vs non-essential
- First-party vs third-party

2. BANNER DESIGN
- Text copy (friendly, clear)
- Accept button
- Reject button
- Customize button
- Link to privacy policy

3. IMPLEMENTATION OPTIONS
Option A: Free tool
- CookieYes, Osano, Klaro

Option B: Custom code
- Show code snippet
- Block cookies until consent
- Remember preference (localStorage)

4. BLOCKING STRATEGY
- Block analytics until consent
- Block ads until consent
- Block third-party embeds until consent

5. COMPLIANCE CHECKLIST
- [ ] Banner shows on first visit
- [ ] No cookies before consent
- [ ] Reject option exists
- [ ] Preference saved
- [ ] Privacy policy linked
- [ ] Re-consent on policy change

Provide HTML/CSS/JS code snippets.
Explain in beginner-friendly language.
```

---

## Phase 3: Performance & Accessibility

### 9. `SEO_META_TAGS.md`
**Purpose:** Add SEO meta tags to every page.
```text
You are an SEO specialist.
Generate SEO meta tags for every page of this project.

CONTEXT:
- Project name: [PASTE NAME]
- URL: [PASTE URL]
- Pages: [PASTE PAGE LIST]
- Target keywords: [PASTE]

For each page, generate:
1. Title tag (50-60 chars)
2. Meta description (150-160 chars)
3. Canonical URL
4. OG title
5. OG description
6. OG image URL
7. Twitter card tags
8. Keywords meta (optional)

Format as:
- HTML `<head>` snippets (for static sites)
- Next.js `metadata` objects (for Next.js)
- React Helmet examples (for React SPAs)

Also provide:
- Homepage: Maximum impact tags
- About page: Personal brand tags
- Projects page: Portfolio tags
- Contact page: Conversion tags

Include a master template that can be reused.
Explain what each tag does in beginner-friendly language.
```

---

### 10. `OG_IMAGE_GENERATION.md`
**Purpose:** Create social preview images.
```text
You are a designer and social media expert.
Create an OG Image generation guide.

CONTEXT:
- Brand colors: [PASTE COLORS]
- Logo: [PASTE LOGO INFO]
- Project name: [PASTE NAME]
- URL: [PASTE URL]

Provide:

1. OG IMAGE SPECIFICATIONS
- Size: 1200 x 630 pixels
- Format: PNG or JPG
- File size: < 300KB
- Safe zone: 1080 x 600 (center)

2. DESIGN TEMPLATE
- Layout (Logo top-left, Title center, URL bottom)
- Typography (Bold, readable at small size)
- Color usage (Brand colors, high contrast)
- Background (Solid, gradient, or pattern)

3. CONTENT VARIATIONS
Design 5 OG images:
- Homepage
- About page
- Each project (Skill Bridge, WalletGuard, ColdCase, VIRASETU)
- Blog posts (if applicable)

4. TOOLS
- Figma template
- Canva template
- Code-based (Vercel OG, Satori)
- Dynamic generation (Next.js ImageResponse)

5. IMPLEMENTATION
Add to <head>:
- og:image
- og:image:width
- og:image:height
- twitter:image

6. TESTING
- LinkedIn Post Inspector
- Twitter Card Validator
- OpenGraph.xyz
- Facebook Debugger

Provide Figma/Canva design specs and HTML snippets.
```

---

### 11. `FAVICON_SETUP.md`
**Purpose:** Create a complete favicon set.
```text
You are a branding designer.
Create a complete Favicon setup guide.

CONTEXT:
- Logo: [PASTE LOGO]
- Brand colors: [PASTE COLORS]
- Project name: [PASTE NAME]

Provide:

1. FAVICON SIZES NEEDED
- favicon.ico (16x16, 32x32, 48x48 combined)
- favicon-16x16.png
- favicon-32x32.png
- apple-touch-icon.png (180x180)
- android-chrome-192x192.png
- android-chrome-512x512.png
- mstile-150x150.png (Windows)
- safari-pinned-tab.svg

2. GENERATION TOOLS
- RealFaviconGenerator (recommended)
- Favicon.io
- Canva

3. FILE PLACEMENT
- /public/ folder structure
- Naming conventions

4. HTML IMPLEMENTATION
Provide copy-paste `<head>` code:
- All icon links
- Manifest link
- Theme color meta

5. MANIFEST.JSON
Provide site.webmanifest content:
- Name
- Short name
- Icons
- Theme color
- Background color
- Display mode

6. TESTING CHECKLIST
- [ ] Browser tab shows icon
- [ ] Bookmark shows icon
- [ ] iOS home screen works
- [ ] Android home screen works
- [ ] Dark mode version (if applicable)

Provide all config files and HTML snippets.
Explain in beginner-friendly language.
```

---

### 12. `SITEMAP_ROBOTS.md`
**Purpose:** Generate sitemap.xml and robots.txt.
```text
You are an SEO technical specialist.
Generate sitemap.xml and robots.txt for this project.

CONTEXT:
- Project URL: [PASTE URL]
- Pages: [PASTE PAGE LIST]
- Update frequency: [PASTE]
- Admin/private areas: [PASTE]

Provide:

1. ROBOTS.TXT
- User-agent rules
- Allow/Disallow paths
- Sitemap URL
- Crawl delay (if needed)

2. SITEMAP.XML
- All public pages
- Last modified dates
- Change frequency
- Priority values

3. STATIC GENERATION
- File placement (/public/)
- Manual XML example

4. DYNAMIC GENERATION
- Next.js `app/sitemap.js` example
- React with react-router-sitemap
- Vite plugin

5. SUBMISSION
- Google Search Console steps
- Bing Webmaster Tools steps
- Yandex (if targeting Russia)

6. VERIFICATION
- Test sitemap loads
- Test robots.txt loads
- Confirm pages are indexed
- Check for crawl errors

Provide complete file contents and setup instructions.
Explain in beginner-friendly language.
```

---

### 13. `IMAGE_OPTIMIZATION.md`
**Purpose:** Compress and optimize all images.
```text
You are a performance engineer.
Create an Image Optimization guide for this project.

CONTEXT:
- Tech stack: [PASTE STACK]
- Current images: [PASTE FILE LIST OR SIZE]

Provide:

1. AUDIT
- List all images with current sizes
- Identify oversized images (> 200KB)
- Identify wrong formats (PNG for photos)

2. FORMAT CONVERSION
- Convert JPG/PNG to WebP
- Convert to AVIF where supported
- Use SVG for icons and logos
- Use next/image for Next.js

3. COMPRESSION TARGETS
- Hero image: < 200KB
- Section images: < 100KB
- Thumbnails: < 50KB
- Icons: < 10KB
- Total page: < 1MB

4. TOOLS
- Squoosh (manual)
- TinyPNG (bulk)
- ImageOptim (Mac)
- Sharp (programmatic)
- next/image (automatic)

5. IMPLEMENTATION
For each tech stack:
- Next.js: <Image> component
- React: lazy loading
- Static HTML: <picture> tag

6. LAZY LOADING
- Below-the-fold images
- `loading="lazy"` attribute
- Intersection Observer

7. CDN & RESPONSIVE IMAGES
- srcset attribute
- sizes attribute
- CDN with image transformation

8. VERIFICATION
- Test on PageSpeed Insights
- Check LCP < 2.5s
- Check total page weight < 1MB

Provide copy-paste code snippets.
```

---

### 14. `PAGE_SPEED_AUDIT.md`
**Purpose:** Achieve a Lighthouse score of 90+.
```text
You are a web performance expert.
Create a Page Speed audit and optimization guide.

CONTEXT:
- Project URL: [PASTE URL]
- Current Lighthouse score: [PASTE OR "unknown"]

Provide:

1. LIGHTHOUSE AUDIT
Run audit and analyze:
- Performance score
- LCP (Largest Contentful Paint)
- INP (Interaction to Next Paint)
- CLS (Cumulative Layout Shift)
- TTFB (Time to First Byte)

2. QUICK WINS (Under 1 hour)
- Compress images
- Add lazy loading
- Enable text compression
- Remove unused CSS
- Defer non-critical JS
- Preload critical fonts

3. MEDIUM FIXES (1-4 hours)
- Code splitting
- Route-based lazy loading
- Cache static assets
- Optimize third-party scripts
- Preconnect to external domains
- Inline critical CSS

4. ADVANCED FIXES (1+ days)
- Server-side rendering
- Static site generation
- Edge caching
- Database query optimization
- Migration to CDN

5. TOOLS
- Lighthouse (Chrome DevTools)
- PageSpeed Insights
- WebPageTest
- GTmetrix
- Chrome Coverage tab

6. MEASUREMENT
- Before/After comparison
- Core Web Vitals monitoring
- Real User Monitoring (RUM)

7. CHECKLIST
- [ ] Lighthouse score > 90
- [ ] LCP < 2.5s
- [ ] CLS < 0.1
- [ ] INP < 200ms
- [ ] No render-blocking resources
- [ ] Compression enabled

Provide actionable steps with code snippets.
```

---

### 15. `COLOR_CONTRAST_FIX.md`
**Purpose:** Ensure WCAG AA compliance for all text.
```text
You are an accessibility specialist.
Create a Color Contrast fix guide for this project.

CONTEXT:
- Brand colors: [PASTE COLORS]
- UI elements: [PASTE]

Provide:

1. CONTRAST REQUIREMENTS
- Normal text: 4.5:1 minimum
- Large text (18pt+): 3:1 minimum
- UI components: 3:1 minimum
- Focus indicators: 3:1 minimum

2. AUDIT
List all color combinations in the project:
- Text on background
- Buttons (default, hover, active)
- Links (default, visited, hover)
- Form labels and inputs
- Navigation items
- Icons and indicators

For each, calculate contrast ratio and mark as:
- ✅ Pass
- ⚠️ Marginal
- ❌ Fail

3. FIXES
For each ❌ failure:
- Current colors
- Contrast ratio
- Suggested replacement colors
- New contrast ratio

4. TESTING TOOLS
- WebAIM Contrast Checker
- Coolors Contrast Checker
- Chrome DevTools (inspect + contrast)
- WAVE browser extension
- Axe DevTools

5. DARK MODE
- Check contrast in dark mode too
- Ensure colors work in both modes

6. CHECKLIST
- [ ] All body text passes 4.5:1
- [ ] All large text passes 3:1
- [ ] All buttons pass 3:1
- [ ] All form fields pass 3:1
- [ ] Focus states visible
- [ ] Dark mode tested

Provide before/after color codes and testing steps.
```

---

### 16. `MOBILE_RESPONSIVENESS.md`
**Purpose:** Ensure the site works perfectly on every device.
```text
You are a responsive design expert.
Create a Mobile Responsiveness audit and fix guide.

CONTEXT:
- Project URL: [PASTE URL]
- Tech stack: [PASTE STACK]

Provide:

1. BREAKPOINT TESTING
Test on:
- 320px (iPhone SE)
- 375px (iPhone 12)
- 414px (iPhone Plus)
- 768px (iPad)
- 1024px (iPad Pro)
- 1440px (Laptop)
- 1920px (Desktop)

2. COMMON MOBILE ISSUES
- Horizontal scroll
- Tiny tap targets (< 44px)
- Small font (< 16px)
- Overlapping elements
- Hidden content
- Broken navigation
- Zoom required
- Slow load on 3G

3. FIXES
For each issue:
- What's wrong
- CSS fix
- Verification method

4. RESPONSIVE PATTERNS
- Mobile-first CSS
- Flexbox layouts
- CSS Grid
- Fluid typography (clamp)
- Responsive images (srcset)
- Hamburger menus

5. TESTING CHECKLIST
- [ ] No horizontal scroll
- [ ] Tap targets ≥ 44px
- [ ] Font ≥ 16px
- [ ] No overlapping elements
- [ ] All content accessible
- [ ] Navigation works
- [ ] Images fit viewport
- [ ] Tested on real phone

6. TOOLS
- Chrome DevTools Device Toolbar
- Responsively App
- BrowserStack (real devices)
- LambdaTest

Provide CSS snippets and testing steps.
```

---

### 17. `CUSTOM_404.md`
**Purpose:** Create a friendly, branded 404 page.
```text
You are a UX designer.
Create a Custom 404 Page for this project.

CONTEXT:
- Project name: [PASTE]
- Brand colors: [PASTE]
- Brand voice: [PASTE TONE]
- Popular pages: [PASTE PAGE LIST]

Provide:

1. CONTENT STRATEGY
- Friendly headline (Not "Error 404")
- Short explanation
- Reassurance (Not user's fault)
- Helpful links
- Search box (optional)

2. DESIGN
- Brand colors
- Illustration or icon (optional)
- Consistent with site
- Mobile responsive

3. CODE
- Next.js `not-found.js`
- React Router 404 route
- Static HTML 404.html

4. SUGGESTED PAGES
- Home
- Projects
- About
- Contact
- Blog (if exists)

5. TONE EXAMPLES
Friendly: "Looks like this page wandered off."
Playful: "404 — This page went on vacation."
Professional: "We couldn't find that page."

6. CHECKLIST
- [ ] Custom page exists
- [ ] Friendly message
- [ ] Link to home
- [ ] Links to popular pages
- [ ] Matches branding
- [ ] Mobile responsive
- [ ] Returns 404 status code

Provide full code snippets (HTML + CSS + JS).
```

---

### 18. `BROKEN_LINK_AUDIT.md`
**Purpose:** Find and fix all broken links.
```text
You are a QA engineer.
Create a Broken Link audit and fix guide.

CONTEXT:
- Project URL: [PASTE URL]
- Pages: [PASTE PAGE LIST]

Provide:

1. AUDIT TOOLS
- W3C Link Checker
- Broken Link Checker
- Ahrefs Broken Link Checker
- Screaming Frog (500 URLs free)

2. COMMON ISSUES
- href="#" (placeholder links)
- External links 404
- Internal links to removed pages
- Typos in URLs
- Case-sensitivity issues
- Missing trailing slashes

3. SCAN COMMANDS
Provide terminal commands:
- grep for href="#"
- grep for dead URLs
- grep for http:// (should be https://)

4. FIX PROCESS
For each broken link:
- Location
- Type (Internal, External, Placeholder)
- Fix approach
- Verify after fix

5. EXTERNAL LINK HYGIENE
Add to all external links:
- target="_blank"
- rel="noopener noreferrer"

6. PREVENTION
- Pre-commit hooks
- CI link checker
- Quarterly audits

7. CHECKLIST
- [ ] No href="#"
- [ ] All internal links work
- [ ] All external links work
- [ ] No 404s from own site
- [ ] External links have rel="noopener"

Provide scan commands and fix examples.
```

---

### 19. `FORM_VALIDATION.md`
**Purpose:** Add robust client + server validation.
```text
You are a full-stack developer.
Create a Form Validation implementation guide.

CONTEXT:
- Forms: [PASTE FORM LIST]
- Tech stack: [PASTE STACK]

Provide:

1. VALIDATION PRINCIPLES
- Never trust client
- Validate on both sides
- Give clear feedback
- Prevent bad data
- Protect against injection

2. CLIENT-SIDE VALIDATION
HTML5 attributes:
- required
- type="email"
- minlength / maxlength
- pattern
- min / max

JavaScript validation:
- Real-time feedback
- Custom error messages
- Accessibility (aria-invalid, aria-describedby)

3. SERVER-SIDE VALIDATION
For each form:
- Field validation rules
- Sanitization (strip HTML)
- Type coercion
- Reject invalid
- Log suspicious activity

4. SECURITY
- SQL injection prevention (parameterized queries)
- XSS prevention (escape output)
- CSRF protection (tokens)
- File upload restrictions

5. ERROR UX
- Inline errors
- Field-specific messages
- Summary of errors
- Accessible announcements

6. CODE EXAMPLES
- React Hook Form + Zod
- Vanilla JS validation
- Server validation (Node, Python)

7. CHECKLIST
- [ ] All required fields enforced
- [ ] Email format validated
- [ ] Password strength enforced
- [ ] Server-side validation exists
- [ ] Error messages clear
- [ ] Success confirmation shown
- [ ] Inputs sanitized

Provide copy-paste code for each stack.
```

---

### 20. `SPAM_PROTECTION.md`
**Purpose:** Protect forms from bots and spam.
```text
You are a security engineer.
Create a Spam Protection implementation guide.

CONTEXT:
- Forms: [PASTE FORM LIST]
- Expected traffic: [PASTE]
- Budget: [PASTE]

Provide:

1. LAYERED DEFENSE
Layer 1: Honeypot
Layer 2: Rate limiting
Layer 3: Time-based checks
Layer 4: CAPTCHA (if needed)
Layer 5: Email verification

2. HONEYPOT
- Invisible field
- Common bot names (website, url, company)
- CSS to hide (display:none, position:absolute)
- Reject if filled

3. RATE LIMITING
- Max submissions per IP per minute
- Max submissions per email per hour
- Tools (express-rate-limit, Cloudflare)

4. TIME-BASED
- Reject if submitted < 3 seconds after load
- Track form load timestamp
- Compare on submit

5. CAPTCHA OPTIONS
- reCAPTCHA v3 (invisible)
- hCaptcha (privacy-friendly)
- Cloudflare Turnstile (free)

6. EMAIL VERIFICATION
- Send confirmation email
- Only process after click
- Prevent fake submissions

7. LOGGING
- Log all submissions
- Log IP, timestamp, user agent
- Alert on suspicious patterns

8. CHECKLIST
- [ ] Honeypot field added
- [ ] Rate limiting enabled
- [ ] Time-based check
- [ ] CAPTCHA (if needed)
- [ ] Email verification (if needed)
- [ ] Logging enabled
- [ ] Alerts configured

Provide copy-paste code for each layer.
```

---

## Phase 4: Growth & Polish

### 21. `ANALYTICS_SETUP.md`
**Purpose:** Install privacy-friendly analytics and track key events.
```text
You are an analytics engineer.
Create an Analytics Setup guide for this project.

CONTEXT:
- Project URL: [PASTE]
- Privacy preference: [Privacy-first / Standard]
- Budget: [Free / Paid]

Provide:

1. TOOL SELECTION
Compare:
- Plausible (privacy, $9/mo)
- Umami (self-hosted, free)
- Fathom (privacy, $14/mo)
- Google Analytics 4 (free, complex)
- PostHog (open source)

Recommend one based on context.

2. INSTALLATION
Provide copy-paste script for:
- Plausible
- Umami
- GA4
- Fathom

3. EVENT TRACKING
Track these events:
- Page views
- Button clicks (CTA, Download)
- Form submissions
- Resume downloads
- External link clicks
- 404 errors
- File downloads

4. GOALS / CONVERSIONS
Set up conversion goals:
- Contact form submit
- Resume download
- Newsletter signup
- Hire me click

5. DASHBOARDS
- Traffic overview
- Top pages
- Traffic sources
- Conversion funnel

6. PRIVACY
- Update privacy policy
- Add cookie consent (if needed)
- Anonymize IPs
- GDPR compliance

7. VERIFICATION
- [ ] Script loads
- [ ] Page views tracked
- [ ] Events fire correctly
- [ ] Goals show conversions
- [ ] Privacy policy updated

Provide copy-paste snippets.
```

---

### 22. `CTA_OPTIMIZATION.md`
**Purpose:** Design a single, clear call-to-action per page.
```text
You are a conversion optimization expert.
Create a CTA Optimization guide for this project.

CONTEXT:
- Project: [PASTE NAME]
- Goal: [Hire / Freelance / Portfolio / Brand]
- Pages: [PASTE PAGE LIST]

Provide:

1. CTA STRATEGY
One primary CTA per page:
- Homepage: "View Projects" or "Hire Me"
- About: "Download Resume"
- Projects: "View Live Demo"
- Contact: "Send Message"
- Blog: "Subscribe"

2. CTA HIERARCHY
- Primary (Filled button, brand color)
- Secondary (Outlined, subtle)
- Tertiary (Text link)

3. CTA COPY
Action verb + value:
- "View My Projects"
- "Download Resume"
- "Hire Me"
- "Get Started Free"
- "Book a Call"

Avoid:
- "Click Here"
- "Submit"
- "Learn More" (vague)

4. PLACEMENT
- Above the fold (Hero)
- After every major section
- Sticky footer CTA (optional)
- Exit intent (advanced)

5. DESIGN
- High contrast
- Larger than secondary
- Whitespace around it
- Mobile-friendly (min 44px)

6. A/B TESTING
- Test copy variations
- Test color
- Test placement
- Measure conversion

7. CHECKLIST
- [ ] One primary CTA per page
- [ ] CTA uses action verb
- [ ] CTA is above the fold
- [ ] Secondary CTAs visually weaker
- [ ] CTA copy is specific
- [ ] Mobile tap target ≥ 44px

Provide CTA examples and A/B test plan.
```

---

### 23. `MASTER_PRE_LAUNCH_CHECKLIST.md`
**Purpose:** Final checklist before shipping to real users.
```text
You are a senior engineer doing final QA.
Generate the ultimate Pre-Launch Checklist for this project.

CONTEXT:
- Project: [PASTE NAME]
- URL: [PASTE URL]
- Audience: [PASTE]

Organize into these categories:

1. LEGAL (4 items)
- [ ] Privacy policy linked
- [ ] Terms & conditions linked
- [ ] Cookie consent shows
- [ ] GDPR/CCPA compliant

2. SECURITY (6 items)
- [ ] No frontend secrets
- [ ] HTTPS enforced
- [ ] HSTS header set
- [ ] Form validation works
- [ ] Spam protection active
- [ ] Rate limiting enabled

3. SEO (7 items)
- [ ] Meta titles on every page
- [ ] Meta descriptions on every page
- [ ] OG image exists
- [ ] Favicon set
- [ ] Sitemap.xml
- [ ] Robots.txt
- [ ] Submitted to Google Search Console

4. PERFORMANCE (6 items)
- [ ] Images compressed
- [ ] Modern formats used
- [ ] Lighthouse score > 90
- [ ] LCP < 2.5s
- [ ] Lazy loading enabled
- [ ] CDN configured

5. ACCESSIBILITY (5 items)
- [ ] Alt text on all images
- [ ] Color contrast passes WCAG AA
- [ ] Keyboard navigation works
- [ ] Focus states visible
- [ ] Screen reader tested

6. UX (6 items)
- [ ] Mobile responsive (all breakpoints)
- [ ] Custom 404 page
- [ ] No broken links
- [ ] Form errors clear
- [ ] Loading states present
- [ ] Success states present

7. CONVERSION (4 items)
- [ ] One clear CTA per page
- [ ] CTA above the fold
- [ ] Analytics installed
- [ ] Conversion goals tracked

8. FINAL LAUNCH (5 items)
- [ ] Tested on real device
- [ ] Tested on slow network
- [ ] Backup plan if deployment fails
- [ ] Rollback plan
- [ ] Post-launch monitoring

Provide:
- Priority order (What to fix first)
- Estimated time per section
- Go/No-go decision criteria

Format as a printable checklist.
```

---

## Support Documents

### 24. `VIBE_CODING_GLOSSARY.md`
```text
You are a technical writer.
Create a Vibe Coding Glossary for non-technical users.

CONTEXT:
[PASTE PROJECT DETAILS]

Define these terms in beginner-friendly language:

1. Legal Terms
- Privacy Policy
- Terms & Conditions
- GDPR
- CCPA
- Cookie Consent

2. Security Terms
- API Key
- Environment Variable
- HTTPS
- HSTS
- CSRF
- XSS
- Honeypot
- Rate Limiting

3. Performance Terms
- Core Web Vitals
- LCP
- INP
- CLS
- TTFB
- Lazy Loading
- CDN

4. SEO Terms
- Meta Tags
- OG Image
- Favicon
- Sitemap
- Robots.txt
- Canonical URL

5. Accessibility Terms
- WCAG
- Alt Text
- Color Contrast
- ARIA
- Screen Reader

6. Growth Terms
- CTA
- Conversion
- Analytics
- Funnel

For each term:
- Simple definition (One sentence, no jargon)
- Real-world analogy
- Why it matters

Use analogies wherever possible.
Keep it extremely simple.
```

---

### 25. `LAUNCH_DAY_PLAYBOOK.md`
```text
You are a launch strategist.
Create a Launch Day Playbook for this project.

CONTEXT:
- Project: [PASTE]
- Launch date: [PASTE]
- Platform: [PASTE]

Provide:

1. T-7 DAYS
- Complete master checklist
- Final device testing
- Backup all files
- Draft announcement

2. T-3 DAYS
- Deploy to staging
- Full regression test
- Prepare social posts
- Notify stakeholders

3. T-1 DAY
- Freeze features
- Final deploy to prod
- Smoke test
- Prepare rollback plan

4. LAUNCH DAY
- Deploy final version
- Verify HTTPS, SSL
- Test critical flows
- Monitor analytics
- Announce on channels

5. T+1 DAY
- Review analytics
- Check error logs
- Respond to feedback
- Fix critical bugs

6. T+7 DAYS
- Full performance review
- Gather user feedback
- Plan next iteration

7. ROLLBACK PLAN
- Trigger conditions
- Rollback steps
- Communication plan

8. MONITORING
- Analytics dashboard
- Error tracking
- Uptime monitoring
- Alerts

Format as a timeline with checkboxes.
```

---

## Footer (End of Category)
---

## 📋 Category Summary

| Phase | Documents | Count |
| :--- | :--- | :--- |
| **Phase 1: Discovery & Audit** | `VIBE_GAP_AUDIT`, `PROJECT_HEALTH_REPORT`, `PRIORITY_MATRIX` | 3 |
| **Phase 2: Legal & Security** | `PRIVACY_POLICY`, `TERMS_CONDITIONS`, `SECRET_AUDIT`, `HTTPS_ENFORCEMENT`, `COOKIE_CONSENT` | 5 |
| **Phase 3: Performance & Accessibility** | `SEO_META_TAGS`, `OG_IMAGE_GENERATION`, `FAVICON_SETUP`, `SITEMAP_ROBOTS`, `IMAGE_OPTIMIZATION`, `PAGE_SPEED_AUDIT`, `COLOR_CONTRAST_FIX`, `MOBILE_RESPONSIVENESS`, `CUSTOM_404`, `BROKEN_LINK_AUDIT`, `FORM_VALIDATION`, `SPAM_PROTECTION` | 12 |
| **Phase 4: Growth & Polish** | `ANALYTICS_SETUP`, `CTA_OPTIMIZATION`, `MASTER_PRE_LAUNCH_CHECKLIST` | 3 |
| **Support** | `VIBE_CODING_GLOSSARY`, `LAUNCH_DAY_PLAYBOOK` | 2 |
| **Total** | | **25 Documents** |

---
