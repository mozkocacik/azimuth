# Azimuth brand book

Azimuth is the corporate system for established electronics manufacturers. Their customers plan with a product for ten years or more, and purchasing, quality, engineering, investors and applicants all use the same site. The design shows the same stability: it changes slowly, it documents everything and it never needs to impress. For growing companies, use Meridian. App screens use Solaris; developer tools use Vesper.

## Principles

1. **Continuity.** Layouts and navigation stay the same across years and product generations. A customer who used the site in 2020 finds the same places in 2030.
2. **Traceability.** Every document, notice and product record shows its number, revision, date and owner. The TitleBlock makes this visible.
3. **Restraint.** One brand color, sentence case, square surfaces, no decorative motion. The company speaks through facts, certifications and documents.
4. **Access by role.** Visitors, registered customers and partners see different content. The access level of each item is shown before the click.

## Differences from Meridian

| Topic | Meridian | Azimuth |
| --- | --- | --- |
| Audience | Growing companies, engineers who evaluate a product | Established groups, purchasing, quality and engineering departments |
| Typeface | Instrument Sans, tight tracking | Source Sans 3, normal tracking |
| Largest heading | 64px, weight 560 | 46px on the cover, 40px on pages, weight 600 |
| Brand color | Accent, only as a signal | Brand, also for the primary action and links |
| Primary button | Graphite | Brand |
| Radius | 2 to 8px | 0 on surfaces, 2px on controls |
| Navigation | One header bar | Utility bar, main bar, mega menu with category rail, local navigation |
| Signature element | Annotation | TitleBlock |
| Motion | Hover and state changes | Feedback only, 100ms |

## Content fundamentals

- The voice is formal, precise and calm. Write in the third person for the company ("Acme supplies the CGW-4 until at least 2036") and in the second person for instructions.
- Name the legal entity in contracts, consent texts and the footer: "Acme Electronics GmbH".
- Sentence case everywhere. No exclamation marks, no superlatives ("best-in-class"), no casual phrases ("Let's talk", "We've got you covered").
- Use the fixed lifecycle words: In development, Active, Not for new designs, Discontinued.
- Dates are ISO 8601. Document numbers carry the revision: "DS-0412-001 Rev C".
- Facts carry their source: "Certified to IATF 16949 since 2004", "Revenue, fiscal year 2025".
- Acme and its products are sample content.

## Visual foundations

**Color.** Neutral greys carry the page. The brand color (navy by default) marks the primary action, links, the selected tab and active markers. Status colors are for status only. A typical page is 68% `canvas`, 20% `panel`, 8% `band`, 3% brand and 1% status. Brand above 10% makes the page look like an advertisement.

**Themes.** Light is the reference. Dark uses `canvas` #0c1117, a lighter `link` tint and lighter status colors so all text stays at 4.5:1 or more; the brand fill stays dark enough for a white label. The `band` (utility bar, cover, footer) is the same in both themes. With no `data-theme`, follow the system setting.

**Type.** Source Sans 3 for all text and Source Code Pro for numbers, codes and dates. Headings use weight 600, normal tracking and sentence case. Labels are never uppercase. Use the styles in `tokens.css`: `cover-title`, `h1` to `h5`, `lead`, `body`, `small`, `caption`, `label`, `fact` and `data`.

**Layout.** Three page templates:
- **T1 Overview:** PageHeader, then content in 12 columns. Category pages, company pages, home.
- **T2 Detail:** LocalNav (2 columns), content (7), ContactRail (3). Product pages, notices, application notes.
- **T3 Data:** toolbar and a full-width table. Product finder, DownloadCenter, distributor list.

Content is at most 1320px wide. Grid: 4 columns below 600px (16px gutter and margin), 8 columns to 1099px (24px gutter, 32px margin), 12 columns above (24px gutter, 40px margin; 32px gutter from 1440px).

**Shape.** Surfaces are square (`r-0`). Buttons and inputs have `r-1` (2px). Round shapes only for radio buttons and timeline points.

**Borders and shadows.** Structure comes from grey panels and 1px rules. Inputs, frames and title block cells use `border-strong`. Only the mega menu, dialogs and the cookie consent float (`shadow-menu`).

**Imagery.** Photos of real plants, products and people at work, in natural light. No illustrations of abstract shapes. Product images on a neutral ground.

**States.** Hover darkens the brand fill or adds `subtle`. Focus is a 2px `focus` ring with a 2px offset. Disabled uses `muted` and `text-3`.

**Motion.** A 100ms color change on hover and press. Nothing moves on scroll. Respect reduced motion.

## Iconography

Lucide, stroke 1.75, round caps and joins, `currentColor`. 18px in content, 16px in buttons and tables, 20px in the main bar. Use icons for navigation, downloads, contact data, locks and alerts only.

## Page structure

A product page (T2): GlobalHeader, PageHeader, then LocalNav, content and ContactRail. Content order: lead, MasterData, Lifecycle, Notice (if any), technical data, downloads (DownloadCenter rows for this product), TitleBlock for the datasheet. Then Footer. The ProductPage card shows it.

A company page (T1): GlobalHeader, PageHeader, KeyFacts, PressList, Footer.

Every page: ConsentBanner on the first visit, Footer with the legal block.

## Accessibility

WCAG 2.2 AA is the minimum; the European Accessibility Act makes it a legal duty for many company sites in the EU. Every text token passes 4.5:1 on the surfaces its usage note names, in both themes. `border-strong` and the focus ring pass 3:1. Body text is 16px or larger. Touch targets are 40px or more; 32px buttons are for pointer areas such as table toolbars. Status and access levels are never shown by color alone.
