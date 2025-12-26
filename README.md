![MIT License](https://img.shields.io/badge/license-MIT-green)
![Stars](https://img.shields.io/github/stars/tayabhavsar/School-Shooting-Prevention-Analysis---Sales-Enablement)

## School Safety Technology Sales Enablement Analysis

Data-driven insights to transform school safety technology sales cycles and prove ROI

## 📊 Project Overview
School safety technology companies face a critical challenge: 9-12 month sales cycles with <20% close rates due to inability to prove ROI. District leaders consistently ask: "What percentage of threats does your platform actually address?"
This analysis provides the answer using 20 years of incident data to quantify which threats behavioral monitoring platforms can address versus physical security measures.

## Business Problem:
- Sales teams forced into defensive selling and price concessions
- Customer success teams rely on surface-level metrics (alerts generated, reports submitted)
- No empirical data to answer: "Why invest in behavioral monitoring vs. physical security?"

The Solution: 
SQL-based analysis of 177 U.S. school shooting incidents (1999-2019) that quantifies addressable risk and provides data-driven sales enablement metrics.

## 🎯 Key Findings

| Finding | Metric | Business Impact |
|-------|--------|-----------------|
| **Internal Risk Dominance** | 71% of perpetrators are current students | Positions behavioral monitoring as the primary prevention investment |
| **Optimal Prevention Window** | 43% involve students aged 14–16 (96% current students) | Justifies high school–focused monitoring features |
| **Weapon Access Points** | 54% of firearms come from family/home environments | Validates anonymous reporting + family education bundling |
| **Market Segmentation** | Medium schools (500–1,500 students) account for 52% of incidents | Supports tiered pricing strategy by school size |
```
🗂️ Repository Structure
.
├── School_Shooting_Prevention_Analysis.sql    # Complete SQL analysis with annotations
├── School Safety Technology Sales Enablement Analysis.pdf    # Executive summary report
└── README.md                                   # This file
```
## 📊 Visual Insights
1. Internal vs. External Threat Profile
"https://github.com/tayabhavsar/School-Shooting-Prevention-Analysis---Sales-Enablement/blob/main/visualizations/Internal%20vs.%20External%20Threat.jpeg"


Sales Talking Point: "Physical security addresses external threats. Our data shows 71% of school shooters are current students already inside your building—behavioral monitoring is the primary prevention investment, not a nice-to-have. This pattern has remained stable for 20 years."



 2. Market Segmentation by School Size
<div align="center">
  <img src="visualizations/market_segmentation_school_size.jpeg" alt="School Size Analysis" width="900"/>
</div>


Pricing Strategy: "Medium-sized schools (500-1,500 students) represent 52% of incidents—your volume opportunity with standard pricing. Large schools (2,000+) show 2× higher casualties per incident—your premium enterprise tier with enhanced response protocols."


3. Weapon Sources & Prevention Pathways
<div align="center">
  <img src="visualizations/weapon_sources.jpeg" alt="Weapon Sources" width="900"/>
</div>


Product Bundling: "Anonymous reporting prevents the DEADLIEST attacks—friend-sourced weapons show 3× higher casualties (9.75 vs 2.89). Family education addresses 54% of weapon sources. Together, they create comprehensive prevention that physical security alone cannot provide."


## 🔍 Analysis Sections
1. Data Preparation & Cleaning

* NULL value handling for casualties data
* Calculated columns (total casualties, student shooter flags)
* Text field standardization (state codes, gender, school type)
* Analysis-ready view creation with era segmentation
  

 2. Exploratory Analysis

* Dataset summary and validation (177 incidents, 1999-2019)
* Year-over-year temporal trends
* Historical vs. modern era comparisons


 3. Prevention Opportunity Analysis (Core Sales Metrics)

* Student shooter prevalence: 71.2% known to schools
* Age distribution analysis: 14-16 age group = optimal intervention window
* Gender patterns: 95% male (stable across 20 years)
* Weapon sources: Family/home (54%), friends/peers (highest casualties)


 4. School Characteristics Analysis

* School type distribution (Public: 99% of incidents)
* School size correlation: Medium schools = volume opportunity, large schools = premium pricing
* Resource officer analysis (demonstrates selection bias awareness)


 5. Geographic Patterns

 * Top 10 states by incident frequency
* Modern era hotspots (frequency vs. severity analysis)
* Territory planning insights: CA, FL, TX = 28% of incidents


 6. Preventability Scoring

* Overall prevention opportunity: 70%+ of incidents show identifiable intervention points
* Era-based stability validation (patterns consistent 1999-2019)


 7. Data Quality & Validation

* Completeness assessment: Student relationship (99%), Age (100%), Gender (96%), Weapon source (39%)
Transparent limitation documentation


## 💡 Strategic Recommendations
1. Reframe Sales Positioning
Current State: Defensive selling focused on features
New Approach: Lead with addressable risk data

"Our threat assessment platform addresses the ACTUAL threat: 71% of school shooters are students you monitor daily. Physical security investments miss 7 out of 10 incidents because the threat is INTERNAL, not external."

2. Segment Pricing by School Size

Medium schools (500-1,500): Standard pricing, full features (52% of market)
Large schools (1,500+): Enterprise pricing, enhanced protocols (highest severity)
Small schools (<500): Simplified tiers

3. Shift Customer Success Metrics
Replace: Alerts generated, reports submitted
With: Estimated incidents prevented, benchmark alignment, ROI narratives
4. Bundle Around Three-Layer Prevention Model
Package together:

Student threat assessment
Anonymous peer reporting (addresses friend-sourced weapons = 3× higher casualties)
Family education (addresses 54% of weapon sources)


## 📈 Expected Impact

| Metric | Current | Expected with Implementation |
|------|---------|------------------------------|
| **Sales Cycle Length** | 9–12 months | 6–9 months |
| **Close Rate** | ~20% | 30–35% |
| **Renewal Rate** | Activity-based justification | Outcome-based retention |
| **Deal Size** | Price pressure | Premium positioning |


## 📝 Key Insights for Sales Presentations

| Insight | Statistic | Sales Implication |
|------|-----------|-------------------|
| **Internal Threat Dominance** | 71% of perpetrators are current students | Internal monitoring is more effective than perimeter security |
| **Optimal Intervention Age** | 43% are ages 14–16 | High school freshmen/sophomores are the highest-impact target group |
| **Student-Based Risk** | 96% of 14–16 year olds are current students | School-based monitoring is highly effective |
| **Weapon Access Source** | 54% of weapons come from family/home | Family education programs deliver strong ROI |
| **Severity Amplifier** | Friend-sourced weapons lead to 3× higher casualties | Anonymous reporting helps prevent worst-case outcomes |
| **Long-Term Validity** | Patterns stable over 20 years | Prevention strategy is durable and future-proof |

Sales Talking Points

"Why not just invest in physical security?"

Physical security addresses external threats. Our data shows 71% of school shooters are current students already inside your building. Behavioral monitoring addresses the actual threat profile.


"Can you quantify ROI?"

Based on 20 years of incident data, 70%+ of school shooting incidents show identifiable prevention opportunities through student threat assessment, anonymous reporting, and family education—the core features of our platform.


"Why focus on high school students?"

Ages 14-16 represent 43% of incidents, with 96% being current students. This is the optimal intervention window: highest frequency, nearly all are monitored students, and lower average casualties suggest early-stage planning that can be disrupted.


## 🤝 Future Framework
This analysis framework can be extended to:
* Additional time periods (2020-present)
* International incident databases
* Cross-platform effectiveness studies
* Predictive modeling for risk assessment

## 📊 Data Source
- Dataset: Washington Post School Shootings Database
- Period: 1999-2019
- Records: 177 incidents
- Completeness: Student relationship (99%), Age (100%), Gender (96%), Weapon source (39%)


## 🛠️ Technical Skills Demonstrated
Data Cleaning: NULL handling, text standardization, type conversions
SQL Techniques:

* Complex CASE statements for categorical grouping
* Window functions (PARTITION BY for percentages)
* CTEs and subqueries for complex calculations
* Pattern matching (LIKE, REGEXP)
* View creation for reusable queries
* Statistical Analysis: Temporal trends, correlation analysis, confounding variable identification
* Business Intelligence: Translating data into actionable sales/CS strategies

## 📄 License
MIT License - See LICENSE file for details

## 👤 Author
Taya Bhavsar
Data Analyst | SQL | Business Intelligence

## ⭐ Star this repo if you found it helpful!
Data-driven insights for school safety technology companies
