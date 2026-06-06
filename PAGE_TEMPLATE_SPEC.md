# PAGE TEMPLATE SPEC

Source: refrigerator-repair.html

Purpose
-------
This document defines a reusable static HTML page template for service, brand, and city pages. It describes the exact, repeatable HTML structure for each section, required classes and attributes, SEO and schema requirements, and rules for content replacement (content-only changes, no layout changes).

Usage
-----
- Use this spec to generate all service pages (e.g., /refrigerator-repair), brand pages (e.g., /samsung-appliance-repair), and city/location pages (e.g., /phoenix-appliance-repair).
- Do not modify classes, element types, or structure — only replace the textual content, URLs, and small attributes explicitly permitted below.
- Keep pages static (no client-side includes required). Include shared stylesheet at /assets/css/style.css.

Global rules (must follow)
-------------------------
- Include the shared stylesheet in the <head>:

  <link rel="stylesheet" href="/assets/css/style.css">

- Title tag: unique, includes primary keyword and city/area when relevant.
- Meta description: unique, 120–155 chars recommended, includes primary keyword and phone CTA mention.
- H1: unique, contains the primary keyword and city when applicable (exact H1 required per page type).
- Internal links: 3–10 links per page minimum (mix of service, brand, city, homepage). Must not be empty.
- Primary phone number: (602) 499-7053 must appear in header, hero CTA, CTA section, and footer; phone link should use tel:+16024997053.
- CTAs: place at least one CTA above the fold (hero) and one CTA every 1–2 sections.
- Word counts: target 800–1800 words per page; at minimum 800 words for service/city pages.
- Accessibility: semantic HTML, ARIA where appropriate, focusable FAQ questions.
- Performance: keep markup simple, lazy-load large images, use WebP where possible.

Template sections
-----------------
The template is composed of the following sections. Each section lists the exact HTML skeleton, required classes, and notes on content replacement.

1) Header (shared)
------------------
Place this at the top of every page. Keep structure and classes exactly as shown.

HTML:

<header>
  <div class="container header-inner">
	<div class="logo">AZ Freeze</div>
	<nav class="nav" aria-label="Main navigation">
	  <a href="/">Home</a>
	  <a href="/refrigerator-repair">Services</a>
	  <a href="/samsung-appliance-repair">Brands</a>
	  <a href="/phoenix-appliance-repair">Locations</a>
	</nav>
	<a class="phone-cta" href="tel:+16024997053">(602) 499-7053</a>
  </div>
</header>

Notes:
- Do NOT change element tags or classes. You may modify nav link URLs/text to suit the generated page, but keep the nav element present.

2) Hero
--------
Purpose: top-of-page conversion. Must contain H1 exactly as required by CONTENT_GUIDELINES.

HTML skeleton:

<section class="hero">
  <div class="container hero-grid">
	<div class="hero-copy">
	  <h1><!-- REPLACE: H1 text (primary keyword + city if applicable) --></h1>
	  <p class="lead"><!-- REPLACE: short intro (1–2 sentences) with primary keyword in first paragraph --></p>
	  <div class="hero-actions">
		<a class="btn btn-primary" href="tel:+16024997053">Call Now (602) 499-7053</a>
		<a class="btn btn-secondary" href="/request-service">Request Service</a>
	  </div>
	</div>
	<div class="hero-visual" aria-hidden="true"></div>
  </div>
</section>

Notes:
- H1 must be unique per page (e.g., "Refrigerator Repair in Phoenix AZ").
- The first paragraph must include the primary keyword.
- Do not change class names or structure.

3) Common Problems
------------------
Purpose: list typical issues for the service; short bullets help SEO and scannability.

HTML skeleton:

<section>
  <div class="container">
	<div class="section-title">Common [Service] Problems</div>
	<div class="card">
	  <ul>
		<li><!-- problem 1 --></li>
		<li><!-- problem 2 --></li>
		<li><!-- problem 3 --></li>
		<!-- add more list items as relevant -->
	  </ul>
	  <div style="margin-top:12px"><a class="btn btn-primary" href="tel:+16024997053">Call for Fast Diagnosis</a></div>
	</div>
  </div>
