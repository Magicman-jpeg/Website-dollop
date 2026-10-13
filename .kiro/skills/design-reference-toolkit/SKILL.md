---
name: design-reference-toolkit
description: Evidence-led workflow and curated public-site pattern library for researching, critiquing, and improving this portfolio without copying source designs. Use for website inspiration, visual reverse engineering, interaction design, portfolio hierarchy, and optional SVG exploration.
---

# Design Reference Toolkit

Use this skill when the user asks to study a public website, take inspiration from a reference, critique the portfolio, choose a layout or interaction, or implement a reference-informed redesign.

This skill is the repository's on-demand reference-research workflow. Apply it together with the current implementation rather than assuming an older design decision is still authoritative.

Its quality floor is built in:
- ground every decision in Jay's real content and recruiter journey;
- avoid generic AI defaults, repeated card kits, decorative labels, and unsupported claims;
- keep the type system and color tokens deliberate rather than adding novelty by default;
- use one signature interaction, progressive enhancement, explicit properties, and ease-out entrances;
- preserve semantic structure, visible focus, accessible contrast, responsive reflow, and `prefers-reduced-motion`;
- read affected code before editing, reuse existing primitives, and write only what the task needs.

## Start from the actual surface

This repository's root portfolio is the target surface unless the user explicitly names another one. Treat these as implementation sources of truth:
- `index.html`: content, information architecture, and markup
- `assets/js/main.js`: client behavior and animation orchestration
- `tailwind.config.js`: design tokens and font roles
- `src/input.css`: authored visual primitives and effects
- `assets/css/tailwind.css`: generated output; rebuild it, never edit it directly

## Evidence-led reference study

Before coding, inspect the live reference when accessible. Record:
1. **Observed:** visible hierarchy, page sequence, navigation, responsive behavior, controls, motion, semantics, and accessibility signals.
2. **Inferred:** why those choices may work for that audience and content.
3. **Unknown:** implementation details or behavior that cannot be verified.
4. **Transferable principle:** the abstract design problem solved.
5. **Portfolio adaptation:** how the principle serves Jay's real content and recruiter journey.

Never describe static inspection as observed runtime behavior. Re-check live sites because public websites change.

For broad research, use a small question ledger:
- What is the page's primary job?
- What does a visitor understand in 5, 10, and 15 seconds?
- What is the strongest proof?
- What is the signature spatial or interaction idea?
- How does mobile differ?
- What remains usable without motion or JavaScript?
- Which claims remain unverified?

Read `references/investigation-protocol.md` for the full workflow.

## Synthesize; do not clone

Extract principles, not pixels. Do not copy a source site's:
- HTML, CSS, JavaScript, assets, copy, exact page composition, exact palette/type pairing, or signature illustration;
- distinctive choreography or interaction sequence closely enough to act as a replica;
- claims or metrics that are not true for this portfolio.

Prefer synthesis from two or more references. Transform across several axes:
- content model and evidence hierarchy;
- page composition and responsive behavior;
- token system and typography;
- interaction model and motion;
- accessibility and reduced-motion path.

The result must be recognizable as Jay's portfolio, grounded in his projects, education, community roles, and target opportunities.

## Choose patterns by problem

Do not ask for “the Thomas Monavon look” or “the Exo Ape layout.” Select a pattern by intent:
- **Recruiter clarity and evidence:** use proof-first hierarchy and compact professional metadata.
- **Project focus:** curate a few strong projects and give the best one more space.
- **Editorial personality:** vary section rhythm while preserving semantic headings and scanability.
- **Domain identity:** use a single metaphor tied to the subject, not unrelated effects.
- **Complex product explanation:** show actors, handoffs, outcomes, and risk reduction in sequence.
- **Motion:** one signature interaction; progressive enhancement; viewport and reduced-motion gating.

Read `references/site-patterns.md` before selecting a source-derived pattern.

## Implementation sequence

1. Audit the current surface before proposing change.
2. State the design problem and audience outcome.
3. Pick one primary pattern and at most two supporting principles.
4. Draft a low-fidelity structure and map it to existing tokens/primitives.
5. Run an originality check: remove source-specific decoration and exact composition.
6. Implement the smallest coherent change.
7. Rebuild generated CSS with `npm run build:css` when Tailwind classes or authored CSS change.
8. Verify desktop, intermediate, 320px/mobile, keyboard, focus, contrast, reduced motion, no-JS core content, links, and generated-source consistency as applicable.
9. Report what was observed, inferred, checked, and not checked.

## REA-derived discipline

The public MIT-licensed REA project is a model for evidence and ownership—not a required runtime dependency for this source repository. Retain these practices:
- distinguish observation, derivation, inference, and unknown;
- keep claims narrow and attach stable sources;
- inspect the smallest useful view first, then follow concrete gaps;
- reuse prior validated findings instead of repeating analysis;
- give authored, generated, and external content explicit owners;
- mark each requested question done, partial, unsupported, or unresolved;
- preserve limitations rather than converting uncertainty into certainty.

Do not run or install REA for ordinary source-code analysis of this portfolio. Its own skill says normal repository tools are the correct route here.

## Optional SVG capability

`bumbu/svg-pan-zoom` is documented as an optional capability only. Do not install it unless the site gains a concrete, dense inline SVG that genuinely needs pan and zoom. If that happens, read `references/svg-pan-zoom.md` first and provide accessible HTML controls, a keyboard path, a static fallback, and a pinned/versioned local asset.

## Reference maintenance

Every source-derived note must include its URL, access date, observed facts, inferred principle, and what was deliberately not copied. Update the note if the live site changes materially.
