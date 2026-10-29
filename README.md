# Maven Manufacturing Analysis

A Power BI portfolio project by **Caio Bergamo**, using the Maven Analytics Manufacturing Downtime dataset.

## Business objective

Identify where production time is being lost, compare downtime across products and operators, and recommend three priorities for further investigation.

## Main findings

The dataset covers **38 production batches from August 29 to September 3, 2024**.

| Metric | Result |
| --- | ---: |
| Recorded downtime | 1,388 minutes |
| Downtime as a share of elapsed batch time | 35.98% |
| Average downtime per batch | 36.53 minutes |
| Downtime classified as operator error | 55.91% |
| Share of downtime from the three leading causes | 58.43% |

Machine adjustment (332 minutes), machine failure (254 minutes), and inventory shortage (225 minutes) were the largest recorded causes. My recommendation is to investigate operator-error-classified losses, machine failure and inventory shortage, and the high downtime percentages for OR-600 and RB-600.

These categories describe recorded stoppages. They do not establish root causes or individual responsibility. OR-600 had only one batch, and differences in product mix affect comparisons across operators.

## Explore the project

- **[Read the analysis report](REPORT.md)** — findings, investigation priorities, and limitations.
- **[Download the Power BI report](powerbi/Maven_Manufacturing_Analysis.pbix)** — interactive analysis in Power BI Desktop.
- **[Download the original Word report](reports/Maven_Manufacturing_Report.docx)**.
- **[Source workbook](data/Manufacturing_Line_Productivity.xlsx)** and **[data dictionary](data/data_dictionary.csv)**.

## Tools and approach

- **Power Query:** prepare and reshape the batch-level production and downtime data.
- **Power BI and DAX:** calculate downtime minutes, shares, and percentages; compare causes, products, and operators.
- **Analysis:** distinguish each category's contribution to total downtime from downtime as a percentage of its own elapsed batch time.

Downtime percentage uses recorded downtime divided by elapsed batch time. It is not an OEE measure. Average downtime per batch includes all batches in the selection, including batches with zero downtime.

## Open the Power BI file

1. Download the repository files and open `powerbi/Maven_Manufacturing_Analysis.pbix` in Power BI Desktop on Windows.
2. Explore the saved report using its slicers.
3. To refresh the data, update the workbook source path in Power Query or Data source settings to point to your local `data/Manufacturing_Line_Productivity.xlsx`, then refresh.

## Data source and attribution

Source: **Maven Analytics Manufacturing Downtime / Manufacturing Line Productivity dataset**, supplied in `Manufacturing_Line_Productivity.xlsx`. The original workbook and dictionary are included unchanged. Analysis and report by Caio Bergamo. This is an independent portfolio project and is not affiliated with Maven Analytics.

No additional license is applied to the source dataset by this repository.
