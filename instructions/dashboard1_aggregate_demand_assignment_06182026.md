# Building an Aggregate Demand and GDP Dashboard

Introduction to Macroeconomics

Product Type: Applied macroeconomic dashboard with an interpretation memo Recommended Output: Excel workbook and short dashboard commentary

# 1. Rationale

This assignment trains students to transform macroeconomic data into a practical dashboard. Using quarterly GDP data from the expenditure side, students will compute growth rates, expenditure shares, contributions to GDP growth, and co-movements between aggregate demand components and GDP. The dashboard should help students understand which components drive economic activity, which are expanding or contracting, and how their movements relate to the broader business cycle.

The assignment emphasizes applied macroeconomic interpretation rather than technical econometric modeling. Students are expected to produce a clean, transparent, and decisionoriented dashboard that is easy for non-specialist users to understand.

# 2. Learning Outcomes

After completing the assignment, students should be able to:

- 1. organize quarterly aggregate demand data for dashboard construction;
- 2. compute year-on-year growth rates for GDP and its expenditure components;
- 3. compute expenditure-component shares in GDP;
- 4. compute expenditure-component contributions to GDP growth;
- 5. construct and interpret simple welfare indicators based on real GDP per capita and real consumption per capita;
- 6. identify demand components that are procyclical, relatively stable, volatile, or vulnerable to shocks;
- 7. prepare visual summaries using charts, tables, and conditional formatting; and
- 8. translate dashboard results into practical insights that a hypothetical policymaker can appreciate.

# 3. Dataset

Each group will use a quarterly dataset containing GDP and its expenditure components for an assigned country. The dataset should include, as available, household final consumption expenditure, government final consumption expenditure, gross capital formation or investment, exports, imports, and GDP. Population data should also be collected if the group will compute GDP per capita and consumption per capita.

Once a country has been selected by one group, it may no longer be selected by another group. Students should verify that the selected country has a sufficiently long and internally consistent quarterly time series. The frequency, price basis, seasonal-adjustment status, units, and source of every series must be documented.

# 4. Aggregate Demand Framework

The dashboard should be organized around the expenditure identity

$$GDP_t = C_t + I_t + G_t + X_t - M_t,$$

where C<sup>t</sup> denotes household consumption, I<sup>t</sup> denotes investment or gross capital formation, G<sup>t</sup> denotes government consumption, X<sup>t</sup> denotes exports, and M<sup>t</sup> denotes imports. If the source dataset uses more detailed categories, students may retain those categories as long as the relationship to the aggregate identity is clearly documented.

# 5. Required Dashboard Components

The final dashboard should contain the following components.

#### 5.1. Headline Indicator Cards

At the top of the dashboard, include at least eight summary cards:

- a. latest real GDP level;
- b. latest real GDP year-on-year growth rate;
- c. fastest-growing aggregate demand component in the latest quarter;
- d. slowest-growing aggregate demand component in the latest quarter;
- e. largest positive expenditure component as a share of GDP in the latest quarter;
- f. most volatile aggregate demand component, based on the standard deviation of yearon-year growth;
- g. initial-period and latest real GDP per capita; and
- h. initial-period and latest real consumption per capita.

Additional cards may be included when they improve interpretation. All cards must identify the reference quarter and the units used.

### 5.2. GDP Trend Chart

Create a line chart showing real GDP over time. This chart should help users see the economy's long-run expansion and identify major periods of slowdown or disruption.

#### 5.3. GDP Growth Chart

Create a line chart or column chart showing year-on-year real GDP growth. This chart should highlight business-cycle turning points more clearly than the GDP level chart.

#### 5.4. Aggregate Demand Growth Chart

Create a line chart or grouped column chart comparing the year-on-year growth rates of the major aggregate demand components. The chart should reveal whether changes in consumption, investment, government spending, exports, or imports are associated with expansions and downturns.

#### 5.5. Expenditure Share Chart

Create a horizontal bar chart showing the latest expenditure-component shares in GDP. Imports may be displayed as a positive ratio for descriptive purposes, but the chart must clearly indicate that imports enter the GDP identity with a negative sign.

#### 5.6. Contribution to GDP Growth Chart

Create a stacked column chart showing the percentage-point contributions of aggregate demand components to year-on-year GDP growth. Import contributions must be entered with the correct negative sign. If a residual or statistical discrepancy prevents the contributions from summing exactly to measured GDP growth, report and explain the difference.

#### 5.7. Component–GDP Correlation Chart

Create a bar chart showing the correlation between each aggregate demand component's year-on-year growth and real GDP year-on-year growth. This chart provides a descriptive measure of co-movement; it does not establish causality.