</section>

Notes:
- Use 5–10 bullet items. Keep short phrases (3–8 words) describing the problem.

4) Brands We Service
--------------------
Purpose: link to brand pages; each brand must link to its brand page.

HTML skeleton:

<section>
  <div class="container">
	<div class="section-title">Brands We Service</div>
	<p class="lead"><!-- REPLACE: 1–2 sentence explanation of brand expertise --></p>
	<div class="brands">
	  <a class="brand" href="/samsung-appliance-repair">Samsung</a>
	  <a class="brand" href="/lg-appliance-repair">LG</a>
	  <a class="brand" href="/whirlpool-appliance-repair">Whirlpool</a>
	  <a class="brand" href="/ge-appliance-repair">GE</a>
	  <a class="brand" href="/frigidaire-appliance-repair">Frigidaire</a>
	  <a class="brand" href="/bosch-appliance-repair">Bosch</a>
	  <a class="brand" href="/viking-appliance-repair">Viking</a>
	</div>
	<div style="margin-top:12px"><a class="btn btn-secondary" href="/samsung-appliance-repair">Learn More About Brand Repairs</a></div>
  </div>
</section>

Notes:
- Keep brand link order consistent across pages.

5) Repair Process
-----------------
Purpose: explain step-by-step how repairs are performed (builds trust and conversion).

HTML skeleton:

<section>
  <div class="container">
	<div class="section-title">Our [Service] Repair Process</div>
	<div class="card">
	  <ol>
		<li><strong>Schedule:</strong> <!-- REPLACE: short description --></li>
		<li><strong>Inspection:</strong> <!-- REPLACE: short description --></li>
		<li><strong>Estimate:</strong> <!-- REPLACE: short description --></li>
		<li><strong>Repair:</strong> <!-- REPLACE: short description --></li>
		<li><strong>Guarantee:</strong> <!-- REPLACE: short description --></li>
	  </ol>
	  <div style="margin-top:12px"><a class="btn btn-primary" href="tel:+16024997053">Schedule [Service] Repair</a></div>
	</div>
  </div>
</section>

Notes:
- Replace bracketed [Service] with the page's service name.
- Keep the 5-step flow structure for consistency across service pages.

6) Trust Signals
----------------
Purpose: short list of trust-building points (same-day, warranty, trained technicians).

HTML skeleton:

<section>
  <div class="container">
	<div class="section-title">Trust & Guarantees</div>
	<div class="card">
	  <ul>
		<li>Same-day service options in [City] when available</li>
		<li>Technicians background-checked and trained</li>
		<li>Transparent pricing and written estimates</li>
		<li>Parts & labor warranty on repairs</li>
		<li>Locally owned business serving the East Valley</li>
	  </ul>
	</div>
  </div>
</section>

Notes:
- Replace [City] only on city-specific pages; for service or brand pages the phrase can remain generic (e.g., "in Phoenix and the East Valley").

7) FAQ
------
Purpose: provide at least 5 relevant questions and answers; include FAQ JSON-LD for search engines (embedded in page).

HTML skeleton (visible content):

<section>
  <div class="container">
	<div class="section-title">Frequently Asked Questions</div>
	<div class="faq">
	  <div class="faq-item">
		<div class="faq-question">Question 1?</div>
		<div class="faq-answer">Answer 1.</div>
	  </div>
	  <!-- Repeat at least 5 faq-item blocks -->
	</div>
	<div style="margin-top:12px"><a class="btn btn-primary" href="tel:+16024997053">Speak With A Technician</a></div>
  </div>
</section>

Structured data JSON-LD (include after the visible FAQ, in the page bottom):

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"FAQPage",
  "mainEntity":[
	{"@type":"Question","name":"Question 1?","acceptedAnswer":{"@type":"Answer","text":"Answer 1."}},
	// ... at least 5 items
  ]
}
</script>

Notes:
- FAQ content must be relevant to the page type (service, brand, or city).
- At least 5 Q&A pairs are required. Keep questions concise and answers 1–3 sentences.

