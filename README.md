# EF5342 Beamer Decks

LaTeX Beamer versions of the 10 weekly lecture decks. The original PPTX files
in `../` were the source of record during the 2026-09-06 migration; since the
2026-09-09 fact refresh these decks lead the pptx on content (see Status).

## Layout

```
beamer/
├── ef5342.sty           — shared course theme. NEVER edit per-week; consistency
│                          across weeks is the entire point of this file.
├── extract_week.py      — pptx → structured markdown + figures extractor
├── week1_Overview/      — one subfolder per week:
│   ├── weekN_*.tex      — content-only deck, \usepackage{../ef5342}
│   ├── weekN_extract.md — per-slide extraction dump (intermediate, keep for
│   │                      the [src] coverage audit)
│   ├── figures/         — images recovered from the pptx
│   └── weekN_*.pdf      — compiled output
└── week2_InterestRate/ ... week10_Banks/
```

## Pipeline (convert or update a week)

1. **Extract** (only when the pptx changes): from the week subfolder run
   `python ../extract_week.py ../../weekN_<Name>.pptx`
   (python = `/c/Users/frank/miniconda3/python.exe`). Image recovery is
   relationship-based, so it catches image-fill placeholders that a
   python-pptx shape walk misses.
2. **Author** `weekN_*.tex` from the extract dump — see conventions below.
3. **Compile** with pdfLaTeX (NOT xelatex/lualatex — the theme requires it):
   `pdflatex -interaction=nonstopmode weekN_*.tex`, twice.
   Pass = 0 errors, 0 overfull boxes.
4. **Audit**:
   `python C:/Users/frank/.claude/skills/beamer-check/scripts/beamer_check.py weekN_*.tex --output-dir beamer-check-output`
   then visually inspect the rendered PNGs in `beamer-check-output/slides/`.
5. **Coverage check** — every source slide must be claimed by a frame's
   `[src: N]` comment:
   ```bash
   python -c "import re; tex=open('weekN_*.tex',encoding='utf-8').read(); cov=set(int(x) for m in re.finditer(r'% \[src: ([\d, ]+)\]',tex) for x in m.group(1).split(',')); miss=[i for i in range(1,66) if i not in cov]; print('missing:',miss)"
   ```
   (adjust the slide-count upper bound per week)

## Authoring conventions

- `\documentclass[aspectratio=169]{beamer}` + `\usepackage{../ef5342}`. No
  per-week theme overrides.
- **Restructure, don't port 1:1.** PowerPoint decks are low-density; merge
  related slides into denser frames (definition + example together, split
  filler slides consolidated). Target roughly 55–70% of the source slide
  count.
- Every frame opens with `% [src: N]` or `% [src: N, M]` listing the source
  pptx slide(s) it covers. This is the coverage audit trail — do not omit.
- Instructor notes from the pptx → `\note{...}` on the matching frame.
- Tables → LaTeX `booktabs` tabulars, never screenshot unless unreadable.
- Figures → `\includegraphics[height=0.58–0.80\textheight,keepaspectratio]{figures/...}`
  (height constraint, not width — several source images are taller than wide).
  Source lines (e.g., "Source: IIF") under the figure in `\small`.
- Equations pasted as images in the pptx → typeset native math when the
  formula is inferable; keep the image only if uncertain.
- Escape `\$ \% \& \# \_`; curly quotes → TeX quotes or straight ASCII.
- Titles are assertions where content allows; `description` lists for
  definition-style content (the decks' dominant pattern).
- Special characters from CJK-adjacent text: keep UTF-8; pdfLaTeX handles it.

## Status

| Week | Folder | Source slides | Frames | State |
|------|--------|--------------|--------|-------|
| 1 | week1_Overview | 65 | 44 | Done (2026-09-06, pilot; full visual audit passed) |
| 2 | week2_InterestRate | 54 | 40 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; UET/LPT/forward-rate/annuity formulas typeset natively; worked-example solution images kept verbatim) |
| 3 | week3_BondMarket | 60 | 39 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; bond-pricing/YTM/duration/convexity formulas typeset natively; duration EMF tables unrenderable — see note in .tex; gif/wmf images converted to PNG) |
| 4 | week4_MoneyMarket | 60 | 39 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; slide34 native chart TODO; 2 EMF diagrams converted to PNG) |
| 5 | week5_StockMarket | 59 | 42 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; slide53 Shiller chart TODO; slide52 EMF converted to PNG) |
| 6 | week6_MarketEfficiency | 64 | 45 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; 6 native PowerPoint charts marked TODO — slides 21, 33, 34, 40, 41, 42; gif/jfif images converted to PNG) |
| 7 | week7_FXmarkets | 61 | 39 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; all parity-condition equations typeset natively; Lustig-Verdelhan wmf chart converted to PNG) |
| 8 | week8_Derivatives | 59 | 38 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; payoff diagrams redrawn as native TikZ; parity formulas native; slide56 EMF dropped — content typeset natively) |
| 9 | week9_Funds | 68 | 47 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; slide20 image corrupted black — dropped, content folded into returns frame) |
| 10 | week10_Banks | 60 | 39 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete) |

**2026-09-09 refresh:** all 34 MUST + 63 SHOULD stale-fact items fixed across
the 10 decks (universal `\date{Semester B 2026--2027}`, refreshed yields,
TIC/SIFMA/QBP/COFER data, DJIA roster with the June 2026 Alphabet change,
Basel III Endgame March 2026 reproposal, etc.); recompiled, 0 errors.
Per-week changelogs and research dossiers in
`agent_tasks/fix_stale_items_2026090923/`. The decks now lead the source
pptx on facts — the pptx still carries the 2025/2026-vintage numbers.

## Known issues

- **Deferred from the 2026-09-09 refresh** (see
  `agent_tasks/fix_stale_items_2026090923/fix_summary.md` §Deferred):
  - ~51 NICE-TO-HAVE items (URL verification batch, housekeeping).
  - Image-regeneration batch via the course-figure skill: W1 IIF/WFE, W2
    1986–2025 chart, W4 ~8 bitmaps + slide-34 TODO, W5 S&P/HSI + slide-53
    TODO, W6 NASDAQ + 6 chart TODOs, W8 VIX/MOVE/contango/CME specs, W9 six
    Factbook figure citations, W10 HSOB map.
  - **Professor arbitration pending:** W1 equity cap $158T (SIFMA) vs $152T
    (WFE); W8 MSFT put-moneyness narrative (source data had an arithmetic
    impossibility, written around); W6 old alpha-figure provenance
    (untraceable).
- Week1's title-page logo image was dropped in conversion (decorative).
- Week4 slide 34 (money market spreads chart) and Week5 slide 53 (Shiller P/E
  chart) were native PowerPoint charts with no extractable figure — marked
  `% TODO: recreate chart` in the .tex; recreate or screenshot before term.
- Week6 slides 21, 33, 34, 40, 41, 42 were native PowerPoint charts with no
  extractable figure — same TODO treatment.
- Low-quality source images that only a data-driven remake can fix
  (2026-09-06 spot audit): week3 slide-25 area chart (blurry source), week9
  slide-61 hedge-fund decomposition table (dense 1080px screenshot), week10
  slide-25 deposit-insurance map (distorted in source). Candidates for the
  course-figure skill.
- All embedded transparent PNGs were flattened onto white (`*_flat.png`,
  2026-09-06) — pdfLaTeX renders alpha-channel charts blank otherwise. New
  extractions need the same treatment: composite any RGBA/PA PNG in figures/
  onto white (ImageMagick `convert in.png -background white -alpha remove
  -alpha off out_flat.png` or PIL equivalent).
