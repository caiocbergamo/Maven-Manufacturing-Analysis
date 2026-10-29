# Maven Manufacturing Analysis

An independent portfolio project by **Caio Bergamo**, using Power BI to analyze downtime on a soda bottling production line.

## Business objective

Identify where production time is being lost, compare downtime across products and operators, and recommend three priorities for further investigation.

## Main findings

The analysis covers **38 production batches from August 29 to September 3, 2024**.

| Metric | Result |
| --- | ---: |
| Recorded downtime | 1,388 minutes |
| Downtime as a share of elapsed batch time | 35.98% |
| Average downtime per batch | 36.53 minutes |
| Downtime classified as operator error | 55.91% |
| Share of downtime from the three leading causes | 58.43% |

Machine adjustment (332 minutes), machine failure (254 minutes), and inventory shortage (225 minutes) were the largest recorded causes. My recommendation is to investigate operator-error-classified losses, machine failure and inventory shortage, and the high downtime percentages for OR-600 and RB-600.

## Explore the project

| File | Contents |
| --- | --- |
| [Analysis report](REPORT.md) | Findings, recommendations, methodology, and limitations |
| [Power BI file](powerbi/Maven_Manufacturing_Analysis.pbix) | Interactive Manufacturing Overview page |
| [Word report](reports/Maven_Manufacturing_Report.docx) | Original editable project write-up |
| [Source workbook](data/Manufacturing_Line_Productivity.xlsx) | Original production, product, downtime, and factor tables |
| [Data dictionary](data/data_dictionary.csv) | Source field definitions |
| [Source documentation](DATA_SOURCE.md) | Dataset origin, preparation, and attribution |

## Tools and approach

- **Power Query:** prepare and reshape batch-level production and downtime data.
- **Power BI and DAX:** calculate downtime minutes, shares, and percentages, and compare causes, products, and operators.
- **Validation:** reconcile report figures with the supplied workbook.

## Scope and methodology

The workbook contains 38 batches, including three with zero recorded downtime. Downtime percentage divides recorded downtime by elapsed batch time. Average downtime per batch includes every batch in the selection. Product downtime share divides product downtime by downtime across products within the retained nonproduct filters.

The source's operator-error classification identifies recorded categories. It does not establish individual responsibility or the underlying cause of each event. Downtime percentage of elapsed time is separate from OEE.

## Limitations and interpretation

The short observation period and differences in product mix limit comparisons. OR-600 had only one batch. Operator averages should be interpreted alongside product mix and batch counts. Recommendations are investigation priorities, and possible explanations in the report remain hypotheses.

## Open and refresh

1. Download the repository files using **Code → Download ZIP**, then extract them.
2. Open `powerbi/Maven_Manufacturing_Analysis.pbix` in Power BI Desktop on Windows and explore the saved report using its slicers.
3. To refresh, update the workbook source path in Power Query or Data source settings to your local `data/Manufacturing_Line_Productivity.xlsx`, then refresh.

## Data source and attribution

Source: [Maven Analytics Manufacturing Downtime dataset](https://mavenanalytics.io/data-playground/manufacturing-downtime), supplied as `Manufacturing_Line_Productivity.xlsx`. Maven Analytics identifies the source dataset as **Public Domain**. The workbook and data dictionary are reproduced unchanged. Analysis and report by Caio Bergamo. See [source details](DATA_SOURCE.md).

## Other portfolio projects

- [Olist Delivery Analysis](https://github.com/caiocbergamo/Olist_Delivery_Analysis)
- [Brick Manufacturing Analysis](https://github.com/caiocbergamo/Brick-Manufacturing-Analysis)