8) CTA (Final strong CTA)
-------------------------
Purpose: final conversion area with phone and request-service options.

HTML skeleton:

<section>
  <div class="container">
	<div class="card" style="text-align:center">
	  <h2><!-- REPLACE: final CTA heading --></h2>
	  <p><!-- REPLACE: final CTA supporting sentence --></p>
	  <div style="display:flex;justify-content:center;gap:12px;flex-wrap:wrap;margin-top:12px">
		<a class="btn btn-primary" href="tel:+16024997053">Call Now</a>
		<a class="btn btn-secondary" href="/request-service">Request Service</a>
	  </div>
	</div>
  </div>
</section>

Notes:
- CTA heading and paragraph must be unique and action-oriented.

Footer (shared)
---------------
Keep footer structure exactly consistent across pages. Example:

<footer>
  <div class="container footer-grid">
	<div style="display:flex;justify-content:space-between;align-items:start;gap:12px;flex-wrap:wrap">
	  <div>
		<div style="font-weight:800;font-size:18px">AZ Freeze Appliance Repair</div>
		<div style="margin-top:6px">Phone: <a href="tel:+16024997053">(602) 499-7053</a></div>
	  </div>
	  <!-- services list and city links -->
	</div>
	<div style="opacity:0.9;font-size:13px">© <span id="year"></span> AZ Freeze Appliance Repair — <a href="/privacy">Privacy</a></div>
  </div>
</footer>

SEO and schema rules
--------------------
- Each page must include LocalBusiness JSON-LD in the page <body> (homepage and all pages). Example:

  <script type="application/ld+json">{ "@context":"https://schema.org", "@type":"LocalBusiness", "name":"AZ Freeze Appliance Repair", "telephone":"+1-602-499-7053", "areaServed":["Phoenix","Tempe","Mesa","Chandler","Gilbert","Scottsdale"] }</script>

- Service pages must include a Service JSON-LD describing the serviceType and provider.
- FAQ JSON-LD must reflect the visible FAQ content and be embedded in the static HTML (no JS generation required).

Content replacement rules (strict)
--------------------------------
- Allowed changes per page generation:
  - Replace title, meta description, and H1 text.
  - Replace textual content inside paragraphs, list items, and FAQ answers/questions.
  - Replace internal href targets (nav links, brand/service/city links) to point to the correct pages.
  - Replace service names inside repeated strings (e.g., "Schedule Refrigerator Repair") to match the page service.
  - Replace city names in copy on city pages only.

- Forbidden changes (do NOT modify):
  - Do not change HTML element tags (for example, do not change <div> to <section> in the template structure).
  - Do not rename or remove CSS class names (e.g., .hero, .card, .btn-primary).
  - Do not alter the order of sections unless page type requires it and approved.
  - Do not move or remove JSON-LD blocks unless replacing with equivalent structured data.

Generation checklist (for each generated page)
-------------------------------------------
1. Ensure <title>, <meta description>, and <h1> are unique and contain primary keyword.
2. Ensure internal links: link to homepage, 3–6 service pages, 2–4 brand pages, and 1–3 city pages where relevant.
3. Confirm CTA buttons use tel:+16024997053 and visible phone number text (602) 499-7053.
4. Provide at least 800 words of unique content for service and city pages; brand pages should be 600+ words recommended.
5. Include LocalBusiness JSON-LD and Service JSON-LD (for service pages), plus FAQ JSON-LD.

Examples and notes
------------------
- Service page H1 example: Refrigerator Repair in Phoenix AZ
- Brand page H1 example: Samsung Appliance Repair — Phoenix & East Valley
- City page H1 example: Phoenix Appliance Repair

Maintenance
-----------
- Keep this PAGE TEMPLATE SPEC in the repository root and update when any layout or design system changes are made.
- If you extract to a static site generator later (recommended), map each template section to a partial or component and keep the semantics and class names identical.

Contact
-------
For questions about the template or if a page requires a layout change, open an issue and tag the maintainers.
