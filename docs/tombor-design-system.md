Tombor Studio HTML/CSS Convention

HTML structure:
- Use semantic structure: <nav> → <main> → repeated <section> blocks → <footer>.
- Each major section uses:
  <section>
      <div class="container" id="section-name">
          ...
      </div>
  </section>
- .container is the shared layout wrapper.
- IDs are used for unique page sections.
- Classes are used for reusable components.

CSS file system:
1. styles.css
   - Global brand/theme styles.
   - Fonts, body defaults, color palette, nav link visuals, footer visuals.

2. layout.css
   - Shared layout structure.
   - Nav layout, containers, cards, CTA layout, footer layout, responsive breakpoints.

3. page-name.css
   - Page-specific styling only.
   - Example: about.css, contact.css, home.css.

Font system:
- Primary font: "Neue Haas", sans-serif.
- Display/accent font available: "Riant Display".
- Body uses Neue Haas.
- Large headings commonly use very oversized type:
  - Hero/subpage headings: 400%–1000%.
  - Section headings: 300%–500%.
  - Card headings: around 250%.

Color palette:
- Cream background: #F1EDE8
- Dark charcoal: #2B2B2B
- Muted tan: #DCD3C4
- Orange/red accent: #D86044
- Dark gray footer/support text: #4A4A4A
- Muted gray: #747474
- White: #FFFFFF

Visual style:
- Minimal, Swiss-inspired, structured, bold typography.
- Strong contrast between cream, charcoal, tan, and orange/red.
- Frequent use of underline links and thick borders.
- Large typographic hierarchy.
- Clean rectangular sections.
- Mostly flexbox-based layouts.

Layout conventions:
- Use flexbox heavily:
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column/row;
- Use .container as the base wrapper.
- Use section IDs to control unique spacing, colors, and layout.
- Cards use .card with fixed/controlled width, centered content, and strong background color blocks.
- CTA sections often use centered headings, underline styling, icons, and .container-stamp.
- Footer is split into:
  #upper-footer
  #lower-footer

Reusable classes:
- .container = shared section wrapper.
- .card = reusable service/card block.
- .container-stamp = horizontal brand stamp/footer-like divider.
- .orange-link = orange/red accent link.
- .icons = small icon sizing.
- .navLinks = nav link styling.
- .logo-nav = logo sizing/spacing.

Responsive conventions:
- layout.css handles global responsiveness.
- Tablet breakpoint: max-width 1024px.
- Mobile breakpoint: max-width 768px.
- Contact page has an additional form breakpoint at max-width 700px.
- Responsive behavior usually changes rows into stacked columns, reduces heading sizes, adds padding, and allows cards to wrap.

Naming convention:
- Global reusable classes use lowercase/kebab or simple names:
  .container, .card, .orange-link, .container-stamp
- Unique page sections use IDs:
  #hero-container
  #CTA-header
  #about-intro
  #contact-form-container
  #portfolio-grid
- Current style is hybrid:
  semantic HTML + containerized layout + page-scoped IDs + reusable components.

Important cleanup rule:
- Do not duplicate rules between styles.css and page CSS.
- styles.css should stay global.
- layout.css should stay structural.
- page CSS should only style that page’s unique sections.