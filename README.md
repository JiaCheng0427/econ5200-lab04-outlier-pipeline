# Outlier Detection on California Housing

## Objective
The goal of this lab was to compare different outlier detection methods on the California Housing dataset and understand how each method flags unusual observations.

## Methodology
- Fixed three bugs in the original outlier detection pipeline.
- Used an `OutlierDetector` class to run Modified Z-score, Tukey Fence, and Isolation Forest.
- Applied Modified Z-score and Tukey Fence to the `MedInc` column.
- Applied Isolation Forest to all 9 numeric columns.
- Compared the number of observations flagged by each method.
- Built an interactive explorer to change the column and method settings.
- Recommended using Tukey Fence first, with Isolation Forest as a second check.

## Key Findings
- Modified Z-score flagged **400** observations on `MedInc`.
- Tukey Fence flagged **681** observations on `MedInc`.
- Isolation Forest flagged **1032** observations using all 9 numeric columns.
- All three methods agreed on **322** observations.
- The methods do not always flag the same rows because they use different ways to define an outlier.
- I would not automatically remove every flagged observation because some extreme values may be real cases rather than data errors.
