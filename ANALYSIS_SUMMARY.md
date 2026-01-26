# Michigan Maritime Supplier Discovery Analysis

## Executive Summary

This analysis identifies the gap between **certified maritime suppliers** and **potential suppliers** in Michigan's manufacturing base. Using BEA Input-Output tables to identify industries that supply inputs to boat building (NAICS 336612) and ship building & repair (NAICS 336611), combined with Census County Business Patterns data and class society certification records.

### Key Findings

| Metric | Value |
|--------|-------|
| Total Potential Supplier Establishments | **1,443** |
| Certified Maritime Suppliers | **19** (1.3%) |
| Untapped Potential | **1,424** |
| Supplier Industries Analyzed | 36 |
| Total Employment in Supplier Industries | 119,601 |

## Methodology

### 1. I-O Supply Chain Analysis
- Used BEA `supply_results.RDS` correlation matrix to identify industries that supply inputs to maritime industries
- Filtered to **positive correlations only** (industries with demonstrated supply relationships)
- Identified **28 supplier industries** for ship building and **17 for boat building** (36 unique total)

### 2. Michigan Establishment Counts
- Queried County Business Patterns (CBP) 2022 data for Michigan (FIPS 26)
- Mapped I-O industry codes to NAICS codes
- Aggregated establishments and employment at the 5-6 digit NAICS level

### 3. Certification Comparison
- Analyzed 81 certifications from 22 unique Michigan companies
- Mapped certification product types to supplier NAICS codes
- Calculated certification rates by industry

## Industry Gap Analysis

### High Certification Industries (>10%)
These industries have relatively good maritime certification penetration:

| Industry | Establishments | Certified | Rate |
|----------|----------------|-----------|------|
| Pumping equipment (333914) | 4 | 2 | 50.0% |
| Valves & fittings (33291A) | 18 | 7 | 38.9% |
| Engine equipment (333618) | 6 | 2 | 33.3% |
| Navigation instruments (334511) | 7 | 1 | 14.3% |

### Major Untapped Industries (0-5% certification)
These industries have significant potential but minimal maritime certification:

| Industry | Establishments | Certified | Untapped |
|----------|----------------|-----------|----------|
| Printing (323110) | 559 | 0 | 559 |
| Fluid power machinery (33399B) | 174 | 1 | 173 |
| Motor vehicle parts (336390) | 136 | 0 | 136 |
| Material handling equipment (333920) | 84 | 0 | 84 |
| Forging, stamping (33211A) | 85 | 2 | 83 |
| Electronic components (33441A) | 48 | 0 | 48 |

## Certified Michigan Companies

22 unique companies hold class society certifications:

1. **The Oilgear Company** (Traverse City) - Valves, Drilling Equipment
2. **Viking Corporation** (Hastings) - Fire Protection, Valves
3. **AlcoTec Wire Corporation** (Traverse City) - Welding Materials
4. **Blackmer/Dover** (Grand Rapids) - Pumps
5. **MP Pumps Inc** (Madison Heights) - Centrifugal Pumps
6. **DAVCO Technology** (Saline) - Fuel Filtration
7. **Yates Industries** (St. Clair Shores) - Hydraulic Cylinders
8. **World Tek Industries** (Romulus) - Diesel Engines
9. **Fireboy-Xintex** (Grand Rapids) - Fire Suppression
10. **Freudenberg Battery** (Midland) - Battery Systems

## Product Type Coverage

| Product Category | Certifications | Primary NAICS |
|-----------------|----------------|---------------|
| Valves | 26 | 33291A |
| Pumps | 13 | 333914 |
| Welding Materials | 10 | 33211A |
| Drilling Equipment | 7 | 333618 |
| Hydraulic Equipment | 4 | 33399B |
| Fire Protection | 4 | 33291A |
| Electrical Components | 2 | 334511, 335312 |

## Strategic Implications

### Supplier Development Opportunities

1. **Fluid Power (174 establishments)** - Michigan's automotive expertise in hydraulic systems translates directly to maritime applications. Only 1 certified company.

2. **Motor Vehicle Parts (136 establishments)** - Cross-over potential for precision machined components, electrical systems, and transmissions.

3. **Metal Fabrication (85 establishments)** - Forging, stamping, and sintering capabilities could serve hull fittings, deck hardware, and structural components.

4. **Material Handling (84 establishments)** - Cranes, hoists, and winches have direct maritime applications.

### Barriers to Entry

- Class society certification costs and complexity
- Maritime-specific material requirements (corrosion resistance)
- Qualification testing and documentation requirements
- Lack of awareness of maritime market opportunities

## Recommendations

1. **Targeted Outreach** - Focus on industries with >50 establishments and 0% certification rate
2. **Certification Pathway Programs** - Create streamlined certification support for automotive-to-maritime crossover
3. **Regional Clusters** - Leverage existing concentrations (Traverse City valves, Grand Rapids pumps)
4. **Matchmaking Events** - Connect shipbuilders with potential Michigan suppliers

## Data Sources

- **BEA Input-Output Tables** (2017) - Supply chain relationships
- **Census County Business Patterns** (2022) - Establishment counts
- **Class Society Certifications** - ABS, BV, ClassNK, DNV, KR, LR

## Files Generated

| File | Description |
|------|-------------|
| `michigan_maritime_suppliers.csv` | Full supplier industry list with MI establishments |
| `michigan_maritime_gap_analysis.csv` | Certification gap by industry |
| `michigan_certifications_clean.csv` | Cleaned certification data |
| `supplier_discovery_dashboard.html` | Interactive visualization |

---

*Analysis conducted: January 2026*
*Manufacturing Intelligence Platform | NO LAB Research*
