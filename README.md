# DSA210

# Project Proposal: Impact of Visa Approval Rates on Tourism in Europe

# 1. Research Question

- How do visa approval and rejection rates affect tourist inflow in European countries?
This study aims to determine whether restrictive visa policies correlate with lower tourism numbers and how factors like safety, cost of living, and cultural significance influence this relationship.

# 2. Motivation

- Tourism is a major economic driver for many countries, yet restrictive visa policies can significantly impact the number of visitors a country receives. This project aims to analyze the relationship between visa approval/rejection rates and tourist inflow in European countries. By identifying patterns and correlations, the study will provide insights into how visa policies shape travel behaviors and tourism revenues.

# 3. Data Sources

The project will integrate two datasets:

* Visitor Visa Statistics Dataset

-- Source: visadata.csv
- Description: This dataset contains visa application data, including approval and rejection rates by country, consulate location, and year.
- Key variables:
- visitor_visa_applications: Total visa applications per country.
- visitor_visa_issued: Approved visas per country.
- visitor_visa_not_issued: Rejected visa applications.
-visitor_visa_refusal_rate: Visa rejection percentage.

* European Tour Destinations Dataset

-- Source: european-tour-destinations-dataset-metadata.csv
- Description: This dataset contains information on popular tourist destinations in Europe, including annual tourist arrivals, safety scores, cost of living, and cultural significance.
- Key variables:
Approximate Annual Tourists: Estimated number of tourists visiting each destination.
- Safety: Perceived safety level in the destination.
- Cost of Living: Economic affordability of the location.
- Cultural Significance: Historical and cultural importance.
- 
# 4. Methodology

The project will follow these key steps:
- Data Cleaning and Preprocessing
- Merge the visa dataset with the tourism dataset based on country.
- Handle missing values, normalize data, and perform outlier detection.
- Convert categorical variables (e.g., safety levels, cultural significance) into numerical representations.
- Exploratory Data Analysis (EDA)
- Distribution of visa rejection rates across countries.
- Relationship between visa approval rates and tourist arrivals.
- Correlation between visa policies, safety scores, and cost of living.
  
Hypothesis Testing

- Conduct a t-test or ANOVA to determine if there is a statistically significant difference in tourist numbers between countries with high and low visa rejection rates.
- Perform correlation analysis to check the strength of the relationship between visa rejection rates and tourist inflow.
 
Data Visualization

- Heatmaps to show visa rejection rates across Europe.
- Scatter plots and regression analysis for visa approval rates vs. tourism numbers.
- Time-series analysis (if applicable) to study trends over the years.
- Predictive Modeling (Optional)

- Build a regression model to predict expected tourist inflow based on visa policies, safety, and economic factors.
- Apply clustering techniques (e.g., K-Means) to categorize countries based on their tourism and visa policies.
  
# 5. Expected Findings

- Countries with higher visa rejection rates may have lower tourist arrivals, especially for non-EU visitors.
- Safety and cost of living may moderate the impact of visa restrictions—i.e., some tourists might still visit a country despite strict visa policies if the country is safe and affordable.
- Some countries may have high tourist numbers despite restrictive visas, likely due to visa exemptions for certain nationalities.

# 6. Limitations and Future Work

The dataset does not account for visa-free agreements (e.g., Schengen Visa).
External factors such as COVID-19 travel restrictions may distort recent visa statistics.
Future work could incorporate economic indicators (GDP, exchange rates) to refine insights on tourism demand.

# Project Phase 2 : EDA, and Hypothesis Testing

# Data Cleaning and Preprocessing

- Merged datasets on Country (standardized case/whitespace).
- Converted Safety and Cost of Living into ordinal numeric levels:
- Low = 1, Medium = 2, Medium-High = 3, High = 4
- Converted tourist counts from strings (e.g., "14 million") to numeric format.
- Dropped rows with missing or malformed critical values.
 
# Exploratory Data Analysis (EDA)

- Histogram: Visa Refusal Rates
o Right-skewed distribution
o Most countries have low refusal rates, indicating generally lenient visa
policies.
- Scatter Plot: Visa Refusal Rate vs. Tourist Volume
o Weak negative trend observed.
o Higher refusal rates tend to correspond with fewer tourists.
o Outliers present, but general pattern supports hypothesis.
- Correlation Heatmap
o Weak correlation between visa refusal rate and tourist volume (~ -0.02)
o Stronger correlations among visa metrics (e.g., issued vs. not issued)

# Summary of EDA Visual Findings:

• Countries with low visa refusal rates tend to receive more tourists.
• Most countries exhibit moderate to low visa refusal rates.
• Tourist volume is moderately influenced by cost and safety but these are not
dominant standalone predictors.
• Visa issuance and refusal metrics are highly internally correlated, confirming data
consistency.

# Hypothesis Testing

• Performed a two-sample t-test:
- Group 1: Countries with high visa refusal rates (above median)
- Group 2: Countries with low refusal rates (below median)
  
• Hypotheses:
- Null Hypothesis (H₀): There is no significant diXerence in tourist volumes
between countries with high and low visa refusal rates.
- Alternative Hypothesis (H₁): Countries with lower visa refusal rates have
significantly higher tourist volumes.

• Results:
- T-statistic = -17.14
- P-value = 1.03e-65
 
• Interpretation:
- The diXerence in tourist volume is statistically significant.
- Countries with lower visa refusal rates attract significantly more tourists.
  
# Key Insights

- Visa policy is a statistically significant factor influencing tourism.
- While not the only driver, more open visa regimes are associated with higher
tourist inflow.
- Clean preprocessing and categorical normalization were essential for valid
statistical inference.
- Visual patterns (e.g., scatter plots and histograms) further support statistical
findings.
- Technologies Used
• Python: Pandas, NumPy, Matplotlib, Seaborn, SciPy
• Environment: Jupyter Notebook

# Limitations and Future Work
• This project does not account for visa-free agreements like the Schengen Zone,
which may distort the relationship.
• External factors (e.g., pandemics, political instability) are not included but could
impact tourism.

# Future Improvements
• Extend the regression model to include Safety and Cost of Living.
• Add external datasets (e.g., GDP, exchange rates, travel warnings).
• Create interactive dashboards using Dash or Streamlit.
• Explore time-series trends if multi-year data becomes available.


