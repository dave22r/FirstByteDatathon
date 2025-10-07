# FlexField Fitness Strategic Partnership Analysis | Datathon Semi-Finalist

## Project Overview
Data-driven analysis to identify the optimal strategic partnership for FlexField Fitness, a declining gym chain facing customer retention challenges. Analyzed 3,494 customer records across four potential partners (Chef's Meal, PulseGear, CoreBoost) to recommend a partnership strategy that addresses 30% membership dropout rates.

## Business Problem
FlexField Fitness experienced declining membership due to competition from budget gyms and digital platforms like Peloton. The company needed to determine which partnership—food delivery, athleisure apparel, or sports supplements—would best improve customer loyalty and create compelling joint products.

## Technologies Used
- **Python 3.x**: pandas, NumPy, scikit-learn, statsmodels, scipy
- **Statistical Analysis**: Chi-squared testing, OLS regression
- **Data Visualization**: seaborn, matplotlib
- **Development**: Jupyter Notebook

## Technical Implementation

### Data Processing & Analysis
- **Datasets**: 4 Excel files with 3,494 total records
  - FlexField Fitness: 897 gym members
  - CoreBoost: 886 sports drink consumers
  - PulseGear: 888 apparel customers
  - Chef's Meal: 823 meal delivery users
- Cleaned data using **pandas**, handled missing values with **SimpleImputer**, removed duplicates
- Applied one-hot encoding for categorical variables (Gender, Fitness Goal, Dietary Preferences)

### Statistical Testing
**Chi-Squared Analysis** to test association between fitness goals and partner products:
- **CoreBoost**: χ² = 224.73, **p-value = 2.47e-41** ✓ (highly significant)
- Chef's Meal: χ² = 2999.53, p-value = 0.319 (not significant)
- PulseGear: χ² = 3382.01, p-value = 0.468 (not significant)

### Regression Modeling
Built **OLS regression models** using **statsmodels** for each partner:

**CoreBoost Model** (R² = 0.162):
- Hours at Gym significantly predicts consumption (coef = 0.796, p < 0.001)

**Chef's Meal Model** (R² = 0.777):
- Calorie Intake (coef = 0.021, p < 0.001) and Whole foods preference (coef = 10.28, p < 0.001) are key predictors

**PulseGear Model** (R² = 0.287):
- Gender is strongest predictor of apparel spending (coef = 211.94, p < 0.001)

### Customer Segmentation
Analyzed spending patterns by fitness goal:
- Build muscle: 356 customers (40% of total)
- Fat loss: 183 customers
- Performance apparel: $218,919 total spend (highest category)

### Visualizations
Created data visualizations using **seaborn** and **matplotlib**:
- Consumption patterns by fitness goal and product type
- Linear regression plots of gym hours vs. product consumption
- Grouped bar charts comparing demographics across segments

## Decision Framework

### Multi-Criteria Decision Matrix
Evaluated partnerships on 4 weighted criteria:
- Strategic Alignment (30%)
- Customer Engagement Potential (30%)
- Revenue Growth & Profitability (20%)
- Feasibility & Implementation (20%)

**Results:**
- **CoreBoost: 8.2/10** ✓ (Recommended)
- PulseGear: 6.6/10
- Chef's Meal: 6.0/10

## Key Recommendation: CoreBoost Partnership

**Why CoreBoost:**
1. Strongest statistical association with fitness goals (p-value near zero)
2. Direct link to workout performance and recovery
3. Year-round revenue stream (mitigates seasonal attendance drops)
4. High personalization potential for different fitness goals

## Key Insights
- CoreBoost scored **37% higher** than alternatives on strategic metrics
- Identified **30.35% average membership dropout rate** requiring intervention
- Each additional gym hour correlates with **0.796 bottle increase** in sports drink consumption
- Performance apparel market represents **$218,919** secondary opportunity

## Business Impact
Delivered actionable recommendation with statistical validation (p < 0.001) that addresses customer retention through performance-enhancing products aligned with fitness goals. Partnership strategy positions FlexField to compete against digital fitness platforms by creating integrated gym + nutrition experience.

---

