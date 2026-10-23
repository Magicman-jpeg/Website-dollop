# Public-Site Pattern Library

Accessed: 2026-10-06. Re-checked: 2026-10-23. Public sites can change; re-check the live page before applying a pattern. These notes are original summaries of observable patterns. They are not copied style guides, markup, assets, palettes, or compositions.

**2026-10-23 re-check summary.** Live re-inspection confirmed the patterns below are still accurate at the recorded URLs:
- **James Magpantay** — still proof-first: role/positioning, education, projects-with-outcomes, certifications roadmap, and a professional summary, in that order.
- **Thomas Monavon** — still one-project-at-a-time with explicit scroll-driven open/close transitions ("scroll up/down to close", a `00%` progress counter per project). Strongest reference for a deliberate, progress-aware page transition.
- **Cyd Stumpel** — still an editorial, GSAP-driven identity that uses an explicit "turn card" flip interaction and foregrounds accessibility. Reinforces that a literal turn gesture can be tasteful *and* accessible.
- **Exo Ape** — redirects to `www.exoape.com`; cinematic, media-led, sparse navigation (unchanged in principle).

## Personal portfolio patterns

### James Magpantay — recruiter utility plus personality
Source: [jamesmagpantay.com](https://www.jamesmagpantay.com/)

**Observed:** Long-form professional profile; sharp cybersecurity positioning; early credentials and resume actions; projects emphasize outcomes; certifications communicate progression; optional personal/off-the-clock content and playful interface elements add personality.

**Transferable:** Make professional positioning and proof immediately scannable, then reveal personality as an optional layer. Interaction should reinforce the candidate's field.

**Use here:** Keep Jay's target role, strongest project, credentials, availability, and contact obvious. Treat community breadth and ASCII/CRT personality as supporting—not competing—information.

**Do not copy:** Its mode switch, mascot, exact project sequence, visual treatment, wording, or interactive choreography.

### Thomas Monavon — curated project drama
Source: [thomasmonavon.com](https://www.thomasmonavon.com/)

**Observed:** Minimal navigation; one project dominates at a time; extreme scale contrast and whitespace; spatial, scroll-driven media transitions; metadata is subordinate to the showcased work.

**Transferable:** Curate instead of cataloging. One dominant project and deliberate absence can carry more authority than many equal cards.

**Use here:** Give only a finished, publicly defensible project the featured treatment. Preserve a semantic project list and calm reduced-motion path.

**Do not copy:** Its reel mechanics, viewport composition, media choreography, project numbering treatment, or exact typography.

### Cyd Stumpel — editorial personality with usable structure
Source: [cydstumpel.nl](https://cydstumpel.nl/)

**Observed:** Strong variable-type identity, editorial collage, multiple professional roles, clear availability/contact information, projects and writing, playful interactions, and stronger semantic/accessibility signals than many experimental portfolios.

**Transferable:** A consistent identity system can unite technical work, speaking, leadership, and personality. Progressive enhancement lets expressive motion sit on top of usable content.

**Use here:** Let one visual language connect cloud/software work and community leadership; keep skip links, landmarks, labels, and readable copy intact.

**Do not copy:** Portrait collage, badges, marquee treatment, illustrations, exact layout, or interaction details.

## Studio and agency patterns

### Junni — one repeated brand behavior
Source: [junni.co.jp](https://junni.co.jp/)

**Observed:** Immersive tiled hero, monumental identity typography, recurring kinetic headings, compact functional copy, and a consistent experimental-digital motif.

**Transferable:** Choose one repeatable visual behavior to carry identity across the site; pair expressive display moments with restrained body content.

**Use here:** If ASCII remains the identity behavior, consolidate it into a few purposeful roles instead of adding unrelated decoration.

**Do not copy:** Tile field, character animation, Japanese visual identity, exact typography, or marquee behavior.

### New Layer Capital / Obys — thesis as a framing system
Source: [nlc.obys.agency](https://nlc.obys.agency/)

**Observed:** A layered outer frame reinforces the brand idea; numbered editorial narrative; rules, labels, metrics, and audience-specific calls to action organize dense information.

**Transferable:** Turn a real strategic idea into the page frame. Use metadata and rules to make evidence navigable.

**Use here:** A restrained terminal/file metaphor may frame Jay's learning path, but proof and contact must remain clearer than the effect.

**Do not copy:** Nested frame geometry, central landscape, exact numbered narrative, typography, or palette.

### Exo Ape — cinematic proof with sparse navigation
Source: [exoape.com](https://exoape.com/)

**Observed:** Full-bleed media, a small route set, oversized transition typography, and a short image/video-led narrative.

**Transferable:** When work is visual, a few high-quality moments can replace many interface components. Copy should orient rather than compete.

**Use here:** Only adopt cinematic media if Jay has strong original assets. Never use spectacle to mask thin or unfinished project evidence.

**Do not copy:** Media assets, cursor, transition choreography, layout, type, or project presentation.

### THE LINE — craft vocabulary as interface language
Source: [thelinestudio.com](https://thelinestudio.com/)

**Observed:** Animation-first hero, production/framing annotations, huge display type, controlled autoplay, and user-initiated substantive media.

**Transferable:** Borrow interface language from the craft itself. Ambient motion can set context; substantive media should be controlled and pausable.

**Use here:** Cloud/system vocabulary can inform labels and diagrams, but avoid fake terminal chrome with no informational purpose.

**Do not copy:** Wordmark, footage, production overlays, labels, layout, or showreel behavior.

### Gradient Labs — explain a system through actors and proof
Source: [gradient-labs.ai](https://gradient-labs.ai/)

**Observed:** Direct value proposition; early social proof; visual system of actors and handoffs; sequence from value to outcomes, mechanism, integrations, security, implementation, and action.

**Transferable:** Visualize abstract systems through named actors and flows. Organize evidence around visitor uncertainty.

**Use here:** For a cloud architecture project, show a compact original actor/service flow and then state what Jay implemented and verified.

**Do not copy:** Isometric world, product diagrams, logos, page sequence, cards, claims, or copy.

## Selection guide

| Portfolio problem | Primary reference principle | Supporting principle |
|---|---|---|
| Recruiters cannot find the point | James: position + proof + action | REA: 5/10/15-second scan |
| Too many equal project cards | Thomas: curate and prioritize | Exo Ape: fewer stronger moments |
| Personality feels detached | Cyd: one identity across roles | Junni: one repeated behavior |
| Design feels decorative | THE LINE: domain vocabulary | NLC: thesis as frame |
| Technical work is hard to explain | Gradient Labs: actors/handoffs | REA: narrow claims + evidence |

Use one primary idea and at most two supporting ideas per change. More sources do not automatically create a better design.

## Applied synthesis: page-turn navigation (2026-10-23)

The portfolio replaced its single long vertical scroll with a **page-turn navigation** model, added as progressive enhancement (`assets/js/pageturn.js`, styles appended to `src/input.css`). This is a worked example of the "synthesize; do not clone" rule.

**Problem borrowed for:** help a visitor move through the portfolio one self-contained "page" at a time instead of an undifferentiated scroll, giving each section a clear beginning and end.

**References synthesized (principles only):**
- *Thomas Monavon* — one section fully owns the viewport; movement is a deliberate, progress-aware transition rather than free scroll. ([thomasmonavon.com](https://www.thomasmonavon.com/), re-checked 2026-10-23)
- *Cyd Stumpel* — a literal "turn" gesture can be expressive and still accessible when it is built as enhancement over usable content. ([cydstumpel.nl](https://cydstumpel.nl/), re-checked 2026-10-23)
- *Exo Ape* — a single oversized transition number marks the moment of change without extra chrome. ([exoape.com](https://www.exoape.com/), re-checked 2026-10-23)

**What was implemented (observed in this repo):**
- Each existing `<section>` / the `#contact` footer becomes a full-viewport page; document order, headings, the skip link, and deep links (`#about`, …) are preserved.
- A 3D left-spine "page curl" turn (forward and backward), a sweeping fold sheen, a vertical pager with numbered labels, and a transient oversized page number.
- Forward/back via wheel, Arrow/Page/Home/End keys, swipe, in-page anchor links, and pager buttons; the URL hash stays in sync for shareable links.
- Inner-scroll-aware wheel handling so a tall page scrolls internally before it turns.

**What was deliberately NOT copied:** no markup, CSS, JavaScript, assets, copy, palette, type pairing, transition choreography, progress-counter treatment, or signature interaction from any reference site. The curl geometry, timing curve, pager vocabulary (reusing the repo's own `index-plate`/mono tokens), and fold effect are original to this repository.

**Fallbacks (verification, 2026-10-23, headless Chromium state-machine test):** the enhancement engages only at `min-width: 1024px` with a fine pointer and no `prefers-reduced-motion`. Confirmed: engages on a 1440px viewport (7 pages, 7 pager buttons), turns forward/back by keyboard, turns via nav-link click with hash sync, and fully disengages to normal document scroll when resized to a 390px viewport (`body` overflow returns to `visible`, pager hidden). Reduced motion disables the 3D/transform choreography via CSS. No-JS leaves the plain scrollable document untouched.

## Source and licensing note

The websites above are references, not dependencies. Their publicly visible designs and content were analyzed only to derive abstract principles. No source code, copy, media, exact palette, exact type pairing, or composition is licensed to this repository by inclusion in this document.
