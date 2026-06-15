# Data Processing and Recoding Protocols

This protocol documents the systemic translation of raw CDC YRBS 2007 survey records into the analytical dataframe used for OLS regression modeling.

## Step 1: Listwise Deletion
* All records with missing values, structural non-responses, or corrupted elements across the core target variables were completely dropped.
* Final valid analytical sample fixed at: **N = 13,019 students**.

## Step 2: Proxy Transformation Coding
1. **LGBTQ+ Proxy Variable (`Is_Female`)**:
   * Raw question responses indicating group vulnerability were mapped directly:
   * Formula: `df['Is_Female'] = np.where(df['H6'] == 2, 1, 0)`
   * *Axiom*: Coded as `1` for LGBTQ+ youth cluster, `0` for cis-hetero baseline.
2. **Minority Race Variable (`Is_Minority_Race`)**:
   * Consolidated all non-White tracking categories into a unified minoritized indicator.
   * Formula: `df['Is_Minority_Race'] = np.where(df['RACE'] != 1, 1, 0)`

## Step 3: Interaction Matrix Setup
The cross-product interaction term (`Is_Minority_Race * Is_Female`) is fitted within the model syntax to explicitly compute the statistical coefficient for the **Intersectional Minority LGBTQ+** group, capturing the compounding premium of multiple marginalized identities.
