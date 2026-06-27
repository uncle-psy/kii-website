---
name: kii-website
description: Work on the Kinship Intelligence Institute (KII) one-page website. This is a NEW, standalone project, separate from the kinship.systems product site and the kinship-web Payload repo. Use whenever Moto mentions the Institute site, the KII page, the Institute one-pager, the agency/alignment site, the charter site, or asks to edit the hero, the pillars, the HEARTS section, the eras section, or any copy or layout on the Institute page. Triggers include: edit the Institute site, rework the KII hero, change the agency section, update the pillars, the institute landing page, the 501(c)(3) site. Err toward using this for anything about the Institute's public page. Does NOT apply to kinship.systems Movements/Exchange copy (use kinship-website-voice), to the kinship-web repo workflow (use kinship-website), or to Nightpapers, white papers, or memos.
metadata:
  type: project
---

# Kinship Intelligence Institute website (KII)

A single static one-page site for the Kinship Intelligence Institute. This is its own project. It is not the kinship.systems product site, and it is not the kinship-web Payload repo. Keep the two mentally separate, because the operational rules are different.

## What this is, and what it is not

- It is a self-contained static page: `index.html` plus an `assets/` folder. No CMS, no build step, no framework. Open `index.html` in a browser and it works.
- It is NOT in the `kinship-web` GitHub repo. There is no `test` or `main` branch, no Vercel preview, no Payload. Do not append the "Test: / Main:" URL footer that the `kinship-website` skill uses. That footer belongs to the product site only.
- It does NOT share the serverURL / GCS / Telegram gotchas from the `kinship-website` skill. Those are repo concerns and irrelevant here.

## Where the files live

Project folder (the connected/mounted folder for this work):
`Kinship Institute Website/`

```
index.html                         the whole site
assets/
  colors_and_type.css              Kinship design tokens (copied from the design system)
  fonts/                           Goudy Heavyface + Avenir (.ttf)
  logo-linear-skyblue.svg          used in the nav
  logo-stacked-skyblue.svg         used in the footer
  logo-stacked-white.svg           spare colorway
kii-website-SKILL.md               this file
```

## Source material (the spine of the copy)

Two documents in the project folder drive the content. Read them before rewriting copy.

1. `Kinship_Intelligence_Institute_Charter.docx (3).pdf` — the factual charter: mission, four pillars (Policy, Ethics, Research, Action) with chairs, funding model (20% founding equity, >=5% net profits), 501(c)(3) structure, editorial independence, governance, twelve-month priorities.
2. `Kinship Institue.pdf` — the manifesto/voice document. This is where the power comes from. Key passages the site draws on:
   - **Fighting fire with fire** (the hero). "These technologies have burned people. We know." The backfire metaphor: a controlled burn clears the fuel so the inferno dies where the backfire passed. "We use AI to make AI rare. Nothing here farms your attention."
   - **The art of agency.** Agency = sensing, choosing, acting on the world. It has been flattened by attention-farming platforms. The Institute protects agency and works to expand it at every scale.
   - **The real alignment challenge.** "But which humans?" There is no generic alignment because there is no generic human. Alignment as obedience scales the worst patterns. Care must reach past the operator to everyone and everything an agent touches. Grown one person, one agent, one organization at a time.
   - **Navigating the emotional field / HEARTS.** Six signals (Harmony, Empowerment, Artistry, Reason, Trust, Synthesis), each -100 to +100, health at the center. Sentinels guide interactions home; coercion is blocked; crisis brings in human support.
   - **Three phases of humanity.** Kinship (given to us), Hierarchical (imposed on us), Biomimetic (this one we design).
   - Mycelial-network metaphor: a forest moves nutrients and warning signals to where they're needed so the whole system can sense, adapt, respond. Use it for agency-at-ecosystem-scale.

## The two ideas the site is built to land

Moto's direction, in priority order:

1. **Agency.** Everything from organisms to ecosystems needs agency. The Institute does not only protect agency (which has been flattened); it works to expand agency everywhere. The page carries this with a dedicated Agency section and a scale band (Cell -> Person -> Community -> Organization -> Ecosystem -> Biosphere). Keep agency the loudest theme.
2. **Alignment to all of life, not generic "humanity."** Alignment runs from organisms to ecosystems, or it doesn't run at all. Avoid framing the mission as alignment "to humanity" in the abstract. Care extends past the operator to people, communities, and ecosystems.

The hero leads with "Fighting fire with fire." Keep that as the opening unless Moto says otherwise.

## Design system (bundled, do not reinvent)

The page links `assets/colors_and_type.css`, the Kinship design system token file. Always use the CSS variables; never hand-pick hexes.

- Background is deep navy (`var(--bg)` #09073A on `var(--bg-deep)` #03011B). Never black, never grey.
- One pulse of orange (`var(--accent)` #EB8000) per viewport, reserved for the single primary action. Two orange buttons in one viewport is a bug.
- Display type is Goudy Heavyface (`var(--font-display)`); body is Avenir (`var(--font-sans)`).
- The signature move: exactly one italic-orange `em.kin-emph` phrase per headline. One, never two.
- Numbers render in Goudy (the stat strip, the funding figures).
- Sky blue (`var(--kin-skyblue)` #03CCD9) for eyebrows, links, and the logo on navy.
- Buttons squared (`--radius-xs`), cards `--radius-lg`. Text arrows (->) as the default CTA glyph.

If a fuller design reference is needed, the original "Kinship Design System -- Collab.zip" has `UI Kit.html` and a `preview/` folder of component cards.

## Voice for this site

This site is an institute, a public-interest 501(c)(3), so it sits between two registers:

- Take the **power, metaphor, and active verbs** from `kinship-website-voice` (em-dashes are fine here, vivid imagery encouraged, short punchy lines land). The manifesto PDF is the tonal reference.
- Keep the **credibility discipline**: no hollow manifesto language ("we believe", "change the world", "revolutionize"), no "not X, it's Y" binary contrast (non-negotiable), no "the question is", no "now more than ever", no sweeping anthem at the end of a block. Specificity over abstraction.
- First person is acceptable here in a way it isn't on the product site: an institute can say "the Institute" and, sparingly, "we". Lean on "the Institute" as the subject.

When in doubt, it should read like the manifesto PDF wrote it, with the charter checking the facts.

## Working rules

- Edit `index.html` directly. It's a single file; keep the `<style>` block in the head.
- Preserve the section order unless asked: hero -> stakes -> agency -> alignment -> HEARTS -> eras -> pillars -> governance -> leadership -> CTA -> footer.
- Primary CTA is email to david.levine@kinship.systems (Moto's call). Keep the orange button count to one per viewport.
- Verify after edits: the sandbox usually can't download headless Chrome, so static-check instead (every `var(--...)` resolves against `colors_and_type.css`, tags balanced, one `kin-emph` per headline, mailto present). Offer to render a screenshot only if a browser is actually available.
- Do not add the Test/Main URL footer. This is not the repo site.

## When uncertain

Re-read the two source PDFs in the project folder. For facts (chairs, funding, governance), the charter wins. For tone and the central ideas (agency, alignment, fire-with-fire, the three eras, HEARTS), the manifesto wins. Ask Moto before inventing new claims about the Institute.
