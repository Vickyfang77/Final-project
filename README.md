## Student Information
Name: 彭鈺芳 (Vickyfang77)
Student ID: 113370218

## Project Repository
https://github.com/[[請在此處填寫你的GitHub倉庫連結]](https://github.com/Vickyfang77/Final-project)

## Presentation Video
https://youtube.com/[請在此處填寫你的YouTube影片連結]

# Intersectional Analysis of School Violence: How Race and Gender Compound Campus Risks (種族與性別對校園暴力與武器威脅的交織性效應分析)

This research project evaluates the multi-layered nature of high school campus violence in the United States using an intersectional framework. Utilizing a national sample from the CDC Youth Risk Behavior Survey (YRBS) 2007, this study transitions past single-variable analysis to explore how biological sex and minority race interact to influence subjective school safety and objective weapon victimization.

## Project Abstract (專案摘要)

Traditional sociological studies often isolate race and gender when monitoring youth risk behaviors. This project applies an intersectional framework to evaluate how structural vulnerability operates across compounding identities. Our empirical results from Ordinary Least Squares (OLS) regression models uncover an intersectional premium: minoritized female youth suffer disproportionately higher frequencies of objective weapon threats and physical injuries on school grounds than traditional additive models predict.

## Variable Operationalization (變數操作化定義)

### 1. Independent Predictors (自變數)
* **Is_Female**: Binary indicator representing biological sex (1 = Female, 0 = Male baseline).
* **Is_Minority_Race**: Binary indicator capturing racial background (1 = Minority, 0 = Non-Hispanic White baseline).

### 2. Dependent Risk Indices (應變數)
* **School_Safety_Index**: Standardized continuous frequency score tracking subjective anxiety and school avoidance due to safety fear over the past 30 days.
* **Weapon_Threat_Index**: Standardized continuous frequency score tracking objective weapon intimidation and physical injuries on school property over the past 12 months.

## Core Visual Insights (核心視覺化洞察)

* **Figure 1 (Sample Composition)**: Establishes a balanced demographic distribution across the 13,019 student analytical matrix.
* **Figure 2 (Risk Distributions)**: Demonstrates that severe school violence measures are highly right-skewed extreme events, validating the application of robust linear model fitting.
* **Figure 3 (Psychological Anxiety)**: Illustrates that minoritized students, regardless of biological sex, exhibit uniform elevations in fearing for their safety on campus.
* **Figure 4 (Physical Victimization)**: Isolates a stark divergence where minority female youth break conventional gender stereotypes, facing the absolute highest rate of physical weapon intimidation.

## Final Conclusion (最終結論)

Our empirical analysis based on 13,019 student observations from the YRBS dataset demonstrates that school violence risks do not operate through simple additive demographic components, but rather through distinct intersectional pathways. The regression modeling uncovers a profound sociological premium: minoritized female youth suffer from a severe "Double Marginalization" effect that significantly amplifies their objective exposure to weapons and physical trauma on school grounds, outstripping the risk profiles predicted by single-variable evaluations. While minority students across both gender groups suffer from elevated psychological safety anxiety and school avoidance, it is the minority female cluster that carries the heaviest burden of material physical vulnerability. Because this study utilizes cross-sectional observational data, these findings confirm a robust multi-layered statistical association between compound social identities and systemic school victimization, but do not establish linear causal mechanisms.

本研究基於 YRBS 數據集中 13,019 位學生的觀測資料進行實證分析，結果證實校園暴力風險並非透過簡單的人口統計變數相加來運作，而是存在顯著的交織性路徑。迴歸模型分析揭示了一個深刻的社會學現象：少數族裔女性青少年正承受著嚴重的「雙重邊緣化」效應，這使得她們在校園內面臨實質武器威脅與身體傷害的風險顯著放大，遠遠超過了單一變數評估所預測的風險範疇。儘管少數族裔學生不分性別皆表現出較高的校園安全焦慮與逃學傾向，但少數族裔女性群體在實質身體脆弱性上承擔了最沉重的負擔。由於本研究採用橫斷面觀察性數據，此處結果證實了複合社會身份與系統性校園受害風險之間存在強烈的多層次統計相關性，但不具備推論線性因果關係之基礎。

## Reproducibility Protocol (重複性執行步驟)

To replicate the empirical results and export all summary files, execute the notebooks sequentially:

* **01_data_check.ipynb**: Cleans the database and drops incomplete survey records.
* **02_eda.ipynb**: Performs categorical breakdowns and saves the four standalone figure files.
* **03_inference.ipynb**: Runs Ordinary Least Squares regressions with interaction terms and exports the structural summary matrix.
