🎯 School Shooting Prevention Analysis
Show Image
Show Image
Show Image

A SQL-based business intelligence project quantifying prevention opportunities in school shooting incidents to enable data-driven sales strategies for school safety technology companies.

📊 Project Overview
This project analyzes 177 school shooting incidents from 1999-2019 to identify patterns that enable data-driven sales strategies for school safety technology companies. Using comprehensive SQL analysis, I discovered that 71% of school shooters are current students known to the school, proving behavioral monitoring platforms address the majority of threats versus physical security that only addresses external risks.
The Challenge: School safety tech companies face 9-12 month sales cycles and <20% close rates due to inability to prove ROI. Can data mining provide the evidence needed to accelerate sales?
🎯 Key Results

71.2% of shooters were current students - High prevention opportunity through behavioral monitoring
80.2% were minors under 18 - Intervention authority exists
42.9% occurred in ages 14-16 - Optimal intervention window identified
53.6% of weapons from family/home - Safe storage education opportunity
95% male pattern stable across 20 years - Reliable benchmarking for alert systems
Pattern stability validated - Historical (70.5%) vs Modern (71.9%) eras show consistency

🔍 Research Questions Answered

What percentage of shooters are students known to the school?
✅ 71.2% - enabling threat assessment and early intervention programs
What age group represents the highest prevention opportunity?
✅ Ages 14-16 (96% are students, lower casualties suggest early-stage planning)
Are patterns stable enough to guide long-term product strategy?
✅ Yes - 71% rate consistent across two decades (1999-2019)
Which states should sales teams prioritize?
✅ California (high frequency), Florida (high severity), Texas (balanced)

📁 Repository Structure
School-Shooting-Prevention-Analysis/
├── README.md                         # Project overview and documentation
├── LICENSE                           # MIT License
│
├── analysis.sql                      # Complete SQL analysis (7 sections)
│   ├── Section 1: Data Preparation & Cleaning
│   ├── Section 2: Exploratory Analysis
│   ├── Section 3: Prevention Opportunity Analysis
│   ├── Section 4: School Characteristics Analysis
│   ├── Section 5: Geographic Patterns
│   ├── Section 6: Preventability Scoring
│   └── Section 7: Data Quality & Validation
│
└── data/
    └── README.md                     # Data dictionary and preprocessing notes
Key Files

analysis.sql: Fully documented SQL analysis with business context and sales talking points
README.md: Complete project documentation with methodology and results
LICENSE: MIT License for open-source usage

Usage
All analysis can be reproduced by running analysis.sql sections sequentially in MySQL Workbench or any MySQL client. See Quick Start section below for setup instructions.
🚀 Getting Started
Prerequisites

Database: MySQL 8.0+ or MariaDB 10.5+
Client: MySQL Workbench, DBeaver, or command line
Dataset: Washington Post School Shootings Database (1999-2019)

Installation
sql-- Step 1: Create database
CREATE DATABASE school_shooting_prevention;
USE school_shooting_prevention;

-- Step 2: Import your CSV data into school_shootings table
-- Required columns: uid, school_name, city, state, date, year,
--                   killed, injured, age_shooter1, gender_shooter1,
--                   shooter_relationship1, weapon_source, school_type,
--                   enrollment, resource_officer

-- Step 3: Run analysis.sql sections sequentially
Quick Start
sql-- Clone the repository
git clone https://github.com/tayabhavsar/School-Shooting-Prevention-Analysis---Sales-Enablement.git
cd School-Shooting-Prevention-Analysis---Sales-Enablement

-- Open analysis.sql in MySQL Workbench and run sections 1-7 in order
Running the Analysis
sql-- Section 1: Clean and standardize data
-- Section 2: Exploratory analysis
-- Section 3: Prevention opportunity scoring (KEY FINDINGS)
-- Section 4: Market segmentation analysis
-- Section 5: Geographic targeting strategy
-- Section 6: Overall preventability assessment
-- Section 7: Data quality validation
📈 Core Analyses & Findings
1. Prevention Opportunity Analysis
Finding: Student Shooter Prevalence
126 of 177 incidents (71.2%) involved current students. Pattern is remarkably stable across Historical (70.5%) and Modern (71.9%) eras.
sqlSELECT 
    COUNT(*) as incidents,
    ROUND(COUNT(*) * 100.0 / 177, 1) as pct_of_all
FROM analysis_view
WHERE is_student_shooter = TRUE
  AND year BETWEEN 1999 AND 2019;
Business Impact: Proves behavioral monitoring addresses the ACTUAL threat (internal) vs physical security (external)
Finding: Age Distribution
Age GroupIncidents% of Total% StudentsAvg Casualties14-16 (High School)7642.9%96%1.6817-18 (H.S. Senior)4022.6%88%2.1519-21 (College)2413.6%42%3.25Under 14 (Elementary)2111.9%81%1.9522+ (Adult)169.0%19%2.56
Business Impact: Ages 14-16 represent optimal intervention window (highest frequency, nearly all students, lower casualties)
Finding: Weapon Sources
SourceIncidents% of KnownAvg CasualtiesFamily/Home3753.6%2.89Friends/Peers ⚠️45.8%9.75Other2231.9%2.45Purchased by Shooter34.3%3.67Stolen34.3%2.33
Business Impact:

Family/Home = largest source → Safe storage education opportunity
Friends/Peers = 3x higher casualties → Anonymous reporting critical for preventing deadliest attacks