#### 5.8. Welfare Indicator Chart

Create a line chart showing real GDP per capita and real consumption per capita, preferably as indices with the initial period set equal to 100 when their units differ. Use these indicators cautiously: they provide information about average material living standards but do not measure inequality, unpaid work, leisure, health, environmental quality, or the distribution of income and consumption.

# 6. Required Computations

#### 6.1. Year-on-Year Growth

For each aggregate demand component and for real GDP, compute year-on-year growth as

YoY Growth<sub>i,t</sub> = 
$$\left(\frac{X_{i,t}}{X_{i,t-4}} - 1\right) \times 100$$
,

where Xi,t is the value of component i in quarter t. Because the data are quarterly, the four-quarter lag compares the current quarter with the same quarter in the previous year. The formula should normally be applied to real measures when the objective is to analyze changes in economic activity.

#### 6.2. Expenditure Component Share in GDP

For each component, compute its descriptive share in GDP as

$$Share_{i,t} = \frac{X_{i,t}}{GDP_t} \times 100.$$

This ratio shows the size of a component relative to GDP. Students must use series measured on the same price basis and in the same units. The shares need not sum to 100 when imports are displayed as a positive ratio or when the source includes inventories, valuables, or a statistical discrepancy.

### 6.3. Contribution to GDP Growth

For consumption, investment, government consumption, and exports, compute the approximate percentage-point contribution to year-on-year GDP growth as

Contribution<sub>i,t</sub> = 
$$\frac{X_{i,t} - X_{i,t-4}}{GDP_{t-4}} \times 100$$
.

For imports, use

Import Contribution<sub>t</sub> = 
$$-\frac{M_t - M_{t-4}}{GDP_{t-4}} \times 100$$
.

Thus, an increase in imports, holding the other components unchanged, makes a negative arithmetic contribution to GDP growth. Students must verify whether the source data are additive. Chained-volume measures are often not exactly additive; when this occurs, the contribution calculation should be described as an approximation unless the statistical agency provides official contribution series or an appropriate chain-linking method.

#### 6.4. Component–GDP Correlation

For each aggregate demand component, compute the correlation between its year-on-year growth and real GDP year-on-year growth:

$$\rho_i = \operatorname{Corr}(g_{i,t}, g_{GDP,t}),$$

where gi,t is the component growth rate and gGDP,t is the real GDP growth rate. Use a common sample period for all correlations and exclude missing observations consistently.

### 6.5. Welfare Indicators

Compute real GDP per capita and real consumption per capita as

Real GDP per capita<sub>t</sub> = 
$$\frac{\text{Real GDP}_t}{\text{Population}_t}$$
,

and

$$\text{Real consumption per capita}_t = \frac{\text{Real household consumption}_t}{\text{Population}_t}.$$

When population is available only annually, document the interpolation or allocation method used to obtain quarterly values. Interpret these measures as limited indicators of average material welfare rather than complete measures of social welfare.

# 7. Step-by-Step Instructions

### 7.1. Step 1: Prepare the Workbook

Create the following sheets in Excel:

|                    | Table 1: Recommended Workbook Structure                        |
|--------------------|----------------------------------------------------------------|
| Sheet Name         | Content                                                        |
| Raw Data           | Original data exactly as downloaded                            |
| Clean Data         | Checked, consistently labeled, and documented data             |
| Growth Rates       | Year-on-year growth rates                                      |
| Expenditure Shares | Aggregate demand component shares in GDP                       |
| Contributions      | Component contributions to GDP growth                          |
| Correlations       | Component–GDP growth correlations                              |
| Welfare Indicators | Real GDP per capita and real consumption per capita            |
| Dashboard          | Final visual dashboard                                         |
| Notes              | Interpretation, formulas, sources, units, and data limitations |

#### 7.2. Step 2: Clean and Label the Data

Check that all quarters are correctly ordered from the initial to the latest period. Rename series codes using the source's variable dictionary. Make sure all values are numeric and that there are no blank rows inside the data range. Verify that GDP and its components have the same frequency, units, price basis, and seasonal-adjustment status. Do not combine nominal and real series in the same computation.

### 7.3. Step 3: Compute Growth Rates

In the Growth Rates sheet, compute year-on-year growth beginning with the fifth observation. For example, if real GDP is in column R and begins in row 2, the first year-on-year growth formula is

=(R6/R2-1)\*100

Copy the formula across all aggregate demand component columns and down all quarters. Check for zero, negative, missing, or structurally incomparable observations before applying the formula.

#### 7.4. Step 4: Compute Expenditure Shares

