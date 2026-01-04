# The Resilient Athlete Handbook Production System

This document distills the production specifications for building **The Resilient Athlete: 8-Week Mental Resilience Curriculum** into a ready-to-export PDF package. Use it as a working guide while building the handbook and exporting the three final deliverables.

---

## Part 1: Primary Constraints
- **Primary format:** PDF (US Letter, 8.5" × 11").
- **Margins:** 0.75" on all sides + 0.5" gutter on the left for binding.
- **Page count target:** 72 pages; **max file size:** 50MB.
- **Exports required:**
  - Color (RGB)
  - Black & white (grayscale, printer-optimized)
  - Print-optimized (CMYK, if available)

### Non-negotiable Style Rules
- Use provided heading sizes, colors, spacing, and line heights exactly.
- Color hex codes must match the palette:
  - Deep Blue `#1F3A70` (H1, accents)
  - Teal `#2E8B9E` (H3, callouts, rules)
  - Orange `#E8744A` (alerts, key points)
  - Dark Gray `#3A3A3A` (body text)
  - Off White `#F5F5F5` (boxes, backgrounds)
  - Pure White `#FFFFFF` (text on colored backgrounds)
- Body text line height: **1.5**.
- Callout boxes: teal background (`#F5F5F5`) with padding.

---

## Part 2: Design System

### Typography
- **Heading 1:** Montserrat Bold 24pt, Deep Blue, 6pt before/after.
- **Heading 2:** Montserrat SemiBold 18pt, Deep Blue, 4pt before/after.
- **Heading 3:** Montserrat SemiBold 14pt, Teal, 3pt before/after.
- **Body text:** Open Sans Regular 11pt, Dark Gray, 1.5 line height, 12pt before/after paragraphs.
- **Coach scripts:** Open Sans Bold 11pt.
- **Callout/notes:** Open Sans Regular 10pt italics where needed.
- **Page numbers:** Helvetica Regular 9pt, bottom-right.

### Spacing & Layout
- Bullet spacing: 6pt between items.
- Section breaks: full-width 2pt teal rule.
- Header/footer area: 0.5" from page edge.
- Left gutter: +0.5".

---

## Part 3: Page-by-Page Assembly

### Front Matter (Pages 1–8)
- **Cover:** Deep blue gradient; centered title/subtitle; logo placeholder; bottom tagline; copyright at 0.5" from edge.
- **Credits & Copyright:** H1 title; author bio; research foundation bullets; version; disclaimer (italic, teal box); contact info.
- **Table of Contents:** Centered H1; bold section labels; dotted leaders with right-aligned clickable page numbers.
- **How to Use This Guide (p4) & Neuroscience Foundation (p5–7):** H1 top; body at 11pt with callouts and lists per spacing rules.

