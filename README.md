# Building Energy Rating (BER) Analysis

## Overview
Homes use a large share of a country’s energy and produce a big part of CO₂ emissions. Making them more energy efficient saves money on bills, helps the environment, and supports government climate goals. The Building Energy Rating (BER) system measures this efficiency on a simple scale from A (best) to G (worst), based on annual energy use per square metre.  

This project uses a dataset of **1 million+ Irish dwellings** to:
- Identify the **key drivers** of BER scores.  
- Explore patterns by **year of build, dwelling type, size, heating system and geography**.  
- Assess the **impact of retrofits** (insulation, boilers, solar).  
- Provide **recommendations** to improve efficiency and reduce emissions.  

---

## Research Questions
The work is guided by **10 questions**, grouped into **5 themes**:

**A. Energy Efficiency Factors and Ratings**

- RQ1: What are the strongest predictors of BER?  
- RQ2: How does construction year affect BER?  
- RQ3: How does dwelling type (detached, apartment, etc.) influence BER?  
- RQ4: How does floor area relate to energy intensity?  

**B. Energy & Emissions**
- RQ5: How do heating systems and fuels affect energy and CO₂?  
- RQ6: Which dwelling types emit the most CO₂ overall?  

**C. Geography**
- RQ7: Are there regional differences in BER?  
- RQ8: Do counties differ in energy use and emissions?  

**D. Retrofits**
- RQ9: How do insulation, solar, and boiler upgrades impact BER?  

**E. Targeting Worst Homes**
- RQ10: How can we identify the least efficient (worst 20%) homes?  
*RQ_ = Research Question
---

## Methodology
- **Data**: SEAI BER Research Tool (~1,048,000 homes, 200+ features).  
- **Cleaning**: handled missing values, corrected types, removed duplicates.  
- **Analysis**:  
  - Correlation checks and feature importance (Random Forest).  
  - Group comparisons (dwelling type, build era, retrofits).  
  - Trend analysis with smoothing.  
  - Decision tree to flag worst-performing homes.  
- **Visualization**: boxplots, scatter plots, heatmaps, county maps.  

---

## Key Findings
- **Fabric dominates**: Wall, roof, and window U-values are the strongest predictors of BER.  
- **Heating systems**: Efficient boilers/heat pumps improve BER by ~60–80 kWh/m².  
- **Construction year**: Post-2010 homes are mostly A/B-rated; pre-1980 homes cluster in D–G.  
- **Dwelling type**: Apartments perform best per m²; detached homes are least efficient.  
- **Floor area effect**: Larger homes tend to have slightly lower energy use per m² (“dilution effect”).  
- **Fuel choice matters**: Oil/solid fuels emit 2–3× more CO₂ than gas or heat pumps.  
- **Regional divide**: East/urban counties (Dublin, Kildare) perform better; west/midlands (Leitrim, Roscommon) lag.  
- **Retrofits**:  
  - Wall insulation improves BER by ~20–30 kWh/m².  
  - Efficient boilers cut ~81 kWh/m².  
  - Solar has little direct BER effect but helps with CO₂.  
- **Worst homes**: High wall U-values + inefficient boilers = strong predictor of F/G ratings.  

---

## Recommendations
1. **Fabric + Heat First**  
   - Prioritise wall/roof insulation and efficient heating upgrades before renewables.  
2. **Target Worst Performers**  
   - Focus on pre-1980 rural homes with poor insulation and old boilers.  
3. **Regional Focus**  
   - Direct grants and retrofit schemes to west/midland counties.  
4. **Policy & Equity**  
   - Support fuel-poor households.  
   - Bundle grants (insulation + heat pump) for maximum impact.  

---
## Repository Structure
├── BERcleaning.ipynb          # Data cleaning and preparation  
├── BER_analysis_final.ipynb   # Main analysis and visualizations  
├── BER_analysis_report.docx   # Full detailed report (academic format)  
├── README.md                  # Project overview (this file)  

---

## Tools & Libraries
- Python: pandas, NumPy, matplotlib, seaborn, scikit-learn
- Azure Machine Learning – for dataset connection and data cleaning workflow  
- Azure Blob Storage – for storing and accessing the raw dataset
- Jupyter Notebook  
- Power BI (Inprogress)
- Data Source: [SEAI BER Research Tool](https://ndber.seai.ie/BERResearchTool/ber/search.aspx)  

---

## Author
**Md Shihab As Samad**  
