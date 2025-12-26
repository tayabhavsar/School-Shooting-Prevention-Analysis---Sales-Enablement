School Shooting Prevention Analysis
A SQL-based business intelligence project quantifying prevention opportunities to enable data-driven sales strategies for school safety technology companies.
Show Image Show Image Show Image

The Business Problem
School safety technology companies face 9-12 month sales cycles and less than 20% close rates due to inability to prove ROI.
This analysis provides concrete statistics to demonstrate that behavioral monitoring platforms address the majority of actual threats (71% of shooters are current students), versus physical security investments that only address external risks.

Key Findings
Dataset: Washington Post School Shootings Database (1999-2019)
Records: 177 incidents analyzed
Data Quality: Student relationship (99%), Age (100%), Gender (96%), Weapon source (39%)
Executive Summary
MetricValueBusiness ImpactCurrent Students71.2%Threat assessment opportunityMinors Under 1880.2%Intervention authority existsAges 14-1642.9%Optimal intervention windowWeapons from Family/Home53.6%Secure storage opportunityMale Shooters95%Stable pattern for benchmarking
Primary Sales Talking Point

"Our platform addresses the ACTUAL threat: 71% of school shooters are students you monitor daily. Physical security investments miss 7 out of 10 incidents because the threat is INTERNAL, not external."


Technologies Used
Primary: MySQL, SQL
Key Technical Skills Demonstrated:

Data cleaning and standardization
Complex CASE statements for categorical grouping
Window functions (PARTITION BY)
CTEs (Common Table Expressions)
View creation for analysis-ready datasets
Temporal analysis and trend identification
Statistical calculations
Text pattern matching (LIKE, REGEXP)

Key Analytical Skills Demonstrated:

Critical thinking (identified selection bias in SRO analysis)
Business-focused insight generation
Data quality transparency
Market segmentation strategy
ROI quantification frameworks


Project Structure
school-shooting-analysis/
│
├── analysis.sql                      # Main analysis (fully documented)
│   ├── Section 1: Data Preparation & Cleaning
│   ├── Section 2: Exploratory Analysis
│   ├── Section 3: Prevention Opportunity Analysis
│   ├── Section 4: School Characteristics Analysis
│   ├── Section 5: Geographic Patterns
│   ├── Section 6: Preventability Scoring
│   └── Section 7: Data Quality & Validation
│
└── README.md                         # This file

Core Analyses
1. Prevention Opportunity Analysis
Finding: Student Shooter Prevalence
126 of 177 incidents (71.2%) involved current students. This pattern is stable across Historical (70.5%) and Modern (71.9%) eras.
Business Value: Proves behavioral monitoring addresses majority of threats
sqlSELECT 
    COUNT(*) as incidents,
    ROUND(COUNT(*) * 100.0 / 177, 1) as pct_of_all
FROM analysis_view
WHERE is_student_shooter = TRUE;
Finding: Age Distribution
Ages 14-16 represent 76 incidents (42.9%), with 96% being current students and average casualties of 1.68 (lower than other age groups).
Business Value: Identifies optimal intervention window
Finding: Gender Patterns
Male shooters represent 95% of incidents, stable across 20 years.
Business Value: Alert benchmarking for Customer Success teams
Finding: Weapon Sources
Family/Home sources represent 53.6% of known sources. Friends/Peers represent only 5.8% but show 3x higher casualties (9.75 vs 2.89).
Business Value: Justifies anonymous reporting features
2. Market Segmentation Strategy
School Type: Public schools = 99% of incidents (proportional to national enrollment)
School Size Correlation:

Medium (500-1500): 61 incidents (52%), avg 2 casualties → Standard pricing
Large/Very Large (1500+): 23 incidents (19%), avg 4 casualties → Premium pricing

Geographic Targeting:

California: 21 incidents, high frequency, lower severity → Volume play
Florida: 15 incidents, high severity (Parkland effect) → Premium positioning
Texas: 13 incidents, balanced pattern → Mixed approach

3. Critical Thinking Demonstration
Resource Officer Correlation Analysis
Initial finding: Schools with SROs show higher casualties
Deeper analysis reveals confounding variable:

