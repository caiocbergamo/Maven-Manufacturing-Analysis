# Data Source and Methodology

## Source and attribution

[Maven Analytics Manufacturing Downtime](https://mavenanalytics.io/data-playground/manufacturing-downtime) contains productivity and downtime data for a soda bottling line. The publisher's source page identifies the dataset as **Public Domain**. This project uses the supplied workbook and dictionary, reproduced unchanged.

Analysis and report: Caio Bergamo. This independent portfolio project is not affiliated with Maven Analytics.

## Files and scope

- [Manufacturing_Line_Productivity.xlsx](data/Manufacturing_Line_Productivity.xlsx): Line productivity (38 batches), Products (6 products), Downtime factors (12 factors), and Line downtime (38 batches).
- [data_dictionary.csv](data/data_dictionary.csv): original source field definitions.
- Observation dates: August 29–September 3, 2024.

## Preparation

Production batches were retained as the denominator for batch counts and averages, including the three batches with zero recorded downtime. Downtime factor columns were reshaped for analysis and linked to the factor descriptions and classifications. Product, operator, and date filters support comparisons in Power BI.

## Metric definitions

| Metric | Definition |
| --- | --- |
| Recorded downtime | Sum of recorded downtime minutes across factors |
| Elapsed batch time | End time minus start time, expressed in minutes |
| Downtime percentage of elapsed time | Recorded downtime ÷ elapsed batch time in the selection |
| Average downtime per batch | Recorded downtime ÷ all batches in the selection |
| Product downtime share | Product downtime ÷ downtime across products, retaining nonproduct filters |
| Operator-error-classified downtime share | Minutes assigned to factors marked Yes in the source ÷ recorded downtime |

## Validation and limitations

The source workbook reconciles to 38 batches, 3,858 elapsed minutes, 1,388 downtime minutes, and 776 minutes classified as operator error. The reported percentages use these matching denominators. Factor, product, and operator comparisons were checked against the workbook.

The observation period is short. Product mix and small batch counts affect operator/product comparisons. Recorded categories do not establish root causes or individual responsibility. Native Power BI rendering and interactive refresh were not rerun during the repository review.

[Back to project overview](README.md) · [Read the analysis report](REPORT.md)
