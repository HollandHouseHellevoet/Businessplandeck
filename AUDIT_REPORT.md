# Deck Audit Report
Generated: 2026-04-19
Repo: HollandHouseHellevoet/Businessplandeck
Branch: `claude/update-deck-poh-bios-FAk1W`
Audited commit: `0ecf020`

## Summary
- Total edits audited: 14
- APPLIED: 4
- NOT APPLIED: 4
- PARTIAL: 6
- NEEDS DECISION: 0

## Detailed findings

### Edit 1 · Section I · Plural hospitals framing
Status: **PARTIAL**

Notes:
- Plural headline is in place. `index.html:1498` reads "Your hospitals write 14 checks a year to people who do not work for you."
- Lede is pluralized at `index.html:1500` ("money your facilities generated").
- Footnote at `index.html:1520` reads "Representative annual outlay per physician-owned hospital with 100 to 500 employees. Multiply by every facility in the system."
- The second expected sentence — "At 27 facilities, the aggregate is larger than anyone has shown you on one page." — is **not present**. Grep for `aggregate is larger` returns no matches. The explicit 27-facility aggregate callout needs to be added to Section I.

### Edit 2 · Section II · Placeholder removal
Status: **APPLIED**

Notes:
- Zero occurrences of the string `[Dutch to confirm]` anywhere in `index.html`. All 14 placeholder flags on the check-row retained column were removed in commit `c3293f2`.

### Edit 3 · Section VI · Proof case audience framing
Status: **NOT APPLIED**

Notes:
- The expected paragraph ("A physician-owned hospital inside the captive for two years. Same facility size, same acuity mix, same insurance market as the hospitals in this room. The only variable that changed is who owns the surplus.") is **not present**. Grep for `acuity mix`, `hospitals in this room`, and `A physician-owned hospital inside the captive` all return zero matches.
- The closest current language lives at `index.html:1917`: "These numbers look like the numbers in your own books. Same cost categories. Same patient demographics. Same insurance market. The only variable that changed is who owns the surplus." It sits **below** the proof-case stats block, not above, and uses "patient demographics" in place of "acuity mix" and omits the "hospitals in this room" framing.
- Section VI lede (`:1857`) reads "One physician-owned hospital, two years inside the structure. The proof case is audited." — this replaces the earlier intro but is not the specified paragraph.

### Edit 4 · NEW Section VI-A · Nutex-Scale Outlay
Status: **PARTIAL**

Notes:
- A new section VI-A exists between Section VI and Section VII (`index.html:1922-1955`).
- **Title mismatch:** eyebrow reads "Aggregate Premium Outlay" (`:1927`); expected "The Nutex-Scale Outlay". The word "Nutex" does not appear in this section.
- **Headline mismatch:** h-section reads "For a system of your size, the annual premium outlay is material." (`:1929`); expected "27 facilities. 900 employees. $43 to $56 million in annual premium."
- **Numbers present:** `$43M – $56M` (`:1936`) and `900 EEs` (`:1941`) anchor stats are in place.
- **Missing content:** no commercial P&C stack table; no line item for "900 employees × $20,000 PEPY" — grep for `PEPY` returns zero matches; no explicit "master health plan" label.
- Overall: the numeric anchors are correct but the section is not Nutex-named and lacks the PEPY math and P&C stack table.

### Edit 5 · NEW Section VI-B · The Trajectory
Status: **PARTIAL**

Notes:
- Section VI-B exists between VI-A and Section VII (`index.html:1957-2000`).
- **Title mismatch:** eyebrow reads "Four-Year Trajectory" (`:1962`); expected "The Trajectory".
- **Headline mismatch:** h-section reads "The outlay triples over four years." (`:1964`); expected "Premium outlay has scaled faster than your CFO has been tracking."
- **Axis mismatch:** the stat grid uses relative labels "Year 1 / Year 2 / Year 3 / Year 4" rather than the expected calendar-year range "2022 / 2023 / 2024 / 2025 / 2026E". Grep for `2026E`, `2022`, `2023`, `2024`, `2025` in the trajectory table returns no matches (only found in unrelated chart JS at `:2623`).
- Concept of a multi-year trajectory with tripling outlay is present, but the CFO framing and calendar-year table are missing.

### Edit 6 · Section VII · Nutex contextual paragraph
Status: **NOT APPLIED**

