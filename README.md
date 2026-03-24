# Marketing-Performance-Customer-Funnel-Analytics-Dashboard
This dashboard was designed as an executive view of marketing performance, helping stakeholders track spend efficiency, customer acquisition, and profitability trends on a daily basis.
It combines high-level KPIs, trend analysis, and granular daily breakdowns in a single view to support quick decision-making.

<img width="1920" height="1080" alt="@jyotiprakash" src="https://github.com/user-attachments/assets/4df66d06-fc89-4819-8c54-735739022396" />

# Business Requirement
The marketing team needed:
- A single source of truth for daily performance tracking
- Clear visibility into:
 - How much we are spending?
 - How many customers we are acquiring?
 - Whether campaigns are profitable?
- Ability to quickly identify good vs bad performing days
- A way to compare CAC vs revenue/profit in real time

Objective of This Dashboard

- Monitor marketing efficiency (CAC vs Profit)
- Track daily performance trends
- Identify high-performing and underperforming days
- Enable data-driven budget allocation decisions
- Provide actionable insights without needing SQL/technical knowledge


 # Visualizations details:

1. KPI Cards (Top Section)
- Spend
- New Customers
- CAC
- Contribution Profit

Purpose:
- Instant snapshot of overall performance
- Helps leadership quickly assess:
- Are we profitable?
- Are we scaling efficiently?

2. Trend Lines (Top Right)

- Spend trend
- Contribution profit trend
- CAC trend

Purpose:
Identify:
- Performance spikes/drops
- CAC fluctuations
- Profit consistency

Detect campaign fatigue or scaling issues

3. Multi-Metric Performance Chart (Center)

Combines:
CAC
Contribution Profit per Customer
AOP / APRP (value metrics)
New customers trend

Purpose:
Compare cost vs value in a single visual

Understand:
Are we acquiring valuable customers or just volume?

4. Customer Data Quality (Left Donut Chart)

Shows:
Matched vs unmatched users
Missing attributes (age, gender, etc.)

Purpose:
Evaluate data reliability
Identify tracking gaps

Business Impact:
Helps team improve data quality & tracking setup

5. Daily Performance Table (Core Visual)
This is the most important part of the dashboard
Includes:
- Spend % contribution
- New customers
- Contribution profit
- Normalized contribution profit
- CAC
- Contribution profit per customer
- AOP / APRP
- Normalization multiplier

Features:
Conditional formatting (data bars)
Easy comparison across days

Purpose:
Identify:
- Best performing days
- Inefficient spend days
- Profitability trends

Business Use:
- Helps marketing team:
- Optimize daily budgets
- Pause low-performing campaigns

6. Slicers & Filters
- Date range
- Platform
- Age group
- Gender
- Product / Territory

Purpose:
Drill-down capability for:
- Campaign-level insights
- Audience-level performance

# Data Sources Used

1. GA4 Event Data (BigQuery)
- User sessions
- Conversions
- Event-level tracking
- Demographics (age, gender)

Role:
Provided customer behavior and conversion data

2. Marketing Spend Data
Platform-level spend (Google, Meta, etc.)
Campaign/variation level cost
Data is processed and stored in SQL server

Role:
Enabled CAC and ROI calculations

4. Session & Attribution Mapping
UTM parameters (source, medium, campaign)
Session-to-campaign mapping
Data is processed and stored in SQL server

Role:
Connected spend with actual user acquisition

4. Derived Tables (Built in BigQuery)
Session-level aggregated data
Daily performance tables
Attribution-adjusted datasets

Role:
Improved performance and enabled fast reporting in Power BI

How This Was Built ?

-Extracted GA4 data from BigQuery (events_*)
-Flattened event parameters into structured columns
-Built session-level datasets
-Joined with marketing spend using:
 -UTM parameters
 -Variation mapping

Created aggregated daily fact tables
Built DAX measures for:
 -CAC
 -Contribution profit
Normalized metrics
Designed Power BI visuals with:
- Conditional formatting
- Dynamic filters

Impact on the Team
- Provided a centralized performance dashboard
- Reduced dependency on manual reporting / SQL queries
- Enabled faster decisions on:
 - Budget allocation
 - Campaign optimization
- Improved visibility into:
 - Profitability (not just spend)
- Helped identify:
 - High CAC days
 - Low ROI campaigns