SRO schools average 1,115 students
Non-SRO schools average 762 students (46% smaller)

Conclusion: Higher casualties reflect school size, not SRO ineffectiveness

This demonstrates the importance of controlling for confounding variables in analysis.


Quick Start
Prerequisites
bashMySQL 8.0+ or MariaDB 10.5+
Setup
Step 1: Create Database
sqlCREATE DATABASE school_shooting_prevention;
USE school_shooting_prevention;
Step 2: Import Data
Load your CSV data into the school_shootings table with required columns:

uid, school_name, city, state, date, year
killed, injured
age_shooter1, gender_shooter1, shooter_relationship1
weapon_source, school_type, enrollment, resource_officer

Step 3: Run Analysis
Execute analysis.sql sections sequentially (1-7).
Sample Queries
Student Shooter Rate by Era:
sqlSELECT 
    era_detailed, 
    COUNT(*) AS incidents, 
    SUM(CASE WHEN is_student_shooter THEN 1 ELSE 0 END) AS student_shooters,
    ROUND(SUM(CASE WHEN is_student_shooter THEN 1 ELSE 0 END) * 100.0 / COUNT(*), 1) AS pct
FROM analysis_view
WHERE year BETWEEN 1999 AND 2019
GROUP BY era_detailed
ORDER BY MIN(year);
Top 10 States:
sqlSELECT 
    state,
    COUNT(*) as incidents,
    SUM(total_casualties) as casualties
FROM analysis_view
WHERE is_modern = TRUE
GROUP BY state
ORDER BY incidents DESC
LIMIT 10;

Business Applications
Sales Enablement

ROI Proof: "70%+ of incidents show identifiable prevention opportunities"
Competitive Differentiation: Internal threat focus vs external security
Objection Handling: Data-backed responses

Customer Success

Alert Benchmarking: 95% male pattern for accuracy validation
Feature Prioritization: Anonymous reporting prevents highest-casualty incidents
Training Focus: Ages 14-16 represent optimal intervention window

Product Strategy

Market Segmentation: Medium schools (volume) vs Large schools (premium)
Feature Development: Family education modules
Partnership Opportunities: Anonymous reporting + secure storage bundling


Data Quality & Limitations
Completeness by Field
FieldCompletenessConfidence LevelStudent Relationship99%⭐⭐⭐⭐⭐Age100%⭐⭐⭐⭐⭐Gender96%⭐⭐⭐⭐⭐Weapon Source39%⭐⭐⭐
Known Limitations

2020-2024 Data Excluded: COVID-19 school closures and incomplete reporting
Weapon Source: Only 39% completeness limits weapon analysis confidence
Causality: This analysis identifies correlations, not causal relationships
Selection Bias: SRO analysis demonstrates need for controlling confounding variables


Portfolio Highlights
This project demonstrates:

Business Acumen: Translated technical analysis into sales-ready insights
SQL Proficiency: Complex queries, CTEs, window functions, view creation
Critical Thinking: Identified and explained selection bias in SRO analysis
Professional Documentation: Comprehensive commenting, clear structure
Data Quality Transparency: Honest about limitations and completeness
Strategic Thinking: Market segmentation, pricing strategy, territory planning


Data Source
Washington Post School Shootings Database

Comprehensive tracking of incidents since 1999
Includes shooter demographics, casualties, school characteristics
Publicly available for research purposes
Database Link


Future Enhancements

 Add Python visualization layer (matplotlib, seaborn)
 Integrate socioeconomic data
 Build interactive Tableau dashboard
 Develop machine learning risk prediction models
 Create time-series forecasting


Ethical Considerations
This analysis examines sensitive data related to real tragedies. The project is conducted with the following principles:

Prevention Focus: Identify patterns that inform evidence-based prevention strategies
Respectful Treatment: Each incident represents real lives affected
No Sensationalism: Professional tone, no graphic details
Transparency: Clear documentation of limitations
Purpose: Supporting legitimate safety technology companies


License
MIT License

Contact
Project by: [Your Name]
LinkedIn: [Your LinkedIn URL]
GitHub: [Your GitHub Profile]
Email: [Your Email]

Last Updated: December 2025

