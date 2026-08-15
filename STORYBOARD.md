# The Death of the Department Store — Storyboard

**One-sentence version:** In 1992 department stores took one in ten US retail dollars and online/mail order one in twenty-five; online passed them in October 2004, COVID finished the job, and by 2024 department stores were 1.8% of retail — a series the Census Bureau stopped publishing in 2025.
**Sources:** US Census Bureau, Monthly Retail Trade Survey (seasonally adjusted, nominal $ millions), via FRED series RSDSELD, RSNSR, RSXFS, RSCCAS, RSGCS, RSEAS, RSSGHBMS, RSFHFS, RSBMGESD, RSHPCS, RSMVPD, RSGASS; e-commerce share ECOMPCTSA (quarterly). Downloaded Aug 2026 → `data/raw/`. Every number computed from those files.
**Caveats:** Nominal dollars (not inflation-adjusted) — growth multiples overstate real growth; shares and crossovers are unaffected. "Online & other nonstore" = NAICS 454 nonstore retailers (e-commerce, mail order, vending, direct selling). Department-store series ends March 2025 (Census discontinued it); annual charts stop at 2024. "Total retail" excludes food services. Store categories do not sum to total; the remainder is shown as "All other stores".

## Data files (`public/data/`)
| File | Shape | Used in |
|---|---|---|
| `retail_monthly.csv` | 415 months × 11 kinds + total, $bn (wide) | Scene A lines |
| `retail_annual.csv` | 33 years × 12 series + total, $bn (wide) | Scene B stacked area / share |
| `retail_monthly_long.csv` | long (year_dec, kind, sales_bn) | Scene C small multiples |
| `covid_feb_apr_2020.csv` | kind, feb, apr, change_pct | Scene C bars |
| `kinds_summary.csv` | 1992 vs 2024, growth, peak month | reference / hero |
| `ecommerce_share.csv` | quarterly 1999Q4–2026Q1 | Scene D |

## Key facts (verified)
- Nonstore: $5.4B/month (Jan 1992) → **$136.9B (Jul 2026), ×25**; annual $66.6B (1992) → $1,413B (2024), ×21; share of retail **3.8% → 19.5%** (20.2% in 2025).
- Department stores: annual $176B (1992) → peak **$232B (2000)**, monthly peak **$19.9B Jan 2001** → $131B (2024), −43% nominal; share **10.1% → 1.8%**. Last published month Mar 2025 ($10.7B).
- **Crossover: October 2004** — nonstore $18.1B vs department stores $18.0B.
- **COVID, Feb→Apr 2020:** total retail −17.3%; clothing −87.6% ($22.0B → $2.7B); furniture −61%; electronics −54%; sporting goods −45%; department stores −43%; motor vehicles −37%; **online +18.9%**; grocery +10.7%.
- Electronics & appliance stores peaked **May 2008 ($9.4B)**; Jul 2026 $8.1B — below the 2008 peak even in nominal dollars. Gas stations peaked Jun 2022 ($68B). Health & personal care ×5.5 since 1992.
- E-commerce share of retail sales: **0.6% (Q4 1999) → 16.9% (Q1 2026)**; 10.0% (Q1 2019).

## Scenes
- **A — Two lines** (hero numbers → monthly lines dept vs online: peak 2001, crossover Oct 2004, COVID)
- **B — Everyone's slice** (annual stacked area of all kinds → 100% share view → highlight the two protagonists)
- **C — The accelerant** (COVID Feb→Apr 2020 bars with negatives; then small multiples: dept, electronics, online, health)
- **D — The share of the cart** (e-commerce % line, 0.6 → 16.9; closing number)
- Footer: source, definitions, nominal caveat, discontinued series.

## Acceptance checklist
- [ ] Numbers trace to `public/data/`; annotations templated; nominal caveat in footer; scroll-back clean; mobile ok; console clean.