In the Expenditure Shares sheet, divide each component by GDP. For example, if investment is in column D and GDP is in column R, use

=D2/\$R2\*100

Copy the formula across all relevant columns and down all quarters. Clearly distinguish between the positive import-to-GDP ratio used for description and the negative sign assigned to imports in the GDP identity.

### 7.5. Step 5: Compute Contributions to GDP Growth

In the Contributions sheet, compute each component's approximate percentage-point contribution to GDP growth. For example, if investment is in column D and GDP is in column R, use

=(D6-D2)/\$R2\*100

For imports in column E, use

=-(E6-E2)/\$R2\*100

Copy the formulas across all components and down all quarters. Add the component contributions and compare the sum with measured year-on-year GDP growth. Document any discrepancy arising from chain linking, inventories, valuables, statistical discrepancies, rounding, or incomplete component coverage.

#### 7.6. Step 6: Compute Component–GDP Correlations

In the Correlations sheet, compute the correlation between each component's year-on-year growth and real GDP year-on-year growth. In Excel, use

=CORREL(Component\_growth\_range, GDP\_growth\_range)

Interpret the results as follows:

- correlation close to 1: the component is strongly procyclical;
- correlation close to 0: the component has weak contemporaneous co-movement with GDP; and
- negative correlation: the component tends to move in the opposite direction from GDP over the sample.

These correlations are descriptive and may depend on the sample period, crisis observations, trends, and data treatment.

#### 7.7. Step 7: Compute Welfare Indicators

In the Welfare Indicators sheet, divide real GDP and real household consumption by population. If desired, convert each per-capita series into an index with the initial period equal to 100. Report the cumulative change between the initial and latest periods and identify major reversals during crisis episodes.

#### 7.8. Step 8: Build the Dashboard

Create a single-page dashboard using clear titles, clean charts, and short notes. Avoid clutter. The dashboard should allow a user to understand the aggregate demand story in less than five minutes.

# 8. Required Written Commentary

Submit a dashboard commentary of 500 to 800 words. The commentary should answer the following questions:

- 1. What is the latest real GDP growth performance?
- 2. Which aggregate demand components are largest relative to GDP?
- 3. Which components are growing fastest and slowest?
- 4. Which components provide the largest positive contributions and the largest negative contributions to GDP growth?
- 5. Which components appear most volatile or most exposed to downturns?
- 6. Which components are most closely associated with GDP movements?
- 7. What do real GDP per capita and real consumption per capita suggest about changes in average material welfare?
- 8. What did the dashboard reveal about major crisis periods, such as 2008–2009 and 2020, when these periods are covered by the data?
- 9. What are the practical implications for managers, investors, workers, and policymakers?

# 9. Macro Bit Requirements

Students should submit the following products:

- 1. an Excel workbook containing all computation sheets and the dashboard;
- 2. a 500- to 800-word dashboard commentary;
- 3. a short documentation note explaining the formulas, sources, units, transformations, and limitations; and
- 4. properly labeled charts and tables.

The workbook must contain formulas rather than pasted values for growth rates, expenditure shares, contributions, correlations, and welfare indicators.

# 10. Suggested Dashboard Design Standards

- Use clear chart titles.
- Label axes, units, frequency, and price basis.
- Use consistent aggregate demand component names.
- Avoid excessive colors.
- Use conditional formatting only where it improves interpretation.
- Highlight the most important components when displaying every available series would make a chart difficult to read.
- Include a short interpretation box on the dashboard.
- Identify the data source and latest observation date on the dashboard.

# <span id="page-8-0"></span>11. Proposed Rubric

Table 2: Assessment Rubric

| Criterion                                      | Description                                                                                                                                                                                    | Weight |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| Data<br>organization<br>and<br>cleaning        | Data are correctly arranged, labeled, documented, and<br>prepared for analysis. The workbook structure is clear<br>and reproducible.                                                           | 20%    |
| Correctness<br>of<br>compu<br>tations          | Growth rates, expenditure shares, contributions,<br>correlations, and welfare indicators are computed<br>correctly using transparent formulas.                                                 | 30%    |
| Dashboard design                               | The dashboard is clean, readable, decision-oriented, and<br>based on appropriate charts that are not overloaded.                                                                               | 20%    |
| Interpretation<br>and<br>macroeconomic insight | The commentary correctly explains aggregate demand<br>patterns, GDP movements, business-cycle behavior,<br>welfare indicators, and shock episodes without making<br>unsupported causal claims. | 25%    |
| Presentation quality                           | Tables, charts, labels, documentation, and written<br>commentary are polished and professional.                                                                                                | 5%     |

# 12. Submission Deadline

The deadline is June 25, 2026.