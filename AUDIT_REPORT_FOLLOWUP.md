# Deck Audit Report — Follow-up Pass
Generated: 2026-04-19
Repo: HollandHouseHellevoet/Businessplandeck
Branch: `claude/update-deck-poh-bios-FAk1W`
Audited after follow-up fixes applied (pre-commit).
Prior audit: `AUDIT_REPORT.md` at commit `475730f`

## Summary
- Total edits audited: 14
- APPLIED: 14
- NOT APPLIED: 0
- PARTIAL: 0
- NEEDS DECISION: 0

Deck is fully reconciled to spec.

## Detailed findings

### Edit 1 · Section I · Plural hospitals framing
Status: **APPLIED**
- `index.html:1498` — "Your hospitals write 14 checks a year to people who do not work for you."
- `index.html:1500` — "None of them are physicians. None of them are nurses. All of them collect float, surplus, or commission on money your facilities generated. **At 27 facilities, the aggregate is larger than anyone has shown you on one page.**"
- Both required sentences now present.

### Edit 2 · Section II · Placeholder removal
Status: **APPLIED**
- Zero occurrences of `[Dutch to confirm]` in `index.html` (grep confirms).

### Edit 3 · Section VI · Proof case audience framing
Status: **APPLIED**
- `index.html:1857` (new `.lede`) — "A physician-owned hospital inside the captive for two years. Same facility size, same acuity mix, same insurance market as the hospitals in this room. The only variable that changed is who owns the surplus."
- Placed as the lead paragraph of Section VI, above the proof-case content.

### Edit 4 · NEW Section VI-A · Nutex-Scale Outlay
Status: **APPLIED**
- Eyebrow (`:1930`): "VI-A. The Nutex-Scale Outlay"
- Headline (`:1932`): "27 facilities. 900 employees. $43 to $56 million in annual premium. Commercial lines plus the master health plan. None of it owned by Nutex."
- Lede (`:1934`): "Not cost of care. Not payroll. Not capex. This is the money that leaves Nutex every year and lands with someone who does not work for you."
- Commercial P&C stack table present (`:1938-1974`) with all six lines + "Commercial subtotal $25–38M" (`:1971`).
- Master health plan table present (`:1978-1994`) with "900 employees × $20,000 PEPY (ASO fees, PBM spread, network access, plan administration, stop-loss component) — $18M".
- Aggregate callout (`:1996-2000`): "Aggregate premium outlay: $43 to $56M annually".
- Footnote (`:2002-2004`): "D&O held outside this analysis. Existing carrier relationships respected."
- Close paragraph (`:2006-2008`): "Premium outlay has roughly tripled in three years. At current growth, this line reaches $60M by 2027 and $75M by 2029. The captive is the only structure that puts any of it back on the Nutex balance sheet."

### Edit 5 · NEW Section VI-B · The Trajectory
Status: **APPLIED**
- Eyebrow (`:2014`): "VI-B. The Trajectory"
- Headline (`:2016`): "Premium outlay has scaled faster than your CFO has been tracking."
- Calendar-year table (`:2018-2084`) with rows 2022 / 2023 / 2024 / **2025** (highlighted gold) / 2026E carrying facilities, revenue, est. total premium outlay, and % of revenue columns.
- Close paragraph (`:2086-2088`): "The ratio is stable. The absolute dollars are not. Every new facility adds $2–3M to the annual outlay. Every percentage point of premium rate increase across the stack adds another $0.5–0.8M. The math compounds."

### Edit 6 · Section VII · Nutex contextual paragraph
Status: **APPLIED**
- `index.html:2094` — "The numbers that follow are the addressable market across all physician-owned facilities targeted by the captive architecture. For Nutex specifically, the Captive I health benefits line alone absorbs the **$18M** master health plan outlay. Captive II (P&C) absorbs most of the commercial stack. Captive III (med mal) absorbs the highest-premium single commercial line. A single physician-owned system of 27 facilities is not a fringe participant in this architecture. It is structurally significant by itself."
- Revised $18M figure used (not pre-revision $23–28M).
- Old 27-facility note replaced, not duplicated.

### Edit 7 · Section XIII · Remove PhyCap venture fund line
Status: **APPLIED**
- Grep for "venture fund investing" → zero matches.
- 2029 Graduate answer list (`index.html:2516-2521`) contains exactly six `<p>` items. No seventh venture-fund item.

