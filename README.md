# SP Safety Rating by Police Department

An interactive dashboard measuring crime per capita across **93 Police Departments (DPs)** in São Paulo Capital, Brazil.

🔗 **Live dashboard:** https://caiomso.github.io/sp-sec-rate

---

## What is the Safety Rating?

The Safety Rating is a **0-to-100 index** that measures crime per capita in each police precinct. Higher = safer.

It combines three steps:
1. **Severity weighting** — incidents are weighted by type (homicide weighs more than theft)
2. **Population normalization** — score converted to rate per 100k inhabitants
3. **Logarithmic transformation** — anchored scale (100 = 150 pts/100k · 0 = 35,000 pts/100k)

| Range | Level |
|-------|-------|
| 80 – 100 | Very Safe |
| 60 – 79 | Safe |
| 40 – 59 | Moderate |
| 20 – 39 | Critical |
| 0 – 19 | Very Critical |

---

## Data Sources

| Period | Coverage | Source |
|--------|----------|--------|
| Q1 2024 | Jan–Mar 2024 | SSP-SP (full year dataset) |
| Q1 2025 | Jan–Mar 2025 | SSP-SP (full year dataset) |
| Q1 2026 | Jan–Mar 2026 | SSP-SP quarterly report |

Population: **SEADE** — Estimativas e Projeções Populacionais (MSP 2026: 12,126,482)

---

## Dashboard Features

- **Dashboard tab** — city-level Safety Rating, regional ranking, top 5 safest/most critical, top 5 improving/worsening
- **Map tab** — interactive choropleth map with tier filters and office location highlights
- **Full Table tab** — sortable table with Q1 2024 · Q1 2025 · Q1 2026 ratings, variation, and crime breakdown per DP

---

## Methodology

Full methodology available in `metodologia_safety_rating_sp.docx`.

Key parameters:
- **City Safety Rating:** log formula applied directly to the city's aggregate weighted score using official SEADE MSP population
- **Anchors:** 150 pts/100k = Safety 100 · 35,000 pts/100k = Safety 0
- **Comparison:** all periods use Q1 (Jan–Mar) for seasonal consistency

---

## Office Locations

| Office | Address | DP | Safety Rating |
|--------|---------|-----|---------------|
| HQ1 | R. Capote Valente, 39 — Pinheiros | 14º DP | 22.1 — Critical |
| HQ2 | R. Capote Valente, 120 — Pinheiros | 14º DP | 22.1 — Critical |
| HQ3 | R. Capote Valente, 210 — Pinheiros | 14º DP | 22.1 — Critical |
| Spark | Av. Manuel Bandeira, 360 — Vila Leopoldina | 91º DP | 27.9 — Critical |

---

*Data: SSP-SP · Population: SEADE · Analysis: own*
