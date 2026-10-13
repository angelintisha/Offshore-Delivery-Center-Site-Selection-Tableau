# Offshore Delivery Center Site Selection — Tableau Decision Dashboard

**Strategic decision analysis**

📊 [Interactive Dashboard (Tableau Public)](https://public.tableau.com/views/CountryReadinessDashboardXYZOffshoreDeliveryCenter/ExecutiveDashboard) · 📄 [Final Report (PDF)](Strategic_Decision_Report.pdf) · 📄 [Proposal (PDF)](Strategic_Decision_Proposal.pdf)

[![Country Readiness Dashboard](https://public.tableau.com/static/images/Co/CountryReadinessDashboardXYZOffshoreDeliveryCenter/ExecutiveDashboard/1.png)](https://public.tableau.com/views/CountryReadinessDashboardXYZOffshoreDeliveryCenter/ExecutiveDashboard)

*Click the image to open the interactive dashboard and adjust the pillar weights.*

---

## Overview

XYZ Clinical Data Solutions, a hypothetical U.S. clinical data management company, is evaluating its first offshore delivery center of 50–75 staff to handle data cleaning, query management, and medical coding. Because the center would handle regulated patient data, the location decision depends on talent, data security, digital infrastructure, and openness to foreign investment, not cost alone.

This project built a data-driven framework in Tableau to compare 43 candidate countries and produce a defensible shortlist for due diligence.

## Approach

- **Data:** OECD Going Digital Toolkit, using standardized 0–100 Distance scores so indicators in different units can be combined
- **Framework:** Nine core indicators organized into four strategic pillars: Talent & Workforce, Trust & Data Security, Business Digital Infrastructure, and Market Openness
- **Scoring:** Pillar scores built with level-of-detail expressions; a weighted composite readiness score controlled by parameter sliders
- **Sensitivity testing:** Rankings recalculated under four weighting scenarios to separate robust candidates from those that suit only one set of priorities
- **Segmentation:** K-means clustering on pillar scores grouped 31 fully scorable countries into three strategic profiles
- **Risk screening:** A two-tier screen separating observed weakness (OECD bottom rankings, bottom-quartile pillars) from missing data
- **Supplementary data:** English proficiency (EF EPI 2025) and time-zone overlap with U.S. Eastern hours

## Data Validation

- Deduplicating 42 double-classified country–indicator records moved one country from sixth to fourth in the ranking
- Separating evidence gaps from risk reduced flagged countries from 25 to 16
- Cluster assignments were independently reproduced outside Tableau with identical results
- Re-running the ranking on the 24 countries with complete data left the top four unchanged

## Key Findings

- **Shortlist:** Finland, Sweden, and Ireland — high composite scores, complete data, no risk flags, and stable across weighting scenarios
- **Conditional:** Korea (strong overall but OECD bottom-ranked on digital services exports, the indicator most tied to cross-border delivery) and Estonia (balanced profile, potential cost advantage pending labor-cost data)
- **Evidence gaps:** 12 countries, including India, Brazil, Colombia, and Costa Rica, could not be ranked due to OECD coverage gaps rather than weak performance; the report recommends supplementary data before excluding them

## Data Sources

- [OECD Going Digital Toolkit](https://goingdigital.oecd.org)
- [EF English Proficiency Index](https://www.ef.com/epi)
