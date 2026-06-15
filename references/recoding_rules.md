# Data Transformation and Recoding Rules

This document outlines the operational normalization and data cleaning pipeline applied to the raw YRBS 2007 survey dataset to ensure reliable OLS regression inference.

## 1. Filtering Criteria for Valid Sample (Row Reduction)

* **Missing Data Elimination:** Observations containing missing values (`NaN`), non-responses, or systemic data corruptions across the four central pillars (`Is_Female`, `Is_Minority_Race`, `School_Safety_Index`, `Weapon_Threat_Index`) were strictly removed.
* **Final Analytical Sample Size:** N = 13,019 individual student records.

## 2. Variable Recoding Implementations

### Demographics Standardization
* **Gender Normalization:** Extracted original biological codes, re-indexing biological males as `0` to serve as the statistical baseline, and biological females as `1`.
* **Race Consolidation:** To facilitate high-powered statistical testing of intersectional marginalization, minoritized populations (Black, Hispanic, Asian, Multi-racial) were consolidated into a single unified category coded as `1`, evaluated against the non-Hispanic White baseline coded as `0`.

### Behavioral Index Standardization
* **Missing Value Thresholding:** Any raw data point flagging systemic omission was pruned before model calculations to prevent statistical distortion.
* **Frequency Mapping Consistency:** Categorical survey responses (tracking incident frequencies from "0 times", "1 time", to "4 or more times") were transformed into standardized continuous frequency rankings ranging from `0` to `4`. This mapping converts localized ordinal attributes into a continuous analytical scale optimized for robust Ordinary Least Squares (OLS) linear model evaluation.
