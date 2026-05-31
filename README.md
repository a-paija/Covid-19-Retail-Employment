## Project Background

Analyzed U.S. labor market dynamics during COVID-19 using IPUMS CPS microdata (2019–April 2022) to quantify the pandemic’s impact on retail employment, unemployment, and earnings.

This project applies time-series analysis, fixed-effects regression, and difference-in-differences (DiD) modeling in R to identify structural breaks, measure employment shocks, and compare industry-level impacts.

This project uses **IPUMS Current Population Survey (CPS) microdata** to examine labor market changes from the pre-pandemic period through April 2022. The goal is to analyze how employment dynamics evolved across retail and non-retail industries and how income patterns shifted for workers during the pandemic.

The analysis is guided by three core questions:

- How has COVID-19 affected retail employment levels?
- How has retail performed relative to other industries?
- How did COVID-19 change who is working and how much they earn?

#### **Overall Goal:**
Quantify the labor market impact of COVID-19 across employment levels, industry composition, and earnings to understand structural changes in workforce dynamics.


## Key Results

- Retail employment declined by approximately 1.03 million jobs following COVID-19 onset
- Retail unemployment increased by approximately 1.27 million workers, with a sharp spike in April 2020
- Probability of employment in retail decreased by 2.9 percentage points (statistically significant at 0.1% level)
- Non-retail industries experienced larger absolute job losses (~11 million), but retail saw sharper relative declines
- Significant shifts in weekly earnings and income volatility observed across industries

Retail and industry groups were constructed using CPS industry codes, and time variables were standardized to monthly frequency for consistent trend analysis.

## Methodology

- Processed CPS microdata using R (tidyverse, fixest, ggplot2)
- Conducted time-series analysis to detect structural breaks in employment trends
- Built fixed-effects regression models to estimate COVID impact on employment and unemployment
- Applied difference-in-differences (DiD) to compare retail vs non-retail industry outcomes
- Controlled for demographic and geographic factors (age, race, citizenship, state, time)

## Executive Summary

<img src="images/retail3.png" width="700" height="550"/>

The COVID-19 pandemic created a **sharp and structurally significant shock** to the U.S. labor market, with retail and service industries experiencing immediate disruptions in employment and earnings.

Key findings:

- Retail employment dropped sharply at the onset of COVID-19 and recovered gradually but unevenly
- Unemployment in retail spiked immediately after April 2020, reaching ~3 million
- Non-retail industries experienced even larger absolute employment declines
- Retail workers experienced a **larger drop in employment rates relative to non-retail**
- Weekly earnings shifted significantly across industries, with heterogeneous recovery patterns

#### **Core Insight:**
COVID-19 did not simply reduce employment—it reshaped **labor allocation, industry composition, and earnings distribution across the workforce**.

## Key Insight

COVID-19 created a structural shift in labor markets—altering not only employment levels, but also workforce composition and income distribution. Retail experienced disproportionate relative disruption, while service sectors absorbed the largest absolute losses.

## Retail Employment Impact (Time-Series Analysis)

Retail employment trends show a clear structural break beginning in April 2020.

- Sharp decline in total employment at pandemic onset
- Gradual recovery following initial shock
- Employment remains below pre-pandemic baseline in later periods

Retail unemployment shows the inverse pattern:

- Sudden spike in unemployment (~3M workers affected)
- Gradual decline as the economy reopens
- Persistent elevated unemployment relative to pre-COVID levels

#### **Insight:**
Retail employment is highly sensitive to external shocks, particularly those affecting consumer demand and physical store operations.



## Pre vs Post COVID Employment Shifts

A comparison of pre- and post-COVID trends reveals:

- Pre-COVID: relatively stable retail employment trajectory
- Post-COVID: sustained downward shift followed by partial recovery
- Structural break in both level and slope of employment trends

#### **Insight:**
COVID-19 caused a permanent shift in the retail labor trajectory rather than a temporary disruption.

## Econometric Analysis: Employment Impact

A fixed-effects regression model estimates the impact of COVID-19:

### Key Results
- Retail employment decreased by ~**1.03 million jobs post-COVID**
- Retail unemployment increased by ~**1.27 million workers**
- Employment shows weak recovery trend over time
- Unemployment declines gradually after initial spike

#### **Insight:**
COVID-19 caused a statistically significant and immediate shock to retail labor markets, followed by partial recovery.



## Individual-Level Employment Analysis

After controlling for demographics and seasonality:

- Probability of employment in retail declined by **~2.9 percentage points**
- Effect remains statistically significant at the 0.1% level
- Controls include age, race, citizenship, month, and state fixed effects

#### **Insight:**
The employment shock persists even after accounting for demographic and geographic variation, confirming a broad structural effect.



## Retail vs Other Industries

### Key Findings:
- Both retail and non-retail sectors experienced employment declines
- Non-retail experienced larger absolute job losses (~11M)
- Retail experienced sharper relative employment rate declines
- Services sector experienced the most severe contraction overall

#### **Insight:**
COVID-19 impacts were uneven across sectors, with services bearing the largest employment shock, while retail showed sharper proportional declines.



## Difference-in-Differences (Industry Comparison)

A DiD model comparing retail vs non-retail shows:

- Non-retail employment dropped significantly post-COVID
- Retail experienced smaller absolute declines but sharper relative contraction
- Significant interaction effects confirm heterogeneous industry responses

#### **Insight:**
Retail was not the most affected in absolute terms, but its labor force experienced stronger relative disruption.



## Earnings & Income Distribution Changes

Earnings analysis shows:

- Significant changes in weekly earnings post-COVID
- Retail workers experienced different recovery patterns compared to non-retail
- Earnings volatility increased during and after pandemic onset
- Structural shifts suggest changes in workforce composition and hours worked

#### **Insight:**
COVID-19 affected not just employment levels, but also **income stability and wage distribution across sectors**.



## Key Assumptions & Limitations

### Key Assumptions:
- Parallel trends assumption for DiD models
- No major confounding shocks coinciding with COVID onset
- CPS data accurately reflects employment conditions
- Homogeneous wage assumptions in earnings construction

### Limitations:
- Earnings are partially imputed (simplified wage assumptions)
- Aggregation reduces individual-level variation
- Potential autocorrelation in time-series models
- Unobserved heterogeneity across industries and workers

## Conclusion

The COVID-19 pandemic created a **large, immediate, and structurally persistent shock** to the U.S. labor market.

While retail employment showed partial recovery over time, the sector experienced:

- Sharp employment volatility
- Declines in employment rates
- Persistent shifts in labor utilization
- Changes in earnings distribution patterns

However, the **services sector experienced even larger absolute employment losses**, highlighting uneven impacts across industries.


