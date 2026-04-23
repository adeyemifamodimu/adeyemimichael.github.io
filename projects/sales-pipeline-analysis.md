This project presents a comprehensive Sales Pipeline Analysis for a B2B computer‑hardware company. The dataset combines information about accounts, products, sales teams, and sales opportunities, providing a unified view of the entire sales process — from client characteristics to product pricing, sales agent performance, and opportunity outcomes.

The goal of this project was to:

- Analyse pipeline quality and health
- Evaluate sales performance across teams and agents
- Understand product performance and pricing impact
- Assess client quality and revenue contribution
- Deliver actionable recommendations for stakeholders

The final solution is a multi‑page Power BI report structured into:
- Executive Overview
- Product Mix
- Team Performance
- Client Dynamics

End‑to‑End Data Preparation Process
This project followed a full BI lifecycle:
- Data sourcing
- Data profiling
- Data cleaning & standardisation
- Dimensional modelling
- Creating analytical SQL views
- Enforcing referential integrity
- KPI alignment
- Insight generation

Below is the detailed process.

Data Profiling & Quality Assessment
I began by profiling each table to understand structure, completeness, and potential issues.

- accounts (85 rows)
7 fields: account, sector, year_established, revenue, employees, office_location, subsidiary_of

Mostly complete except subsidiary_of (70 missing values)

- products (7 rows)
3 fields: product, sales_price, series

Fully complete

- sales_teams (35 rows)
3 fields: sales_agent, manager, regional_office

Fully complete

- sales_pipeline (8,800 rows)
8 fields: opportunity_id, sales_agent, product, account, deal_stage, engage_date, close_date, close_value

- Significant missing data:

account: 1,425 missing

engage_date: 500 missing

close_date: 2,089 missing

close_value: 2,089 missing

500 rows missing all three date/value fields

This profiling step guided the cleaning strategy and highlighted where business assumptions were needed.

2. Data Cleaning & Standardisation
Key cleaning actions:

- Standardising categorical values
- Replaced missing account values with a placeholder: “Dambase”

- Normalised product naming: GTXPro → GTX Pro

- Type conversions
year_established → INT

revenue → DECIMAL

employees → INT

sales_price → INT

engage_date, close_date → DATE

close_value → INT (after NULLIF to handle empty strings)

These conversions ensured consistency across the model and prevented aggregation issues in Power BI.

3️⃣ Dimensional Model Construction
I designed a star schema to support analytical queries and KPI consistency.

Dimension tables created
Dim_Managers

Extracted unique managers and regional offices

Assigned surrogate keys via IDENTITY

Dim_SalesAgents

Linked each sales agent to a manager using manager_id

Dim_Products

Loaded product, series, and price information

Dim_Accounts

Loaded account metadata including sector, revenue, employees, office location, and subsidiary information

Fact table
Renamed sales_pipeline → Fact_SalesPipeline

Added foreign keys:

sales_agent_id

product_id

account_id

Populated via joins to dimension tables

Dropped original text columns to avoid redundancy

4️⃣ Creating Analytical SQL Views
To provide clean, analysis‑ready layers for Power BI, I created SQL views:

Dim_AccountsVW

Dim_ProductsVW

Dim_SalesAgentsVW

Dim_ManagersVW

Fact_SalesPipeline_VW

These views abstracted raw complexity and ensured Power BI connected to curated, structured entities.

5️⃣ Enforcing Referential Integrity
Foreign key constraints were added to guarantee consistency:

Fact_SalesPipeline.sales_agent_id → Dim_SalesAgents.sales_agent_id

Fact_SalesPipeline.product_id → Dim_Products.product_id

Fact_SalesPipeline.account_id → Dim_Accounts.account_id

Dim_SalesAgents.manager_id → Dim_Managers.manager_id

This prevented orphaned records and ensured the semantic model was trustworthy.

6️⃣ Objectives, Key Questions & KPI Alignment
🔹 Analyse pipeline quality and health
Questions:

Is the pipeline healthy?

Are we winning enough?

Are we winning the right deals?

Is deal value rising or collapsing?

KPIs:

Win Rate

Deal Value Trend

Deal Count Trend

Average Deal Size

🔹 Evaluate sales performance across teams and agents
Questions:

Who is converting effectively?

Are agents winning high‑value deals or just high volumes?

Which agents drive revenue vs dilute it?

KPIs:

Win Rate by Agent

Deal Value by Agent

Average Deal Size by Agent

🔹 Understand product performance
Questions:

Which products generate value?

Which products dilute revenue?

How does pricing affect win rate?

Is the product mix healthy?

KPIs:

Deal Value by Product

Deal Count by Product

Average Deal Value by Product

Product Win Rate

Product Mix Contribution %

Price vs Win Rate Correlation

🔹 Evaluate client quality and revenue contribution
Questions:

Are we attracting high‑value clients?

How does client revenue size affect deal value?

How diversified is our client base?

KPIs:

Deal Value by Client Revenue Size

Win Rate by Sector

Win Rate by Geography

Average Deal Size by Client

📈 Key Insights Generated
⭐ 1. Pipeline quality is weak despite stable win rate
Win rate is stable at 48%, close to the 55% target

But deal value, deal count, and average deal size collapsed (−57% to −60%)

The issue is pipeline quality, not conversion efficiency

⭐ 2. Product mix is heavily skewed toward low‑value products
Low‑priced products (GTX Basic, MG Special) dominate volume

High‑value products (GTX 500) have very low volume

73% of revenue comes from the GTX series, but mostly from lower‑tier products

Pricing does not significantly reduce win rate → opportunity to push premium products

⭐ 3. Sales agents convert well but win low‑value deals
Many agents have win rates above 50%

But their wins are concentrated in low‑value opportunities

Example: Darcel Schlecht leads in deal value but averages only $3.3K per deal

⭐ 4. Client base is dominated by small‑revenue accounts
Larger clients generate bigger deals but represent a small share of the pipeline

Client revenue size correlates strongly with deal value

Geographic concentration is high — the US dominates, limiting diversification

🧭 Recommendations for Stakeholders
🔹 1. Improve pipeline quality
Strengthen qualification criteria

Reduce low‑value opportunities entering the pipeline

🔹 2. Shift focus to high‑value products
Incentivise sales teams to promote premium products

Provide targeted training on high‑value product positioning

🔹 3. Target higher‑value clients
Prioritise accounts with larger revenue size

Develop sector‑specific strategies for high‑value industries

🔹 4. Diversify geographically
Expand into markets with strong win rates (e.g., Panama, Germany)

Reduce over‑reliance on the US market

🛠️ Technical Skills Demonstrated
Power BI
Advanced DAX

Semantic modelling

Star schema design

Performance optimisation

Storytelling & UX design

SQL
Data cleaning & transformation

Creating analytical views

Enforcing referential integrity

Analytics
Trend & variance analysis

Segmentation (product, client, agent)

Correlation analysis

Root‑cause analysis