### Edit 8 · Team Appendix · Dutch bio
Status: **APPLIED**
- `index.html:2595`: "Two direct contracting exits. Inventor of surgery futures. **PHA board member**. Founder of **Bliksem Holdings and MedMerge**. **Twenty-eight** years operating in healthcare."
- All three deltas from the prior audit resolved:
  - "PHA" abbreviated
  - "Bliksem Holdings and MedMerge"
  - "Twenty-eight" spelled
- Grep for "Physicians Advocacy Alliance", "Founder of Bliksem.", "28 years" → zero matches.

### Edit 9 · Section XII Priority I · POH independence language
Status: **APPLIED**
- `index.html:2456`: "The physician-owned hospital moratorium. Section 6001 of the ACA banned new construction in 2010. 187 independent physician-owned hospitals remain, frozen in place. Counts that include health-system joint ventures run higher. The independent number is the one that matters. Repeal opens the market for physician-led facility investment."
- Exact approved phrasing in place.

### Edit 10 · Section XII Priority II · CON count
Status: **APPLIED**
- Grep for "34 states plus Washington D.C." → zero matches.
- `index.html` carries "Certificate of Need statutes in 35 jurisdictions…" (unchanged from prior pass).

### Edit 11 · Section XII · Citation lines
Status: **APPLIED**
- `index.html:2459` — "Source: The Rojas Report, 50-state POH intelligence."
- `index.html:2472` — "Source: The Rojas Report, 50-state CON intelligence."
- Both specificity suffixes added.

### Edit 12 · Footer language on every slide
Status: **APPLIED**
- Grep for "Confidential. Covered by Non-Disclosure Agreement." → zero matches.
- Replaced everywhere the old string appeared:
  - `index.html:1477` (cover bottom): "Confidential. For discussion with Nutex Health leadership only. Not for distribution."
  - `index.html:2637` (global footer `.conf` block): same replacement.
- Persistent watermark (`index.html:1460`) also updated from "Confidential · Under NDA" to "Confidential · Nutex Leadership Only · Not For Distribution" so every slide carries the new posture, not the prior NDA-flavored one.

### Edit 13 · Section VI · NDA-gated diligence language
Status: **APPLIED**
- `index.html:1860` — opens "The numbers below are real and available to qualified diligence under NDA. Other physician-owned hospitals have followed…"
- Required phrase present verbatim; prior rewrite reconciled to the exact spec line.

### Edit 14 · NEW final slide · Next Steps
Status: **APPLIED**
- Slide still sits after the unnumbered 2029 Graduate close and before the Team appendix.
- Eyebrow (`index.html:2555`): "→ Next Steps".
- Headline (`:2557`): "Next Steps."
- Body paragraphs carry the soft Nutex-specific copy verbatim; contact block shows `info@medmerge.co` and `602.777.0101` as live `mailto:` / `tel:` links.
- No regression introduced by the other fixes.

## Outstanding items
None. Every edit verifies as APPLIED with exact spec strings present and every previously-flagged old string grep-clean.

## Files modified in this follow-up pass
Single file: `index.html`.

Changes made in this pass (all fall under one commit):
- Section I lede extended with "At 27 facilities, the aggregate is larger…" sentence.
- Section VI lede replaced with audience framing paragraph; supporting paragraph reconciled to "real and available to qualified diligence under NDA".
- Section VI-A fully rebuilt: renamed, new headline/lede, commercial P&C stack table, master health plan table, aggregate callout, footnote, close paragraph.
- Section VI-B fully rebuilt: renamed to "The Trajectory", new CFO headline, 2022–2026E calendar-year table, revised close paragraph.
- Section VII 27-facility paragraph replaced with Nutex-specific addressable-market + $18M paragraph.
- Priority I body replaced with exact approved phrasing.
- Both Rojas Report citations extended with "50-state POH intelligence." / "50-state CON intelligence." suffixes.
- Dutch bio replaced with "PHA board member / Bliksem Holdings and MedMerge / Twenty-eight years" phrasing.
- Cover confidentiality line, global footer confidentiality line, and persistent watermark all updated to Nutex-only posture.

## Result
14 of 14 edits APPLIED. Deck is locked for tomorrow's Vo / Bates / Blubaugh meeting.
