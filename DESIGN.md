# TEICA Design System — Classic Institute

**Chosen direction (June 2026):** Classic Institute

User feedback: "I really like the classic institute theme/style"

**The word is classic institute.** 

Full rollout complete for main site pages:
- index.html, starting-guide.html, resources.html, faq.html, skills-tools.html, community-assessment.html, health.html, quickstart.html, FIRST_30_DAYS.html, BAY_AREA_GUIDE.html, governance.html all now use:
  - bg #f8f1e3 cream
  - text #1e2937 dark
  - primary #14532d deep green
  - accent #b48c5e gold
  - fonts EB Garamond (display) + Instrument Sans (body)

**Logo block finalized (3 lines):**

TEICA
TECHNIQUECOLOGICAL INSTITUTE
OF CALIFORNIA

- No "THE "
- TEICA (line 1) has `-mt-px mb-[2px]` — slightly raised relative to the logo mark + adds a little space above line 2.
- Second line (TECHNIQUECOLOGICAL INSTITUTE) uses `-mt-2` to relieve crowding between line 2 and line 3.
- Third line uses `-mt-px` for tight but uncrowded pairing with line 2.
- Font: text-[8px] tracking-[0.5px] on subtitle lines.
- Stacked `flex flex-col leading-none`
- Uniformly applied to all main pages.
- logo.svg in root for reuse.

Say the word.

This aesthetic balances established institutional credibility with warm, California-specific humanity. It feels serious, trustworthy, and rooted in tradition while remaining practical and approachable.

## Core Tokens

**Colors**
- Primary Green (Deep Forest): #14532d
- Accent Gold (California Gold): #b48c5e
- Cream / Warm Off-White: #f8f1e3
- Text: #1e2937
- Muted Text: #475569 / #64748b
- Borders: #e2d9c9

**Typography**
- Display / Headings: EB Garamond (serif, 400–600)
- Body: Instrument Sans (sans, 400–600)
- Generous line-height and tracking for elegance

**Logo**
The refined circular seal (inline SVG):
- Outer circle in Deep Forest
- Stylized leaf/technique path
- Small accent in Gold

**Spacing & Components**
- Generous margins
- Cards with subtle borders and hover lift
- Rounded corners (xl on buttons and cards)
- Clean nav with light background, no fixed dark overlay

## Implementation Notes

- All public HTML pages use Tailwind CDN + the custom style block for consistency.
- Hero uses large serif display type for impact.
- Primary CTAs: deep green buttons; secondary: gold-bordered.
- Backgrounds are cream or white for a warm, paper-like, institutional feel.

## Current Status (June 2026)
**Full rollout complete** for the main public site:

- index.html, starting-guide.html, resources.html, faq.html, skills-tools.html, health.html, governance.html, quickstart.html, community-assessment.html, BAY_AREA_GUIDE.html, FIRST_30_DAYS.html
- Consistent classic institute aesthetic across all of them
- Final 3-line logo block locked and uniformly applied (see below)
- DESIGN.md is current

`designs/` contains historical aesthetic explorations (preserved for reference; not part of the live site).

`logo.svg` committed as the reference seal.

## Canonical Logo / Header Block
Because this is a pure static site, the header is currently duplicated. When creating or editing pages, copy this exact structure for the brand area:

```html
<div class="flex items-center gap-3">
  <div class="logo-mark">
    <svg viewBox="0 0 48 48" ...> ... </svg>
  </div>
  <div class="flex flex-col leading-none">
    <a href="./index.html" class="font-display text-2xl tracking-tight font-semibold teica-green -mt-px mb-[2px]">TEICA</a>
    <div class="text-[8px] -mt-2 tracking-[0.5px] text-[#b48c5e] font-medium hidden lg:block">TECHNIQUECOLOGICAL INSTITUTE</div>
    <div class="text-[8px] -mt-px tracking-[0.5px] text-[#b48c5e] font-medium hidden lg:block">OF CALIFORNIA</div>
  </div>
</div>
```

(The rest of the nav + CTAs follow the established pattern in index.html.)

## Next Steps (low-hanging / stabilization)
- Minor doc hygiene and CTA consistency across pages
- Optional: GitHub Pages / easy live view setup
- Prepare clean base before next content or feature tangent
- (Later) evaluate whether to extract a tiny include or build step if duplication becomes painful

Refine copy tone toward institute voice on an as-needed basis as content evolves.

This direction best supports the long-term reputation we want as an institute focused on technique, character, and stewardship.