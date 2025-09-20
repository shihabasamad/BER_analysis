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

## Key Insights

### 1. Fabric drives performance
Wall, roof, and window U-values are the strongest predictors of BER.  
<img width="468" height="273" alt="Picture1" src="https://github.com/user-attachments/assets/475619e2-22bd-4f0f-8011-40830a2ddd4e" />
Feature Importance: Fabric vs Systems

---

### 2. Year of construction matters
Post-2010 homes are mostly A/B-rated, while pre-1980 homes cluster in D–G.  
<img width="561" height="396" alt="Picture2" src="https://github.com/user-attachments/assets/7b104e6d-ee99-43bf-ba91-0c3e9db88207" />
BER vs Year of Construction

---

### 3. Dwelling type differences
- Apartments are most efficient per m².  
- Detached homes are least efficient.  
<img width="541" height="368" alt="Picture3" src="https://github.com/user-attachments/assets/1cee6bbf-06c9-4d93-b833-9c928ef5dd12" />
BER by Dwelling Type

---

### 4. Heating systems & fuel
- Efficient boilers/heat pumps reduce BER.  
- Oil/solid fuel homes emit 2–3× more CO₂ than gas/heat pumps.  
<img width="541" height="368" alt="Picture3" src="https://github.com/user-attachments/assets/7e77ef91-df9e-4685-8bc8-212bd086099f" />
Impact of Boiler Efficiency on BER

---

### 5. Regional differences
Eastern counties (Dublin, Kildare, Meath) perform best; West/Midlands lag behind.  
<img width="624" height="688" alt="Picture5" src="https://github.com/user-attachments/assets/11fe9d8c-25b6-4209-bbc0-ba65077ea0c9" />
BER Distribution by County

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