2. Market Segmentation Strategy
School Size Correlation
School SizeIncidents% of TotalAvg CasualtiesStrategyMedium (500-1500)6152%2Volume play - Standard pricingLarge/Very Large (1500+)2319%4Premium - Enterprise pricingSmall (<500)3429%2Standard pricing
Geographic Targeting
StateIncidentsCasualties/IncidentStrategyCalifornia212.4High frequency → Volume playFlorida155.0High severity → Premium positioningTexas133.5Balanced → Mixed approachWashington72.3StandardPennsylvania71.9Standard
Top 3 states = 28% of all incidents
3. Critical Thinking Demonstration
Resource Officer Correlation Analysis
Initial Finding: Schools with SROs show higher casualties
Deeper Analysis Reveals Confounding Variable:

SRO schools average 1,115 students
Non-SRO schools average 762 students (46% smaller)

Conclusion: Higher casualties reflect school size, not SRO ineffectiveness

This demonstrates the importance of controlling for confounding variables in analysis—a key skill for data-driven decision making.

📊 Data Quality & Limitations
Completeness by Field
FieldCompletenessConfidence LevelStudent Relationship99%⭐⭐⭐⭐⭐Age100%⭐⭐⭐⭐⭐Gender96%⭐⭐⭐⭐⭐Weapon Source39%⭐⭐⭐
Known Limitations

Geographic scope: United States only
Temporal coverage: 1999-2019 (2020-2024 excluded due to COVID-19 closures)
Weapon source: Limited completeness (39%) constrains weapon analysis confidence
Causality: Analysis identifies correlations, not causal relationships
Quality range: Dataset quality is high but some fields have missing values

🛠️ Technical Skills Demonstrated
SQL Proficiency
✅ Complex CASE statements for categorical grouping
✅ Window functions (PARTITION BY for within-group calculations)
✅ CTEs (Common Table Expressions) for readability
✅ View creation for analysis-ready datasets
✅ Temporal analysis with era segmentation
✅ Text pattern matching (LIKE, REGEXP)
✅ Aggregate functions with statistical calculations
✅ Data cleaning and standardization
Analytical Skills
✅ Critical thinking (selection bias identification)
✅ Business-focused insight generation
✅ Market segmentation strategy development
✅ ROI quantification frameworks
✅ Data quality transparency and documentation
✅ Statistical validation (percentages, averages, distributions)
💼 Business Applications
Sales Enablement
Primary Talking Point:

"Our platform addresses the ACTUAL threat: 71% of school shooters are students you monitor daily. Physical security investments miss 7 out of 10 incidents because the threat is INTERNAL, not external."

Supporting Data:

ROI Proof: "70%+ of incidents show identifiable prevention opportunities"
Competitive Differentiation: Internal threat focus vs external security
Objection Handling: Data-backed responses to "physical security is enough"

Customer Success

Alert Benchmarking: 95% male pattern for accuracy validation
Feature Prioritization: Anonymous reporting prevents highest-casualty incidents (9.75 vs 2.89 casualties)
Training Focus: Ages 14-16 represent optimal intervention window

Product Strategy

Market Segmentation: Medium schools (volume) vs Large schools (premium)
Feature Development: Family education modules (54% weapon source)
Partnership Opportunities: Anonymous reporting + secure storage bundling

📚 Dataset
Source: Washington Post School Shootings Database
Time Period: 1999-2019
Samples: 177 incidents
Features: 11+ variables including demographics, casualties, school characteristics
Target: Prevention opportunity identification
Citation:

Washington Post School Shootings Database
Comprehensive tracking of incidents since 1999
Publicly available for research purposes

Access: Washington Post Database
🔬 Methodology Highlights
✅ Rigorous data cleaning with NULL handling
✅ Era segmentation for temporal validation
✅ Comprehensive market segmentation analysis
✅ Multi-dimensional prevention opportunity scoring
✅ Confounding variable identification (SRO analysis)
✅ Geographic pattern analysis for territory planning
✅ Statistical validation with percentages and confidence checks
✅ Business-focused interpretation throughout
🔮 Future Enhancements

 Add Python visualization layer (matplotlib, seaborn, Plotly)
 Integrate socioeconomic and mental health data
 Build interactive Tableau/Power BI dashboard
 Develop machine learning risk prediction models
 Create time-series forecasting for resource planning
 Expand analysis to include 2020-2024 data

⚠️ Ethical Considerations
This analysis examines sensitive data related to real tragedies. The project is conducted with the following principles:

Prevention Focus: Identify patterns that inform evidence-based prevention strategies
Respectful Treatment: Each incident represents real lives lost or affected
No Sensationalism: Professional tone, no graphic details
Transparency: Clear documentation of limitations and data quality
Purpose: Supporting legitimate safety technology companies that save lives

📝 License
This project is licensed under the MIT License - see the LICENSE file for details.
👤 Author
Taya Bhavsar

📧 Email: [tayab492@gmail.com]
💼 LinkedIn: linkedin.com/in/yourprofile
🐙 GitHub: @tayabhavsar

🙏 Acknowledgments

Washington Post for providing comprehensive school shooting data
UCI Machine Learning Repository for data science methodology guidance
SQL and data analysis community for best practices


⭐ If you found this analysis insightful, please consider giving it a star!
📫 Questions or collaboration opportunities? Feel free to open an issue or reach out directly.
📈 Portfolio Highlights
This project demonstrates:

Business Acumen: Translated technical analysis into sales-ready insights
SQL Mastery: Complex queries, CTEs, window functions, view creation
Critical Thinking: Identified and explained selection bias in SRO analysis
Professional Documentation: Comprehensive commenting throughout codebase
Data Quality: Transparent about limitations and completeness
Strategic Thinking: Market segmentation, pricing strategy, territory planning

