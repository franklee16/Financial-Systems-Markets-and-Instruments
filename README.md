# EF5342 Beamer Decks

LaTeX Beamer versions of the 10 weekly lecture decks for EF5342 —
*Financial Systems, Markets, and Instruments*, a master-level investment
course at City University of Hong Kong. 

**Public mirror:** [github.com/franklee16/Financial-Systems-Markets-and-Instruments](https://github.com/franklee16/Financial-Systems-Markets-and-Instruments) — excludes `agent_tasks/`, `SESSION_REPORT.md`, LaTeX build artifacts, and `beamer-check-output/`. Push from this folder to keep them in sync.

## Lectures

The course walks from the architecture of the financial system through each
major market, then to the institutions that connect them:

| Week | Deck                                             | Topics                                                                                                                                                                                                                                                                                                                                                                             |
| ---- | ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | [week1_Overview](week1_Overview/)                 | **Overview of the Financial System.** Role of financial markets and intermediaries; direct vs. indirect finance; the flow of funds; size and structure of global equity, bond, and derivatives markets; financial crises as motivation for the course.                                                                                                                       |
| 2    | [week2_InterestRate](week2_InterestRate/)         | **Interest Rates.** Determinants of interest rates (supply/demand for loanable funds, Fisher equation, inflation and the ex-ante real rate); the term structure — yield curves, expectations hypothesis, liquidity premium and preferred habitat; time value of money (PV/FV, annuities, perpetuities) with worked examples; closes with the group-project grading rubrics. |
| 3    | [week3_BondMarket](week3_BondMarket/)             | **Bond Markets.** Treasury bonds and TIPS, municipal bonds and the tax exemption, corporate bonds and credit risk; bond pricing and yield to maturity; interest rate risk — duration, modified duration, convexity — with numerical examples.                                                                                                                              |
| 4    | [week4_MoneyMarket](week4_MoneyMarket/)           | **Money Markets.** Why money markets exist; the full instrument set — Treasury bills, repos and reverse repos, commercial paper, negotiable CDs, banker's acceptances, SOFR/Eurodollar legacy pricing; money market yield quotes (discount vs. bond-equivalent yields); money market funds.                                                                                 |
| 5    | [week5_StockMarket](week5_StockMarket/)           | **Stock Markets.** Primary markets — IPOs, underwriting, and IPO underpricing; secondary markets — exchanges, brokers, market makers, order types, alternative trading systems; stock market indexes (Dow, S&P 500, NASDAQ, global indexes) and how they are constructed; regulation of stock markets.                                                                     |
| 6    | [week6_MarketEfficiency](week6_MarketEfficiency/) | **Market Efficiency.** Efficient-market hypothesis in weak, semi-strong, and strong form; empirical evidence for and against; anomalies (size, value, momentum, calendar effects) and their explanations; fund performance and the active-management debate; smart beta ETFs.                                                                                                |
| 7    | [week7_FXmarkets](week7_FXmarkets/)               | **Foreign Exchange Markets.** FX market structure, quotes (spot, forward, bid-ask), and trade types; hedging FX risk with forwards; exchange-rate determination — interest rate parity, purchasing power parity, and the empirical failure of parity conditions; carry trade and other currency strategies.                                                                 |
| 8    | [week8_Derivatives](week8_Derivatives/)           | **Derivatives.** Overview — forwards, futures, swaps, options and the markets they trade on; options in depth — payoffs, put-call parity, factors determining option value, Black-Scholes intuition; hedging and speculation with derivatives, including option strategies and real-positions examples.                                                                    |
| 9    | [week9_Funds](week9_Funds/)                       | **The Asset Management Industry.** Size, structure, and fee economics of asset management; types of investment companies — open-end vs. closed-end funds, ETFs, index funds, unit investment trusts — with loads, fees, and return computation; hedge funds — strategies, fee structures (2-and-20), and performance.                                                     |
| 10   | [week10_Banks](week10_Banks/)                     | **Banking.** Structure and trends of the US banking industry — consolidation, off-balance-sheet activities; commercial bank regulation, deposit insurance, and Basel III; investment banks — what they do (underwriting, M&A advisory, trading) and their regulation after 2008.                                                                                           |

## Layout

```
beamer/
├── ef5342.sty           — shared course theme. NEVER edit per-week; consistency
│                          across weeks is the entire point of this file.
├── week1_Overview/      — one subfolder per week:
│   ├── weekN_*.tex      — content-only deck, \usepackage{../ef5342}
│   ├── figures/         — images used by the deck
│   └── weekN_*.pdf      — compiled output
└── week2_InterestRate/ ... week10_Banks/
```

## Pipeline (update a week)

1. **Edit** `weekN_*.tex` — see conventions below.
2. **Compile** with pdfLaTeX (NOT xelatex/lualatex — the theme requires it):
   `pdflatex -interaction=nonstopmode weekN_*.tex`, twice.
   Pass = 0 errors, 0 overfull boxes.
3. **Audit**:
   `python C:/Users/frank/.claude/skills/beamer-check/scripts/beamer_check.py weekN_*.tex --output-dir beamer-check-output`
   then visually inspect the rendered PNGs in `beamer-check-output/slides/`.
4. **Coverage check** — every source slide must be claimed by a frame's
   `[src: N]` comment:
   ```bash
   python -c "import re; tex=open('weekN_*.tex',encoding='utf-8').read(); cov=set(int(x) for m in re.finditer(r'% \[src: ([\d, ]+)\]',tex) for x in m.group(1).split(',')); miss=[i for i in range(1,66) if i not in cov]; print('missing:',miss)"
   ```

   (adjust the slide-count upper bound per week)

## Authoring conventions

- `\documentclass[aspectratio=169]{beamer}` + `\usepackage{../ef5342}`. No
  per-week theme overrides.
- Every frame opens with `% [src: N]` or `% [src: N, M]` listing the source
  slide(s) it covers. This is the coverage audit trail — do not omit.
- Instructor notes live in `\note{...}` on the matching frame.
- Tables → LaTeX `booktabs` tabulars, never screenshot unless unreadable.
- Figures → `\includegraphics[height=0.58–0.80\textheight,keepaspectratio]{figures/...}`
  (height constraint, not width — several images are taller than wide).
  Source lines (e.g., "Source: IIF") under the figure in `\small`.
- Equations are typeset as native math wherever the formula is known.
- Escape `\$ \% \& \# \_`; curly quotes → TeX quotes or straight ASCII.
- Titles are assertions where content allows; `description` lists for
  definition-style content (the decks' dominant pattern).
- Special characters from CJK-adjacent text: keep UTF-8; pdfLaTeX handles it.

## Status

| Week | Folder           | Frames | State |
|------|------------------|--------|-------|
| 1 | week1_Overview         | 44 | Done (2026-09-06; full visual audit passed) |
| 2 | week2_InterestRate     | 40 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; UET/LPT/forward-rate/annuity formulas typeset natively; worked-example solution images kept verbatim) |
| 3 | week3_BondMarket       | 39 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; bond-pricing/YTM/duration/convexity formulas typeset natively; duration EMF tables unrenderable — see note in .tex; gif/wmf images converted to PNG) |
| 4 | week4_MoneyMarket      | 39 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; slide34 native chart TODO; 2 EMF diagrams converted to PNG) |
| 5 | week5_StockMarket      | 42 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; slide53 Shiller chart TODO; slide52 EMF converted to PNG) |
| 6 | week6_MarketEfficiency | 45 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; 6 native charts marked TODO — slides 21, 33, 34, 40, 41, 42; gif/jfif images converted to PNG) |
| 7 | week7_FXmarkets        | 39 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; all parity-condition equations typeset natively; Lustig-Verdelhan wmf chart converted to PNG) |
| 8 | week8_Derivatives      | 38 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; payoff diagrams redrawn as native TikZ; parity formulas native; slide56 EMF dropped — content typeset natively) |
| 9 | week9_Funds            | 47 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete; slide20 image corrupted black — dropped, content folded into returns frame) |
| 10 | week10_Banks           | 39 | Done (2026-09-06; 0 errors / 0 overfull, coverage complete) |

