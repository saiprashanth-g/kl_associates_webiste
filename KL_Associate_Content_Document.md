# KL Associate — Website Content & Design Document
### Everything that goes into the website. No code. No guides.

---

# PART 1 — BRAND & DESIGN SYSTEM

---

## Company Identity

**Company Name:** KL Associate  
**Location:** Chennai, Tamil Nadu, India  
**Industry:** Construction & Engineering  
**Tagline:** Building Strength, Delivering Excellence  
**Vision:** To redefine the built environment through timeless, sustainable, and innovative design and construction that inspires communities and enhances quality of life worldwide.  
**Mission:** To deliver innovative, sustainable, and high-quality construction solutions through excellence, integrity, and collaboration, creating lasting value for our clients and communities.

---

## Color System

| Role | Name | Hex |
|------|------|-----|
| Primary | Deep Navy | #051650 |
| Secondary | Near White | #F5FEFD |
| Secondary Alt | Soft Mint | #EBF5F0 |
| Accent | Gold | #C9963D |
| Text Dark | Near Black | #111111 |
| Text Mid | Dark Grey | #444444 |
| Text Light | Near White | #F5FEFD |
| Border | Navy Transparent | rgba(5, 22, 80, 0.12) |

**Usage rules:**
- Navy (#051650) is dominant — used for navigation, footer, stats bar, testimonials section, and all headings
- Gold (#C9963D) is the accent — used only for CTAs, hover states, active states, stat numbers, and highlights
- Near White (#F5FEFD) and Soft Mint (#EBF5F0) alternate as section backgrounds
- Text is always #111111 on light backgrounds, #F5FEFD on dark/navy backgrounds
- Gold is never used as a background color for large areas

---

## Typography

**Display / Hero Headlines**
- Font: Cormorant Garamond
- Weights used: 600, 700
- Used for: Hero headline, all section headings (H2), testimonial quotes
- Character: Elegant, architectural, premium serif

**Sub-headings**
- Font: DM Serif Display
- Weight: 400
- Used for: H3 labels, card titles, sub-section headings

**Body & UI**
- Font: DM Sans
- Weights used: 300 (light), 400 (regular), 500 (medium)
- Used for: All body copy, navigation links, labels, captions, form fields, button text

**Type Scale**
- Hero headline: fluid, large — Cormorant Garamond 700
- Section heading (H2): large — Cormorant Garamond 600
- Sub-heading (H3): medium — DM Serif Display 400
- Body text: 16px, DM Sans 400, line height 1.75
- Section label (eyebrow): 12px, DM Sans 500, uppercase, wide letter spacing
- Caption / tag: 12px, DM Sans 400

---

## Spacing & Layout

- Maximum content width: 1200px, centered
- Section vertical padding: generous — large on desktop, reduced on mobile
- Card border radius: 4px (sharp, architectural — not rounded or bubbly)
- Button border radius: 2px
- Grid gap between cards: 32px
- Cards never have heavy shadows — only a subtle lift on hover

---

## Animation Approach (GSAP — already installed)

GSAP with ScrollTrigger is the animation library. The following are the animation behaviors, not code.

**Standard scroll reveal (applied to all sections):**
- Elements start invisible and slightly below their final position
- As they enter the viewport, they fade in and move up to their final position
- Duration: smooth, not snappy
- Easing: power2.out (decelerates, feels natural)

**Card groups (services, projects, testimonials):**
- Cards animate one after another with a short delay between each (stagger)
- Creates a cascading reveal effect as you scroll down

**Hero entrance (on page load, no scroll needed):**
- Elements appear in sequence: eyebrow label first, then headline line 1, then line 2, then sub-text, then buttons
- Each element fades up with a delay after the previous one
- Feels like the page is composing itself

**Hero background:**
- The animated hero background (Option A — grid lines) moves slowly and continuously
- Grid lines are fine, gold-tinted, very subtle — architectural blueprint feeling
- Gold corner brackets sit at top-left and bottom-right of the hero
- This is a CSS animation, not dependent on scroll

**Navigation:**
- On page load: transparent background, white text
- After scrolling 80px: white background, navy text, subtle shadow appears
- Smooth transition between both states

**Stats numbers:**
- Count up from zero to their final number when the stats bar scrolls into view
- Duration: approximately 2 seconds, eases out at the end

**About section:**
- Text block animates in from the left
- Image animates in from the right
- Both trigger when the section enters the viewport

---

# PART 2 — SITE STRUCTURE

Single scrollable page. Nine sections in this exact order:

1. Navigation
2. Hero
3. Stats Bar
4. Services
5. Projects
6. Testimonials
7. About
8. Contact
9. Footer

Navigation links scroll smoothly to each section anchor.

---

# PART 3 — SECTION CONTENT

---

## NAVIGATION

**Logo:** logo.png (KL Associate logo file)  
**Navigation links:** Home · Services · Projects · About · Contact  
**Call to action button (right side):** Get a Quote — links to Contact section  

**Behaviour:**
- Sticky — stays at top as user scrolls
- Transparent with white text when over the hero
- White background with navy text after scrolling past the hero
- Mobile: hamburger icon replaces the nav links, opens a full overlay menu

---

## HERO

**Background:** Deep navy (#051650) with an animated fine grid of gold-tinted lines moving slowly — like a living architectural blueprint. No photograph.

**Corner accents:** Thin gold lines forming bracket corners at top-left and bottom-right of the hero area.

**Eyebrow label (above headline):**
Chennai's Trusted Construction Partner

**Main Headline — two lines:**
Building Strength,
Delivering Excellence.

**Supporting text beneath headline:**
From industrial facilities to commercial landmarks — KL Associate engineers spaces that endure, with 30+ years of precision behind every project.

**Two buttons:**
- Primary button (gold, filled): View Our Work — links to Projects section
- Secondary button (outlined, white border): Get in Touch — links to Contact section

**Scroll indicator:** A small animated downward arrow at the bottom center of the hero, inviting the user to scroll

**Text colors in hero:**
- Eyebrow label: Gold (#C9963D)
- Headline: Near white (#F5FEFD)
- Supporting text: Near white at 60% opacity
- Buttons: as described

---

## STATS BAR

**Background:** Deep Navy (#051650)  
**Layout:** Three equal columns with thin vertical gold dividers between them

**Three stats — numbers in gold, labels in near-white:**

| Number | Label |
|--------|-------|
| 30+ | Years of Experience |
| 60+ | Projects Completed |
| 60+ | Satisfied Clients |

Numbers count up from zero when this section scrolls into view.

---

## SERVICES

**Section background:** Near White (#F5FEFD)

**Eyebrow label:** What We Build  
**Section heading:** Four Pillars of Our Craft  
**Section sub-copy:** Every structure we raise is a commitment — to quality, timeline, and the people who will use it.

**Layout:** 2×2 card grid on desktop, single column on mobile

---

**Card 1 — Residential Construction**

Icon: House / villa outline (SVG, inline)

Title: Residential Construction

Body:
From luxury villas to gated community homes, we bring precision and care to every residential project. Your home deserves a builder who treats it like their own.

---

**Card 2 — Commercial Construction**

Icon: Building / office outline (SVG, inline)

Title: Commercial Construction

Body:
Retail spaces, office complexes, commercial plazas — we build commercial environments that are functional, durable, and built to impress clients and customers alike.

---

**Card 3 — Industrial Construction**

Icon: Factory / industrial outline (SVG, inline)

Title: Industrial Construction

Body:
Manufacturing plants, MDMF facilities, research centers — we understand the exacting standards of industrial build-outs. Precision engineering, on time, every time.

---

**Card 4 — Renovation & Remodeling**

Icon: Tools / wrench outline (SVG, inline)

Title: Renovation & Remodeling

Body:
Breathing new life into existing structures. Whether it's an upgrade, an expansion, or a complete transformation — we renovate with the same rigor we build.

---

**Card hover behavior:**
- Left border becomes 3px solid gold
- Icon color shifts from navy to gold
- Card lifts with a soft shadow

---

## PROJECTS

**Section background:** Soft Mint (#EBF5F0)

**Eyebrow label:** Our Portfolio  
**Section heading:** Work That Speaks for Itself  
**Section sub-copy:** Ten projects across Chennai and Tamil Nadu — each one a benchmark we set for ourselves.

**Filter bar (above the project grid):**
All · Commercial · Industrial · Research · Residential

- Default active filter: All
- Active filter styling: gold underline, navy text
- Clicking a filter shows only matching cards, hides others
- Transition: smooth fade and slight movement

**Layout:** 3 columns desktop · 2 columns tablet · 1 column mobile

---

### Project Cards — Full List

Each card shows: project image, project name, type tag, location, and a status badge (Ongoing or Completed).

On hover: a dark navy overlay appears over the image with the project name in gold and the type in small caps beneath it.

---

**Project 1**
Image file: project-morrisons.jpg
Name: Morrisons
Type: Medical Device Manufacturing Factory
Filter category: Industrial
Location: SIPCOT Medical Devices Park, Oragadam
Year: 2025
Status: Ongoing

---

**Project 2**
Image file: project-vim-alloy.jpg
Name: VIM Alloy
Type: Factory
Filter category: Industrial
Location: Vallam
Year: 2025
Status: Completed

---

**Project 3**
Image file: project-brf2.jpg
Name: BRF 2
Type: Research Center
Filter category: Research
Location: Sendadu, Tiruvallur
Year: 2024–25
Status: Ongoing

---

**Project 4**
Image file: project-redia.jpg
Name: ReDia
Type: MDMF
Filter category: Industrial
Location: SIPCOT Medical Devices Park, Oragadam
Year: 2025–26
Status: Ongoing

---

**Project 5**
Image file: project-shriram-mart.jpg
Name: Shri Ram Mart
Type: Commercial Space
Filter category: Commercial
Location: Nolambur, Chennai
Year: 2021
Status: Completed

---

**Project 6**
Image file: project-bioscience.jpg
Name: Bioscience Research Foundation
Type: Research Center
Filter category: Research
Location: Sriperumbudur
Year: 2021–22
Status: Completed

---

**Project 7**
Image file: project-tirupathi.jpg
Name: Tirupathi House
Type: Villa
Filter category: Residential
Location: Tirupathi
Year: 2010–11
Status: Completed

---

**Project 8**
Image file: project-gesco.jpg
Name: GESCO
Type: MDMF
Filter category: Industrial
Location: SIPCOT Medical Devices Park, Oragadam
Year: 2025
Status: Ongoing

---

**Project 9**
Image file: project-church.jpg
Name: Church
Type: Church
Filter category: Commercial
Location: Sirkali, Chidambaram
Year: 2024–25
Status: Completed

---

**Project 10**
Image file: project-righttight.jpg
Name: Right Tight Fasteners Pvt Ltd
Type: Automobile Manufacturing
Filter category: Industrial
Location: Oragadam
Year: 2024–25
Status: Completed

---

**Status badge colors:**
- Ongoing: Gold (#C9963D) background with dark text
- Completed: Soft mint/green tone — subtle, not bright

---

## TESTIMONIALS

**Section background:** Deep Navy (#051650) — this is a full dark section for contrast

**Eyebrow label:** Client Stories  
**Section heading:** What Our Clients Say  
**Heading and label text color:** Near white (#F5FEFD)

**Layout:** 3 columns desktop · 1 column mobile

**Card style:** Navy card with a 3px gold left border, italic quote in Cormorant Garamond, gold stars, white attribution text at bottom.

---

**Testimonial 1**

Stars: ★★★★★

Quote:
"KL Associate delivered our manufacturing facility on time and within budget. Their site management and quality of work is something we've rarely seen from any contractor in Tamil Nadu."

Attribution: Project Director, Manufacturing Client

---

**Testimonial 2**

Stars: ★★★★★

Quote:
"From foundation to finish, they were transparent about every stage. No surprises, no shortcuts. We're already planning our next project with them."

Attribution: Business Owner, Commercial Client

---

**Testimonial 3**

Stars: ★★★★★

Quote:
"Our research center was a complex build with very specific requirements. KL Associate understood the brief and executed it with exceptional precision."

Attribution: Operations Head, Research Institution

---

## ABOUT

**Section background:** White (#FFFFFF)

**Layout:** Two columns on desktop — text on the left, image on the right. Stacked (text first, image second) on mobile.

**Eyebrow label:** About KL Associate  
**Section heading:** We Didn't Set Out to Just Build Buildings.

**Image file (right column):** about.jpg

---

**Opening line (immediately after heading, larger than body text):**
We set out to build better ones.

---

**Main body paragraph:**
KL Associate is a Chennai-based construction company with a reputation built the same way we build everything else — carefully, honestly, and without cutting corners.

From the ground up, we have worked on commercial and industrial projects across Chennai and beyond. But what defines us isn't the number of projects we've completed — it's the number of clients who came back for the next one.

---

**Sub-section: Who We Are**

Sub-heading: Who We Are

Body:
We are a team of engineers, site managers, and craftsmen who take construction personally. Every project that leaves our hands carries our name, and we treat that responsibility seriously. At KL Associate, there are no small projects — only projects that deserve our full attention.

---

**Sub-section: What We Believe**

Sub-heading: What We Believe

Body:
We believe that great construction is mostly invisible. The work that holds a structure together — the foundation, the framework, the finishing — is rarely what people see. But it's everything. That's where we obsess. That's where we refuse to compromise.

Timelines are commitments. Budgets are boundaries, not suggestions. Transparency isn't a policy here — it's just how we operate.

---

**Sub-section: Our Promise**

Sub-heading: Our Promise

Body:
When you work with KL Associate, you're not hiring a contractor. You're bringing in a partner who will treat your project with the same care we'd give our own. We sign every wall we build. And we make sure it's worth signing.

---

**Vision block (displayed as a distinct styled quote or highlighted paragraph at the bottom of the About section):**

Vision:
To redefine the built environment through timeless, sustainable, and innovative design and construction that inspires communities and enhances quality of life worldwide.

Mission:
To deliver innovative, sustainable, and high-quality construction solutions through excellence, integrity, and collaboration — creating lasting value for our clients and communities.

---

## CONTACT

**Section background:** Near White (#F5FEFD)

**Eyebrow label:** Let's Build Together  
**Section heading:** Start Your Project

**Layout:** Two columns — contact details on the left, contact form on the right. Stacked on mobile.

---

**Left column — Contact Details**

Address:
No. 415, MIG Ground Floor,
4th Cross Road,
Mogappair Eri Scheme,
Chennai — 600 037

Phone:
+91 98409 50949

Email:
klassociate6@gmail.com

LinkedIn:
linkedin.com/company/kl-associate
(opens in a new tab)

---

**Right column — Contact Form**

Field 1: Full Name — text input, required  
Field 2: Email Address — email input, required  
Field 3: Phone Number — tel input, optional  
Field 4: Project Type — dropdown, options are: Residential / Commercial / Industrial / Renovation / Other  
Field 5: Message / Project Brief — textarea, 4 rows tall, optional  

Submit button text: Send Enquiry  
Submit button style: Gold filled (#C9963D), full width, 2px border radius

**Form input style:**
- Bottom border only — no full box border around fields
- Default state: 1px navy bottom border
- Focused state: 2px gold bottom border
- Labels float above the field when focused or filled
- No border radius on input fields — sharp, architectural

**After successful submission:**
A message appears inline below the form:
"Thank you! We'll be in touch within 24 hours."
The page does not reload.

---

## FOOTER

**Background:** Deep Navy (#051650)  
**Text color:** Near White (#F5FEFD)

**Layout — three columns:**

Left column:
- KL Associate logo (logo.png)
- Tagline beneath logo: Building Strength, Delivering Excellence

Center column — navigation links (same as header):
- Home
- Services
- Projects
- About
- Contact

Right column — contact snapshot:
- +91 98409 50949
- klassociate6@gmail.com
- Chennai, Tamil Nadu

**Bottom bar (full width, below the three columns):**
- Left: © 2025 KL Associate. All rights reserved.
- Right: LinkedIn icon (SVG inline) linking to https://www.linkedin.com/company/kl-associate/

---

# PART 4 — IMAGE FILES REFERENCE

All images live in the images/ folder alongside index.html.

| File Name | Used In | Notes |
|-----------|---------|-------|
| logo.png | Navigation, Footer | KL Associate logo on navy and white backgrounds |
| about.jpg | About section, right column | Site or team photograph |
| project-morrisons.jpg | Projects grid | Morrisons — SIPCOT Oragadam |
| project-vim-alloy.jpg | Projects grid | VIM Alloy — Vallam |
| project-brf2.jpg | Projects grid | BRF 2 — Sendadu, Tiruvallur |
| project-redia.jpg | Projects grid | ReDia — SIPCOT Oragadam |
| project-shriram-mart.jpg | Projects grid | Shri Ram Mart — Nolambur |
| project-bioscience.jpg | Projects grid | Bioscience Research Foundation — Sriperumbudur |
| project-tirupathi.jpg | Projects grid | Tirupathi House — Tirupathi |
| project-gesco.jpg | Projects grid | GESCO — SIPCOT Oragadam |
| project-church.jpg | Projects grid | Church — Sirkali, Chidambaram |
| project-righttight.jpg | Projects grid | Right Tight Fasteners — Oragadam |

---

# PART 5 — MOBILE BEHAVIOR

Every section adapts to mobile screens (below 768px):

- Navigation collapses to a hamburger icon. Tapping it opens a full-screen overlay with the nav links centered and large.
- Hero text scales down. Both buttons stack vertically.
- Stats bar: three stats stack vertically instead of side by side.
- Services grid: 2×2 becomes a single column, one card at a time.
- Projects grid: 3 columns → 2 columns (tablet) → 1 column (mobile).
- Testimonials: 3 columns → 1 column.
- About: side-by-side → text on top, image below.
- Contact: side-by-side → details on top, form below.
- Footer: 3 columns → stacked, centered.

---

*KL Associate — Content Document · Prepared May 2025*
