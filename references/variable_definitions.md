# Data Dictionary and Variable Definitions

This document clear defines the behavioral metrics extracted from the CDC Youth Risk Behavior Survey (YRBS) 2007 dataset used in this intersectional research project.

## 1. Demographics (Independent Predictors)

### Is_Female
* **Description:** Binary indicator representing the biological sex of the student respondent.
* **Source Variable:** YRBS 2007 original sex designation.
* **Value Mapping:** 
  * `0`: Male (Reference Base)
  * `1`: Female

### Is_Minority_Race
* **Description:** Binary indicator capturing racial and ethnic intersectionality by clustering minority racial groups against the majority white baseline.
* **Source Variable:** YRBS 2007 original race/ethnicity tracking code.
* **Value Mapping:** 
  * `0`: White / Non-Hispanic (Reference Base)
  * `1`: Minority Race (including Black, Hispanic, Asian, Native American, and Mixed Race)

## 2. Risk Indicators (Dependent Variables)

### School_Safety_Index
* **Description:** Continuous severity frequency score capturing subjective psychological anxiety and formal school avoidance due to perceived structural danger on campus.
* **Measurement Window:** Past 30 days prior to survey administration.
* **Value Range:** `0` (Lowest Risk / Continuous Attendance) to `4` (Highest Risk / Chronic Absenteeism due to Fear)

### Weapon_Threat_Index
* **Description:** Continuous frequency score tracking objective exposure to severe campus violence, specifically measuring times threatened or injured with weapons on school property.
* **Measurement Window:** Past 12 months prior to survey administration.
* **Value Range:** `0` (Zero Incidents) to `4` (Frequent Physical Victimization / Multiple Attacks)