**2026-09-09 fact refresh:** all 34 MUST + 63 SHOULD stale-fact items fixed
across the 10 decks (universal `\date{Semester B 2026--2027}`, refreshed
yields, TIC/SIFMA/QBP/COFER data, DJIA roster with the June 2026 Alphabet
change, Basel III Endgame March 2026 reproposal, etc.); recompiled, 0 errors.
Per-week changelogs and research dossiers in
`agent_tasks/fix_stale_items_2026090923/`.

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
- Week4 slide 34 (money market spreads chart) and Week5 slide 53 (Shiller P/E
  chart) are chart placeholders with no figure — marked
  `% TODO: recreate chart` in the .tex; recreate or screenshot before term.
- Week6 slides 21, 33, 34, 40, 41, 42 are chart placeholders — same TODO
  treatment.
- Low-quality figures that only a data-driven remake can fix (2026-09-06 spot
  audit): week3 slide-25 area chart (blurry), week9 slide-61 hedge-fund
  decomposition table (dense 1080px screenshot), week10 slide-25
  deposit-insurance map (distorted). Candidates for the course-figure skill.
- All transparent PNGs are flattened onto white (`*_flat.png`, 2026-09-06) —
  pdfLaTeX renders alpha-channel charts blank otherwise. New figures need the
  same treatment: composite any RGBA/PA PNG in figures/ onto white
  (ImageMagick `convert in.png -background white -alpha remove -alpha off
  out_flat.png` or PIL equivalent).
