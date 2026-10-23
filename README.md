# Dutch Renewable Energy & Weather Analytics 🇳🇱

**Status:** 🚧 Work in progress

## Business question
How has renewable electricity production in the Netherlands evolved, and how do weather conditions affect wind and solar output?

## Data sources
| Dataset | Source | Granularity | License |
|---|---|---|---|
| Renewable electricity; production and capacity (`82610ENG`) | CBS StatLine | Annual, 1990–2025 | CC-BY 4.0 |
| Electricity balance sheet; supply and consumption (`84575ENG`) | CBS StatLine | Monthly, 1929–2026 | CBS |
| Weather observations | KNMI | Daily / monthly | Open data |

## Tech stack
Databricks (Unity Catalog) · PySpark · SQL · Power BI

## Project tickets
| Ticket | Description | Status |
|---|---|---|
| 001 | Profile the raw datasets | ✅ Done |
| 002 | Data quality assessment | 🔄 In progress |
| 003 | Data cleaning | ⏳ |
| 004 | Build analytical tables | ⏳ |
| 005 | KPI analysis (capacity factor) | ⏳ |
| 006 | Weather integration (KNMI) | ⏳ |
| 007 | Power BI dashboard | ⏳ |
| 008 | Final report | ⏳ |

## Key findings so far (TICKET-001)
- Monthly file mixes annual, quarterly and monthly rows, so naive sums would triple-count.
- Annual file is hierarchical (totals alongside components).
- All missing values traced to structural causes (technology not yet existing, interconnectors not yet built, provisional figures).
- Hidden trailing whitespace in 6 period labels would have silently dropped data during date parsing.

## Repository structure
```
notebooks/   Databricks notebooks, one per ticket
```
