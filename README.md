# Marketing-Performance-Customer-Funnel-Analytics-Dashboard
This dashboard was built to analyze marketing performance and customer acquisition efficiency for a digital business. The goal was to enable data-driven decision-making across marketing spend, customer acquisition, and profitability.

# Objectives
Evaluate marketing efficiency using CAC and contribution profit
Track daily and trend-based performance of campaigns
Understand customer acquisition patterns across segments
Compare different attribution windows (7D, 30D, 365D)
Identify high-performing geographies and audience cohorts
Enable stakeholders to optimize budget allocation


 Data Sources Section 
1. GA4 Event Data (BigQuery Export)
User interactions (events, sessions)
Page views, conversions, engagement metrics
Event-level granularity

2. Marketing Spend Data

Platform-level ad spend (Facebook, Google, etc.)
Campaign and variation-level cost data

3. Session & Attribution Data

UTM parameters (source, medium, campaign)
Session-level variation mapping
Attribution windows (7D, 30D, 365D)

4. Derived / Modeled Tables (Built in BigQuery)

fact_funnel_combined → Funnel stage tracking
variation_spend_map → Spend allocation
session_variation_fact → Session-level attribution
ga4_page_performance_data → Performance metrics
