# Michigan Maritime Supplier Discovery

An interactive dashboard analyzing the gap between certified maritime suppliers and potential manufacturing capacity in Michigan.

## Live Dashboard

**[View the Interactive Dashboard](https://nosheal.github.io/michigan-maritime/)**

## Key Findings

| Metric | Value |
|--------|-------|
| Total Potential Suppliers | **1,443** establishments |
| Certified Maritime Suppliers | **19** (1.3%) |
| Untapped Potential | **1,424** establishments |
| Supplier Industries Analyzed | 36 |

Michigan has over **1,400 manufacturing establishments** that produce inputs for the shipbuilding and boat building industries but lack class society certification. These represent significant opportunities for supplier diversification and regional supply chain development.

## Methodology

1. **Supply Chain Mapping** - Used BEA Input-Output tables to identify industries that supply inputs to:
   - Ship Building & Repair (NAICS 336611)
   - Boat Building (NAICS 336612)

2. **Establishment Analysis** - Queried Census County Business Patterns (2022) for Michigan establishments in supplier industries

3. **Certification Comparison** - Analyzed class society certifications (ABS, DNV, BV, ClassNK, KR, LR) for Michigan companies

## Top Opportunity Industries

Industries with significant manufacturing capacity but minimal maritime certification:

| Industry | MI Establishments | Certified | Gap |
|----------|-------------------|-----------|-----|
| Printing | 559 | 0 | 559 |
| Fluid Power Machinery | 174 | 1 | 173 |
| Motor Vehicle Parts | 136 | 0 | 136 |
| Material Handling Equipment | 84 | 0 | 84 |
| Forging & Stamping | 85 | 2 | 83 |

## Data Files

| File | Description |
|------|-------------|
| `index.html` | Interactive dashboard (GitHub Pages) |
| `ANALYSIS_SUMMARY.md` | Detailed methodology and findings |
| `michigan_maritime_suppliers.csv` | Supplier industries with MI establishment counts |
| `michigan_maritime_gap_analysis.csv` | Certification gap by industry |
| `michigan_certifications_clean.csv` | Class society certification records |

## Data Sources

- **BEA Input-Output Tables** (2017) - Inter-industry supply relationships
- **Census County Business Patterns** (2022) - Establishment counts by NAICS
- **Class Society Certifications** - ABS, BV, ClassNK, DNV, KR, LR approval records

## About

This analysis is part of the [Manufacturing Intelligence Platform](https://github.com/nosheal) research initiative, exploring regional manufacturing capabilities and supply chain opportunities.

---

*NO LAB Research | January 2026*
