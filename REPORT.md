# Maven Manufacturing Analysis

*Prepared by Caio Bergamo*

[Back to project overview](README.md) · [Data source and methodology](DATA_SOURCE.md)

## Executive summary

During the analyzed period, from August 29, 2024, to September 3, 2024, there were 38 batches and 1,388 minutes of downtime, accounting for 35.98% of total elapsed batch time. Machine adjustment, machine failure, and inventory shortage were the three leading causes, together accounting for 58.43% of total downtime. Downtime classified as operator error represented 55.91% of recorded losses, making it an important area for further investigation.

My suggestion is to investigate the reasons behind operator-error-classified downtime, while also examining machine failure and inventory shortage, which together accounted for 34.51% of total downtime. OR-600 and RB-600 also deserve attention, as they recorded the highest percentages of their own elapsed batch time lost to downtime. However, OR-600 had only one batch, and the short observation period limits the conclusions that can be drawn. These findings provide a starting point for investigation, but additional data is needed to understand the root causes and determine the appropriate actions.

## Business objective

Identify where production time is being lost, compare downtime across products and operators, and recommend three priorities for further investigation.

## Key findings

### Overall downtime and leading causes

During the analyzed period, from August 29, 2024, to September 3, 2024, there were 38 batches. Total downtime was 1,388 minutes, accounting for 35.98% of total elapsed batch time. The top three leading causes of downtime were machine adjustment (332 min), machine failure (254 min), and inventory shortage (225 min). Together, these factors accounted for 58.43% of total downtime. The average downtime per batch was 36.53 minutes, while downtime classified as operator error accounted for 55.91% of total downtime.

The leading causes classified as non-operator errors were machine failure (254 min), inventory shortage (225 min), and other (74 min). These three factors accounted for 39.84% of total downtime across all causes. The top three causes classified as operator error were machine adjustment (332 min), batch change (160 min), and batch coding error (145 min). These three factors accounted for 45.89% of total downtime across all causes.

### Differences across products

The three products with the highest accumulated downtime were CO-600 (494 min), CO-2L (277 min), and RB-600 (258 min), accounting for 35.59%, 19.96%, and 18.59% of total downtime, respectively.

The three products with the highest percentage of their own elapsed batch time lost to downtime were OR-600 (55.56%), RB-600 (38.05%), and CO-2L (36.11%). It is important to note that OR-600 had only one batch produced. During that batch, more than half of the total elapsed time was recorded as downtime, so additional observations would be needed to assess its typical performance.

The products with the highest proportions of downtime classified as operator error were LE-600 at 85.21% across 6 batches, OR-600 at 80.00% in 1 batch, and RB-600 at 74.81% across 7 batches. Across these three products combined, 79.08% of their recorded downtime was classified as operator error.

### Differences across operators

Mac recorded the highest average downtime per batch at 41.50 minutes across 8 batches, while Dee recorded the lowest at 33.64 minutes across 11 batches. Charlie had the highest proportion of downtime classified as operator error at 59.38% across 11 batches. Dee had the lowest proportion at 51.89%, also across 11 batches. Even the lowest proportion exceeded 50% of the operator’s recorded downtime.

It is important to note that Charlie, Dee, and Dennis each recorded over 150 minutes of downtime while producing CO-600, whereas Mac did not produce any CO-600 batches. This difference in product mix should be considered when comparing overall operator averages. Of the downtime recorded during CO-600 production, 42.11% was classified as operator error, with machine adjustment and product spill tied at 57 minutes each.

## Recommended investigation priorities

### Priority 1

Further investigate downtime classified as operator error and develop a plan to reduce it.

Downtime classified as operator error accounted for 55.91% of total downtime. Addressing the underlying causes may offer a substantial opportunity for downtime reduction. Machine adjustment accounted for 332 minutes, followed by batch change and batch coding error at 160 and 145 minutes, respectively.

My suggestion is to investigate the circumstances leading to these events. Possible explanations include insufficient training on operating the machinery, unclear production schedules, or unclear instructions for specific products. These are hypotheses to investigate rather than explanations established by the dataset.

### Priority 2

Investigate machine failure and inventory shortage, the second- and third-largest downtime causes by minutes.

Machine failure and inventory shortage are both classified as non-operator-error causes. Together, they accounted for 479 minutes, or 34.51% of total downtime.

Further investigation should determine whether inventory shortages resulted from an unusual, temporary increase in demand, a supplier issue, or another explanation. For machine failure, the investigation should examine whether machinery is being operated according to instructions, whether additional preventive maintenance is needed, and whether equipment age or condition warrants an assessment of replacement options. The dataset does not establish which of these explanations applies.

### Priority 3

Further investigate the two products with the highest percentages of total elapsed batch time lost to downtime: OR-600 and RB-600.

OR-600 had only one batch during the period, but downtime accounted for 55.56% of its elapsed batch time, the highest percentage among products. In that batch, 80.00% of recorded downtime was classified as operator error, specifically batch change. RB-600 lost 38.05% of its elapsed batch time to downtime across seven batches, with 74.81% of its recorded downtime classified as operator error.

Although OR-600 had only one observed batch, its high downtime percentage warrants checking whether this was a one-time occurrence or whether the product requires additional attention. For RB-600, the seven observed batches provide a broader basis for investigation, although the sample remains small. Understanding the causes may identify opportunities to improve production efficiency.

This product-level investigation complements Priority 1 by focusing on where operator-error-classified downtime represents a particularly high proportion of recorded losses.

## Limitations and interpretation

The short observation period limits how confidently the findings can be generalized. Only CO-600 had more than ten batches during the period, and OR-600 had only one. The findings provide a basis for targeted investigation, but additional observations are needed to determine whether the patterns persist.

Differences in product mix and batch counts also affect comparisons across operators. Overall downtime averages alone do not establish individual operator performance.

The downtime categories identify recorded reasons for stoppages but do not establish their underlying root causes or individual responsibility. More detailed event records, including maintenance history, material availability, operating conditions, and training records, would help determine the appropriate corrective actions.

## Data source and measurement notes

Source: Maven Analytics Manufacturing Downtime dataset, supplied as Manufacturing_Line_Productivity.xlsx and analyzed in Power BI.

| Metric | Definition |
| --- | --- |
| Downtime share by product | Product downtime divided by downtime across all products within the retained nonproduct filters. |
| Downtime percentage of elapsed time | Recorded downtime divided by elapsed batch time for the current selection. |
| Average downtime per batch | Recorded downtime divided by all production batches in the selection, including zero downtime batches. |
