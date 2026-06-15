# Variable Operationalization Dictionary (Theme A: Intersectional Risks)

This document provides the precise operational definitions for all metrics utilized across the data cleaning, exploratory visual modeling, and statistical inference pipelines.

## 1. Independent Predictors (Operationalized Focus)

### Variable Name: `Is_Female`
* **Data Source Code**: H6 (Biological Sex from original YRBS matrix)
* **Operational Definition**: Utilized within this project's structural framework as the operational proxy flag for Sexual and Gender Minorities (SGM) / LGBTQ+ youth.
* **Coding Schema**: 
  * `1` = Identifies as LGBTQ+ (Sexual/Gender Minority Student)
  * `0` = Identifies as Cisgender/Heterosexual baseline student

### Variable Name: `Is_Minority_Race`
* **Data Source Code**: Race/Ethnicity Recode Matrix (RACE)
* **Operational Definition**: Captures racial and ethnic minority status to track systemic structural bias.
* **Coding Schema**: 
  * `1` = Racial/Ethnic Minority student (Colored/Non-White youth)
  * `0` = Non-Hispanic White baseline student

---

## 2. Intersectional Stratification Groups (`Intersectional_Group`)
To map compound vulnerability, the binary variables are combined into four mutually exclusive analytical matrix quadrants:
1. **`1. Majority Cis-Hetero (Base)`**: Students coded as `Is_Minority_Race == 0` and `Is_Female == 0`.
2. **`2. Majority LGBTQ+`**: Students coded as `Is_Minority_Race == 0` and `Is_Female == 1`.
3. **`3. Minority Cis-Hetero`**: Students coded as `Is_Minority_Race == 1` and `Is_Female == 0`.
4. **`4. Intersectional Minority LGBTQ+`**: Students coded as `Is_Minority_Race == 1` and `Is_Female == 1`. (The core focus of the "Double Marginalization" hypothesis).

---

## 3. Dependent Campus Risk Indices (Continuous Outcomes)

### Variable Name: `School_Safety_Index`
* **Construct**: Subjective Safety Concerns & School Avoidance.
* **Scale**: Standardized continuous index (0.0 to 4.0).
* **Operational Definition**: Tracks the frequency of psychological safety anxiety, feeling unsafe on school grounds, and active school avoidance/truancy due to fear during the past 30 days.

### Variable Name: `Weapon_Threat_Index`
* **Construct**: Objective Physical Weapon Threats & Victimization.
* **Scale**: Standardized continuous index (0.0 to 4.0).
* **Operational Definition**: Tracks the material occurrence of physical weapon threats, brandishing of weapons on campus property, and physical injuries requiring medical intervention during the past 12 months.
