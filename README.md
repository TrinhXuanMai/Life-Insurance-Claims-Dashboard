# Life Insurance Claim Settlement Performance Dashboard

![Dashboard Screenshot](dashboard_screenshot.png)

## Project Overview
This project analyzes the death claim settlement performance of 18 Indian life insurers over 5 fiscal years (FY2018–FY2022), using publicly available IRDAI disclosure data. The dashboard simulates the market comparison and performance monitoring workflow typically conducted in a Product or Business Analysis role at a life insurance company.

## Tools & Technologies
- **Microsoft Excel:** Data Aggregation, Conditional Formatting (Color Scale), Basic Charting (Bar, Line, Clustered Column), Dashboard Layout Design
- **Data Source:** IRDAI (Insurance Regulatory and Development Authority of India) via Kaggle

## Dataset
| File | Description |
|---|---|
| `cleaned_individual_death_claims.csv` | Individual life policies (term, endowment) — 18 insurers × 5 fiscal years |
| `cleaned_group_death_claims.csv` | Group policies (employer-employee, credit life) — 18 insurers × 5 fiscal years |

**Key Metrics:** Claims Intimated, Claims Paid, Amount Paid (INR Cr), Settlement Ratio, Repudiation Ratio, Pending Ratio

## Data Cleaning
1. **Removed aggregate rows** — Excluded "Industry Total" and "Private Total" to prevent distortion in insurer-level rankings.
2. **Standardized insurer names** — Resolved duplicate short/full name entries (e.g., "HDFC" vs "HDFC Life").
3. **Corrected Sahara Life ratio** — Original source recorded ratio = 0 despite valid claim counts; recalculated manually as `Claims Paid / Claims Intimated`.

## Dashboard Structure
- **`Individual_Data` & `Group_Data`:** Cleaned data with color-scale conditional formatting on Settlement Ratio (Red → Yellow → Green).
- **`Analysis`:** Insurer rankings, YoY industry trend, Individual vs Group comparison.
- **`Dashboard`:** Executive summary with KPI scorecards and 3 charts:
  - Top 5 insurers by average settlement ratio
  - Industry settlement ratio trend (FY18–FY22)
  - Individual vs Group settlement ratio by year

## How to View
1. Download `Life_Insurance_Claims_Dashboard.xlsx` from this repository.
2. Open with Microsoft Excel.
3. Navigate to the **Dashboard** tab for the executive summary.
4. Navigate to the **Analysis** tab to view the background calculations and data aggregation.

## Key Findings
- **Max Life ranked #1** with 98.89% average settlement ratio — the most reliable insurer for individual policyholders across all 5 years.
- **Industry improved +4.22pp** from FY18 (94.31%) to FY22 (98.53%), driven by regulatory pressure and market competition.
- **COVID-19 Resilience (FY21):** Claims volume spiked +28.6% (83,837 → 112,806 intimated), yet the settlement ratio continued improving — demonstrating strong operational scalability under crisis conditions.
- **Individual vs Group:** Individual policies consistently exhibit a higher settlement ratio than Group policies (outperforming by ~2-5.5pp in 4 out of 5 years). This suggests stronger underwriting protocols and regulatory scrutiny for individual retail products compared to bulk group schemes.

## Business Implications
- Settlement ratio is a key product reliability signal — top performers (Max Life, Tata AIA, HDFC Life) can leverage these metrics in bancassurance partnerships and agency distribution.
- The ~6pp gap between top and bottom performers (98.89% vs 92.88%) signals significant room for operational improvement among mid-tier insurers.

---