Notes:
- A 27-facility paragraph exists at `index.html:2018-2020` but the copy is different from the spec. Current text begins "Read this section against a 27-facility system. Every line below scales on facility count…" and does not contain the expected "The numbers that follow are the addressable market across all physician-owned facilities…" language.
- The expected phrases "Captive I health benefits line alone absorbs", "master health plan outlay", "$23-28M", and "$18M" are **all absent**. Grep for `master health plan` and `addressable market across` return zero matches.
- Because the expected paragraph is not present at all, this is NOT APPLIED rather than PARTIAL on a stale number. When this edit is applied, use the revised **$18M** figure, not the draft-era $23-28M.

### Edit 7 · Section XIII · Remove PhyCap venture fund line
Status: **APPLIED**

Notes:
- The string "The venture fund investing in the startups that support her practice." is **absent**. Grep returns zero matches.
- Answer list in Section XIII (`index.html:2441-2446`) contains exactly **six `<p>` items**: intelligence platform, captive, direct contracts, forward contracts, exchange, policy organization. No seventh venture-fund item.

### Edit 8 · Team Appendix · Dutch bio
Status: **PARTIAL**

Notes:
- Old "Only non-physician GP at PhyCap" language is **removed**.
- Current bio (`index.html:2520`): "Two direct contracting exits. Inventor of surgery futures. Physicians Advocacy Alliance board member. Founder of Bliksem. 28 years operating in healthcare."
- **Differences from expected:**
  - "Physicians Advocacy Alliance board member" is spelled out; expected abbreviation "PHA board member".
  - "Founder of Bliksem" is missing both "Holdings" and "and MedMerge"; expected "Founder of Bliksem Holdings and MedMerge".
  - "28 years" uses numerals; expected spelled form "Twenty-eight years".
- Intent is captured but wording does not match the approved replacement text.

### Edit 9 · Section XII Priority I · POH independence language
Status: **PARTIAL**

Notes:
- Current Priority I body (`index.html:2381`): "The physician-owned hospital moratorium. Banned new construction in 2010 under the ACA. 187 independent physician-owned hospitals remain—distinct from broader counts that fold in joint ventures with incumbent systems. Repeal opens the market for physician-led facility investment."
- **Correct:** "187 independent physician-owned hospitals" and the joint-venture distinction are present.
- **Deltas from expected exact language:**
  - Expected opens "Section 6001 of the ACA banned new construction in 2010." Current opens "Banned new construction in 2010 under the ACA." — section number is missing.
  - Expected includes the separate sentences "frozen in place." and "Counts that include health-system joint ventures run higher. The independent number is the one that matters." Current collapses the distinction into a single em-dash clause.
- Substance matches; phrasing does not.

### Edit 10 · Section XII Priority II · CON count
Status: **APPLIED**

Notes:
- String "34 states plus Washington D.C." is **absent**. Grep returns zero matches.
- `index.html:2394` reads "Certificate of Need statutes in 35 jurisdictions let incumbent systems block new competitors from building."

### Edit 11 · Section XII · Citation lines
Status: **PARTIAL**

Notes:
- Both Priority I and Priority II carry a citation line:
  - `index.html:2384`: "Source: The Rojas Report"
  - `index.html:2397`: "Source: The Rojas Report"
- Both are **missing the specificity suffixes**. Expected: "Source: The Rojas Report, 50-state POH intelligence." under Priority I and "Source: The Rojas Report, 50-state CON intelligence." under Priority II. Grep for `50-state POH` and `50-state CON` returns zero matches.

### Edit 12 · Footer language on every slide
Status: **NOT APPLIED**

Notes:
- Expected replacement string "Confidential. For discussion with Nutex Health leadership only. Not for distribution." is **absent**. Grep for `Nutex Health leadership` returns zero matches.
- Old language "Confidential. Covered by Non-Disclosure Agreement." still appears at:
  - `index.html:1477` (cover slide bottom block)
  - `index.html:2562` (global footer)
- An additional persistent watermark was added at `index.html:1460` reading "Confidential · Under NDA". Global footer was also expanded with "Every figure in this deck is representative or illustrative / Audited numbers, facility names, and line-by-line pro formas / are released only under an executed mutual NDA." None of these carry the Nutex-specific "For discussion with Nutex Health leadership only. Not for distribution." copy the edit specifies.
- This edit needs a global string replacement across the cover, footer, and watermark.

### Edit 13 · Section VI · NDA-gated diligence language
Status: **NOT APPLIED**