### Core Program (Pages 8–55)
- Each week uses a 6–7 page template:
  1. **Opening spread:** Light teal gradient; “WEEK [#]” (H1 36pt, white), title (H2 24pt, white), tension question (14pt, white italics).
  2. **Session Overview:** H2; teal box listing Core Tension, Primary Skill, Duration (5-10-20-10-5).
  3. **Facilitator Script:** H3; “Coach Opening” subheading; script box with gray background; bold coach words.
  4. **Constraint-Led Game:** H3; subheading game name; sections for Field Setup (bullets), One Rule (orange box), Why This Rule Works (numbered), Coach Behavior (✅/❌ boxes), At Water Break callout, drill diagram placeholder.
  5. **Peer-Led Reflection:** H3; setup bullets; facilitator questions (numbered); coach role in italics.
  6. **Real-Time Debrief:** H3; location note; opening with timing; small-group reflection.
  7. **Closing Intention:** H3; format explanation; closing script in script box.
  8. **Facilitator Notes page:** H2; watch-fors (red icons), success markers (✅), adjustments, parent communication (email template), weekly survey question.

### Appendices (Pages 56–72)
- **Appendix A – Assessment Questions:** MTI (8 items) with scoring; APSQ (10 items) with scoring; weekly survey table.
- **Appendix B – Parent Email Templates:** 8 templates (subject, 11pt body, bold key concepts, signature).
- **Appendix C – Drill Diagrams:** 8 diagrams with overhead view, player colors (Blue attack, Red defend), ball path dotted, constraint callout (orange), coach watch-fors (blue).
- **Appendix D – Neuroscience Cheat Sheet:** One-page triad diagram (Amygdala, PFC, Vagus) with 10pt bullets and quick reference.
- **Appendix E – Research Citations:** APA 7 citations by category with DOIs where possible.

---

## Part 4: Diagram Standards
- Format PNG/SVG at **300 DPI** with white background and 1pt light-gray border.
- Labels: Open Sans Regular 9pt, Dark Gray.
- **Week 1 example:** “Unmarked Shot Only Drill” with half-field, marked goal/penalty boxes, attacking (blue) vs defending (red) markers, ball carrier with white X, shaded open space, orange constraint box (“Only shots in 1v0 situations count”), blue watch-for box (“Notice identity responses after invalid shots”).
- Weeks 2–8: follow same style; vary positions, rules, and observation points.

---

## Part 5: Production Workflow
1. **Content Preparation (2–3h):** Clean text, verify spelling, extract scripts/emails/assessments, plan page breaks.
2. **Design System Setup (1h):** Create color swatches; install fonts; build paragraph styles.
3. **Template Building (4–5h):** Front matter templates; full Week 1 sample; verify spacing/colors/fonts; create master for Weeks 2–8.
4. **Content Assembly (3–4h):** Populate all weeks, diagrams, appendices, TOC.
5. **Graphics & Diagrams (3–4h):** Generate neuroscience and drill diagrams; callout graphics; ensure 300 DPI PNG/SVG.
6. **Linking & Interactivity (1h):** Clickable TOC page numbers; bookmark structure; test links.
7. **QA & Testing (2h):** Fonts embedded; page numbers; color accuracy; line heights; headings; formatting; mobile readability; proofreading.
8. **Export & Finalization (1h):** Export RGB color, grayscale, and CMYK print PDFs; compress if needed; confirm <50MB and test in readers.

---

## Part 6: Quality Checklist
- Typography and spacing match specifications for all headings, body text, callouts, rules, margins, and page numbers.
- Content completeness: front matter (pp.1–8), all 8 weeks with full segments, appendices A–E, parent emails, drill diagrams, facilitator notes.
- Navigation: accurate clickable TOC, bookmarks, no broken images, embedded fonts.
- Quality: no typos, consistent terminology, aligned elements, 300 DPI images, accurate colors, file size <50MB.
- Multi-format verification: color, B&W, and print PDFs open correctly and remain legible after grayscale conversion.

---

## Part 7: Deliverables & Naming
- **Primary PDFs:**
  - `Resilience_Curriculum_Complete_Color.pdf` (RGB, 300 DPI, web optimized)
  - `Resilience_Curriculum_Complete_BW.pdf` (grayscale, 300 DPI, printer optimized)
  - `Resilience_Curriculum_Complete_Printable.pdf` (CMYK if available, 300 DPI, print ready)
- **Supporting files:**
  - `Coach_QuickReference_Cards.zip` (8 laminated one-pagers)
  - `Neuroscience_CheatSheet_PrinterFriendly.pdf`
  - `Drill_Diagrams_HighRes.zip` (8 PNG/SVG at 300 DPI)

---

## Part 8: Timeline & Milestones (Jan 6–12, 2026)
- Day 1: Content preparation.
- Day 2: Design system setup.
- Days 2–3: Templates (front matter + Week 1 sample).
- Days 3–5: Populate Weeks 2–8 and appendices; create diagrams.
- Day 6: Linking and QA.
- Day 7: Final exports and verification.

---

## Part 9: Troubleshooting Quick Wins
- **Fonts missing:** confirm Montserrat/Open Sans/Helvetica installed; embed all fonts on export.
- **Color drift:** double-check hex codes; export RGB for digital, CMYK for print; test in multiple readers.
- **Page numbers off:** fix footer position (0.5" from bottom, right-aligned) and verify margins.
- **Blurry diagrams:** ensure 300 DPI PNG/SVG; scale appropriately; test at 100% and 200% zoom.
- **Broken TOC links:** use named anchors/bookmarks for each page and link to them; retest after pagination changes.
- **Oversize files:** compress images (80–85% quality), reduce digital-version DPI to 150 if needed, strip metadata.

---

## Part 10: Success Criteria
- 72 fully formatted pages using the design system and color palette.
- Identical structure across all weeks; appendices complete.
- Accurate colors, spacing, and typography with embedded fonts and 300 DPI imagery.
- TOC links and bookmarks functional; file size under 50MB.
- Three exports (color, B&W, print) open correctly on desktop and mobile.

