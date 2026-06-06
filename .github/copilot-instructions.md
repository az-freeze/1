.github/copilot-instructions.md

AZ Freeze Appliance Repair — Copilot System Instructions

CRITICAL RULE

You are working inside a structured web project.

Before generating ANY code, page, component, or content, you MUST treat the project documentation as mandatory system context.

You MUST follow all rules in this repository as if they are system-level instructions.

---

REQUIRED PROJECT FILES (READ FIRST)

Whenever you generate or modify code, you MUST follow and apply the rules from ALL of the following files:

- PROJECT_CONTEXT.md
  (Business goals, SEO strategy, conversion rules)

- SITE_MAP.md
  (Full website structure, pages, sections, and navigation)

- DESIGN_SYSTEM.md
  (UI design system, colors, typography, spacing, components)

- CONTENT_GUIDELINES.md
  (Writing style, SEO content rules, tone, conversion logic)

---

FILE PRIORITY ORDER (IMPORTANT)

If there is any conflict between files, use this priority:

1. CONTENT_GUIDELINES.md (content + SEO + conversion rules)
2. PROJECT_CONTEXT.md (business + SEO strategy)
3. SITE_MAP.md (structure and pages)
4. DESIGN_SYSTEM.md (visual design system)

---

GLOBAL PROJECT GOAL

This website is designed to:

- Generate phone calls
- Generate service requests
- Rank in Google local search (Arizona)
- Build trust for appliance repair services

Primary conversion = PHONE CALL

---

SEO REQUIREMENTS (MANDATORY)

Every page MUST:

- Be unique (no duplicate content)
- Have unique:
  - Title tag
  - Meta description
  - H1
- Follow local SEO structure
- Include internal links (3–10 per page)
- Use semantic HTML

Target areas:

Phoenix, Tempe, Mesa, Chandler, Gilbert, Scottsdale

---

PAGE GENERATION RULES

When creating any page:

You MUST follow SITE_MAP.md structure exactly.

Do NOT invent new pages unless explicitly requested.

Each page MUST include:

- Hero section
- Service explanation
- Trust signals
- FAQ section
- CTA section (Call Now)
- Footer CTA

---

DESIGN RULES

You MUST follow DESIGN_SYSTEM.md exactly.

Rules:

- No random colors
- No external UI frameworks (unless explicitly requested)
- Mobile-first layout
- Clean and modern UI
- Fast loading design
- Accessible HTML structure

---

CONTENT RULES

You MUST follow CONTENT_GUIDELINES.md exactly.

Rules:

- Clear, human-readable English
- No keyword stuffing
- No exaggerated marketing claims
- Short paragraphs
- Conversion-focused writing

Tone:

- Professional
- Local business
- Trustworthy
- Simple and direct

---

CONVERSION RULES (VERY IMPORTANT)

Every page MUST prioritize:

1. Phone call button visibility above the fold
2. Click-to-call on mobile
3. Multiple CTAs per page (every 1–2 sections)
4. Trust signals (same-day service, experienced technician, etc.)

---

INTERNAL LINKING RULES

Every page MUST include links to:

- Related service pages
- Relevant city pages
- Relevant brand pages
- Homepage

No orphan pages allowed.

---

TECHNICAL RULES

- Use only HTML5, CSS3, Vanilla JavaScript
- No heavy frameworks
- No unnecessary dependencies
- Optimize for PageSpeed 90+
- Use semantic HTML tags
- Use clean folder structure

---

AUTOMATION BEHAVIOR RULE

Before generating ANY output, you MUST:

1. Check SITE_MAP.md for page structure
2. Check DESIGN_SYSTEM.md for styling rules
3. Check PROJECT_CONTEXT.md for SEO + business logic
4. Check CONTENT_GUIDELINES.md for writing rules

If any required rule is missing, assume it is MANDATORY anyway.

---

DO NOT

- Do not create random pages outside SITE_MAP
- Do not break design system
- Do not duplicate content between pages
- Do not ignore SEO rules
- Do not ignore conversion rules
- Do not skip internal linking

---

FINAL GOAL

Everything you generate must behave like a real production website built by a senior SEO + frontend team.

The result must be:

- SEO optimized
- Conversion focused
- Clean and structured
- Consistent across all pages
- Ready for deployment