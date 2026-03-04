# A/B Test Analysis
Analyzed the performance of a new recommendation engine through an A/B test to determine if it significantly improved user conversion across the sales funnel.
---

## ⚙️ Project Type Flags

- [x] Exploratory Data Analysis (EDA)
- [x] SQL Analysis / Querying
- [x] Dashboard / Data Visualization
- [ ] Data Pipeline / ETL
- [ ] Predictive Modelling / Machine Learning
- [ ] Data Cleaning / Wrangling
- [ ] End-to-End (multiple of the above)
- [ ] Other: ___________

---

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Repository Structure](#3-repository-structure)
4. [Analysis & Metrics](#4-analysis--metrics)
5. [Key Insights](#5-key-insights)
6. [Deliverables](#6-deliverables)
7. [Author](#7-author)

---

## 1. Project Overview

An international online store tested a new recommendation system to see if it could increase conversions by 10% at each stage of the funnel within 14 days of signup. The original analysis was never completed, so it was unclear whether the test met its goal. I filtered the data to EU users in the correct time frame, removed overlapping users, and ran a Z-test for proportions. The results showed that the new system performed worse than the control group at each stage and did not meet the expected lift.

---

## 2. Objectives

Primary Objective:
Determine whether the new recommender system (Group B) achieved a statistically significant 10% increase in conversion rates at the product page, cart, and purchase stages within 14 days of user signup.

Secondary Objective 1:
Validate the integrity of the A/B test by identifying and removing overlapping users between groups and confirming that only EU users within the defined test period (December 2020–January 2021) are included.

Secondary Objective 2:
Quantify the conversion rates and drop-off percentages at each stage of the funnel—login → product page → cart → purchase—for both control and treatment groups.

## 3. Repository Structure

```
[project-root]/
│
├── data/
│   └── raw/                  # Original, unmodified source data - never edited
│
├── notebooks/                # Jupyter, R Markdown, or Colab notebooks
│
├── scripts/                  # Reusable .py, .R, or .sh processing files
│
├── reports/                  # Final outputs: PDFs, slide decks, Word docs
│
├── visuals/                  # Exported charts, dashboard screenshots, ERD diagrams
│
└── docs/                     # Data dictionaries, schema notes, reference material

```

## 4. Analysis & Metrics


### Analytical Approach

### Key Metrics Defined

| Metric | Plain-Language Definition | Why It Matters |
|--------|--------------------------|----------------|
| `Conversion Rate (CR)` | The percentage of users who move from one stage of the funnel to the next.] | [Measures the specific impact of the recommender system on shopping behavior. |
| `14-Day Retention Conversion` | Conversion metrics calculated only using events within 14 days of a user's signup.] | [Ensures the "Expected Outcome" defined in the technical specs is measured accurately. |
| `Statistical Significance (p-value)` | The probability that the difference between groups happened by chance.] | [Validates whether the "improvement" (or decline) is real or just noise. |

### Methods Used

Descriptive statistics for event distribution per user.

Funnel analysis (Login -> Product Page -> Cart -> Purchase).

Z-test for independent proportions (Alpha = 0.05).

---

## 5. Key Insights

<!--
  Findings + implications. Not just what happened - what it means.

  WHAT GOOD LOOKS LIKE:
  ✅ "Return rates, not sales volume, explain Region A's underperformance.
      Region A's return rate on home goods was 34% - more than double the
      company average. Revenue was not lost at the point of sale; it was
      lost post-sale through refunds. This points to a fulfilment or
      product quality issue specific to that region, not a demand problem."

  WHAT TO AVOID:
  ❌ "Region A had lower revenue than other regions in Q4."
     (That's an observation. It describes what happened.
      An insight says what it means and where to look next.)

  Aim for 3–6 insights. Quality over quantity.
-->

**Insight 1: Test Integrity Failure**
A significant number of users were found to be participating in two tests simultaneously. Additionally, the test was conducted during the "Christmas Calendar" marketing event, which likely skewed purchase behavior across both groups.

**Insight 2: [Negative Conversion Impact**
Contrary to the 10% increase goal, Group B showed a lower conversion rate than Group A at the very first step (Product Page). Group A converted at ~65% while Group B converted at only ~56%.

**Insight 3: Funnel Bottleneck**
The largest drop-off in both groups occurs between the login and product_page stages. The new system failed to entice users to even look at products at the same rate as the old system.

**Insight 4: Statistical Rejection**
The Z-test resulted in p-values significantly lower than 0.05 for the product_page and purchase stages, confirming that the decrease in performance in Group B was statistically significant.


## 6. Deliverables

| Deliverable | Description | Location |
|-------------|-------------|----------|
| Code | Jupyter Notebook containing EDA, Funnel Visualizations, and Z-test results. | `/path/to/file` |
| Visualizations | images where we can find the results | [`/path/to/file` |

---

## 7. Author

**Cristian Barrientos**
Your role or title - current or target

- 🔗 [LinkedIn URL](https://www.linkedin.com/in/cristian-barrientos-pomposo/)
- 💼 [Portfolio or GitHub profile URL](https://github.com/cris971107)
- 📧 cristian971107@hotmail.com

---