Notes:
- Neither the expected phrase "available to qualified diligence under NDA" nor the baseline "available to qualified diligence" appears anywhere in the deck. Grep for `qualified diligence` returns zero matches.
- The earlier "real, audited, and available to qualified diligence" phrasing is also gone — replaced in the VI rewrite with a completely different lede: "One physician-owned hospital, two years inside the structure. The proof case is audited." (`index.html:1857`).
- Section VI now carries a dedicated "Under NDA" callout box (`index.html:1884-1891`) stating audited statements, loss triangles, percentage moves, retention, and the facility name are available on request with executed mutual NDA — but this is new prose, not the exact "real and available … to qualified diligence under NDA" edit requested.
- Net: the intent (gate detail behind NDA) is addressed in a different form; the specific phrase the audit requires is not present.

### Edit 14 · NEW final slide · Next Steps
Status: **APPLIED**

Notes:
- New slide exists at `index.html:2475-2503`, positioned after the unnumbered 2029 Graduate close (`:2462-2473`, "You built the hospitals…") and before the Team appendix (`:2505`).
- Title: "Next Steps." (h-section, `:2482`).
- Body paragraphs match the soft version verbatim:
  - `:2486` — "The architecture in this deck is the beginning of the conversation. The numbers that matter most, the specific case studies, the facility-level diligence on three Nutex hospitals, and the pathway to execution sit one layer deeper."
  - `:2489` — "The next layer includes live client financials, the engineering memo behind the three captives, and a Nutex-specific deployment framework. Happy to walk through it under NDA when you are ready."
- Contact block below a thin gold rule:
  - `:2498` — `info@medmerge.co` (live `mailto:` link)
  - `:2499` — `602.777.0101` (live `tel:+16027770101` link)

## Outstanding items
No edits require a decision from Dutch before being actionable. Every NOT APPLIED / PARTIAL item above is a pure copy edit and can be closed in a single follow-up commit.

The only judgement call embedded in the checklist is **Edit 6**'s reminder that if Section VII's Nutex paragraph is added, it should use **$18M**, not the pre-revision $23-28M figure.

## Files modified since audit list was drafted
Commits on `claude/update-deck-poh-bios-FAk1W` that landed during this planning session, newest first:

- `0ecf020` — Replace Next Steps slide with Nutex-specific closing copy
- `3f6f2a9` — Monday meeting update: plural hospitals, NDA-gated proof, system-scale sizing
- `c3293f2` — Update POH framing, CON count, Dutch bio; drop PhyCap venture fund line

Only `index.html` is touched across these three commits. No other deck files were modified.

## Follow-up edit set (single commit to bring status to APPLIED)
1. Append "At 27 facilities, the aggregate is larger than anyone has shown you on one page." to Section I (Edit 1).
2. Insert the "A physician-owned hospital inside the captive for two years…" paragraph above the Section VI proof-case stat grid (Edit 3).
3. Rename Section VI-A to "The Nutex-Scale Outlay" with the "27 facilities. 900 employees. $43 to $56 million in annual premium." headline; add the commercial P&C stack table and the `900 employees × $20,000 PEPY` math line (Edit 4).
4. Rename Section VI-B to "The Trajectory" with the "Premium outlay has scaled faster than your CFO has been tracking." headline; replace relative year labels with the 2022–2026E table (Edit 5).
5. Replace the current 27-facility framing paragraph in Section VII with the "The numbers that follow are the addressable market… For Nutex specifically, the Captive I health benefits line alone absorbs the $18M master health plan outlay…" paragraph (Edit 6, with revised $18M figure).
6. Update Dutch's bio to the exact approved wording: "…PHA board member. Founder of Bliksem Holdings and MedMerge. Twenty-eight years operating in healthcare." (Edit 8).
7. Replace the current Priority I body with the exact approved Section 6001 phrasing ("frozen in place… Counts that include health-system joint ventures run higher. The independent number is the one that matters.") (Edit 9).
8. Extend the two `Source: The Rojas Report` lines to `Source: The Rojas Report, 50-state POH intelligence.` and `Source: The Rojas Report, 50-state CON intelligence.` (Edit 11).
9. Replace every instance of "Confidential. Covered by Non-Disclosure Agreement." (cover, global footer) and the watermark with "Confidential. For discussion with Nutex Health leadership only. Not for distribution." (Edit 12).
10. In Section VI lede, restore "real and available" and add "under NDA" to the qualified-diligence phrasing (Edit 13).
