---
layout: default
title: Client Portfolio Analysis
---

# Client Portfolio Analysis  
**End‑to‑End BI Solution for AUM Decline, Fee Leakage & Adviser Performance**

<iframe title="Portfolio Analytics" width="600" height="373.5" src="https://app.powerbi.com/view?r=eyJrIjoiMzc4OGQ4OWUtZjgwNC00ZjY5LTk0YjktNjE2YjZiNTliMmExIiwidCI6IjhlYzBiZGRhLWViMTEtNDk4ZS04NmUzLWJjYzk4ZjEwOWFiYiJ9" frameborder="0" allowFullScreen="true"></iframe>
---

## Project Overview

This project presents a **three‑page Client Portfolio Analysis Dashboard** built to give senior leadership a complete, data‑driven understanding of portfolio health. The solution integrates **AUM trends, client churn, fee performance, and adviser accountability** into a single, interactive BI experience.

The dashboard was designed to move users seamlessly from **high-level portfolio trends** to **client-level root causes** and finally to **adviser/team performance insights**. It supports:

- Executive decision‑making
- Revenue protection and fee optimisation
- Client retention strategy
- Adviser and team performance management
- Early detection of portfolio risks

Built in **Power BI**, the solution leverages robust **data modelling**, advanced **DAX**, and automated **Power Query** transformations to deliver a **scalable, filter‑aware, drill‑safe analytics environment**.

---

## Business Problem

The organisation was experiencing a rapid deterioration in portfolio performance but lacked the visibility to understand why. Key challenges included:

- A significant decline in Assets Under Management (AUM)
- A sharp reduction in fee income, despite stable pricing policies
- No clear view of which clients, advisers, or teams were driving losses
- Fragmented Excel‑based reporting with no auditability or drill‑down capability
- Inability to distinguish between market-driven effects and client attrition

Leadership needed a unified BI solution to answer critical questions:

- Why is AUM declining so sharply?
- Which clients are leaving, and what is their impact?
- Where is fee leakage occurring across the portfolio?
- Who owns the problem — advisers, teams, or regions?
- How do we prioritise retention, pricing, and performance interventions?

---

## Solution Architecture

The solution was built using a modern BI architecture designed for performance, clarity, and scalability:

- **Power BI** for interactive reporting and narrative storytelling
- **Star-schema data model** optimised for speed and drill‑down
- **Advanced DAX** for YoY growth, variance, CAGR, contribution analysis, and ranking logic
- **Power Query** for data cleansing, shaping, and automated refresh
- Role‑driven navigation across three analytical layers:
  - Portfolio Overview
  - Fee Performance
  - Adviser & Team Performance

---

## Page 1 – Portfolio Overview (AUM & Client Dynamics)

### Key Insights Delivered

- Current AUM: £28M
- CAGR (1990–2025): 9.7%
- Latest YoY AUM Change: –73.1%
- Clear identification of the AUM peak, followed by a sharp structural decline
- Parallel drop in client volume confirming client churn as the primary driver

### Analytical Focus

- Long‑term AUM trend with YoY growth overlay
- Client volume trend vs AUM movement
- Client‑level contribution to the £76M AUM decline
- Dynamic filtering by Year, Adviser, Adviser Team, Investment Manager

### Value

This page enabled leadership to **pinpoint the turning point** in portfolio performance and distinguish between **market effects and client attrition‑driven decline**.

---

## Page 2 – Fee Performance & Revenue Leakage

### Key Insights Delivered

- Effective Fee Rate: 0.52% (above 0.50% policy target)
- Actual Fee Growth YoY: –68.9%
- Management Fee Variance: –£11M

### Analytical Focus

- Comparison of standard vs actual management fees
- Identification of clients responsible for £11M in lost fees
- Fee leakage analysis highlighting high‑AUM, low‑efficiency clients
- Bubble analysis exposing pricing inefficiencies masked by headline AUM

### Value

The analysis demonstrated that the revenue decline was not pricing‑related, but driven by:

- Client exits
- Sub‑optimal fee realisation
- Concentration risk in a small number of large clients

This page provided a **clear roadmap for fee recovery and pricing discipline**.

---

## Page 3 – Adviser & Team Performance

### Key Insights Delivered

- Fee Efficiency: –98.6%
- AUM per Adviser: £19.6M
- AUM per Adviser Team: £221M

### Analytical Focus

- Top advisers by AUM and fee contribution
- Identification of advisers and teams driving portfolio contraction
- Discretionary vs non‑discretionary control analysis
- Adviser‑level fee efficiency vs revenue contribution

### Value

This page provided management with **clear accountability**, enabling:

- Targeted adviser interventions
- Performance‑based coaching
- Team‑level strategic decisions
- Identification of high‑risk books requiring oversight

---

## Key DAX & Metrics Implemented

- YoY Growth %
- CAGR
- AUM Variance
- Fee Variance vs Policy
- Contribution % to Total Decline
- Fee Efficiency %
- Client & Adviser Ranking Logic

All measures were designed to remain **filter‑aware, drill‑safe, and hierarchy‑consistent** across the entire model.

---

## Business Impact

- Replaced fragmented Excel reporting with a **single executive BI solution**
- Enabled rapid identification of loss drivers at client, adviser, and team level
- Improved confidence in financial and performance reporting
- Provided a scalable framework for ongoing portfolio monitoring
- Strengthened pricing governance and adviser accountability
- Supported strategic decisions around retention, coaching, and revenue protection

---

## Tools & Technologies

- **Power BI** (DAX, Data Modelling, Power Query)
- **SQL** (Views, Aggregations, ETL)
- **Data Governance & Validation**
- **Stakeholder‑Centric Dashboard Design**

---

[Back to Projects](../projects)
