# **Building Energy Rating (BER) Dataset Analysis**

This project focuses on analyzing Ireland's **Building Energy Rating (BER)** data to streamline energy efficiency evaluations for residential properties. The dataset contains over **1 million records and 211 attributes**.


## **Dataset Overview**

- **Source**: SEAI-National BER Research tool ([Link](https://ndber.seai.ie/BERResearchTool/ber/search.aspx)).
- **Size**: Over 1 million rows, 211 columns (Over 1 GB in size).
- **Attributes**:
  - **Energy Ratings**: BER scores and CO2 emissions for properties.
  - **Property Features**: Construction year, dwelling type, floor area, wall area, roof type, etc.
  - **Heating Systems**: Types of main and supplementary heating systems, efficiency ratings, and fuel types.
  - **Energy Usage**: Delivered and primary energy usage for lighting, heating, and ventilation.
  - **Insulation Data**: Wall and roof U-values, insulation types, and draught-proofing measures.
  - **Assessment Data**: Date of BER assessment, purpose (sale, rent, or grant), and provisional vs. final ratings.


## **Possibilities of the Project**

The BER dataset provides opportunities to:
1. Explore energy efficiency across properties and regions.
2. Identify patterns and provide actionable insights for policy-making or marketing strategies.

### **Goals**:
- Identify key factors affecting energy efficiency (e.g., dwelling type, construction year).
- Compare energy usage patterns and CO2 emissions across regions.
- Examine trends in energy ratings over time or across building categories.
- Highlight areas where retrofitting or energy efficiency improvements are needed.
- Provide visual insights via interactive dashboards to support decision-making.


## **Key Questions to Explore**

1. How does construction year influence energy efficiency ratings?
2. Which regions or property types have the highest CO2 emissions?
3. What percentage of properties utilize renewable energy sources?
4. What are the trends in energy usage and emissions across years?
5. Are larger properties less energy-efficient compared to smaller ones?
6. Are semi-exposed walls or certain insulation types correlated with higher energy losses?
7. How do provisional ratings compare with final ratings for new dwellings?


## **Project Progress**

This project is ongoing, with the next steps focused on **Exploratory Data Analysis (EDA)** and **Dashboard Development** using **Power BI**. The cleaned dataset is now ready for detailed analysis.


## **Steps Taken**

1. **Data Loading and Inspection**:
   - Loaded the dataset into a Python environment using **Azure Machine Learning Studio**.
   - Inspected column types, unique values, and memory usage to design a cleaning strategy.

2. **Data Cleaning Strategy**:
   - Focused on preserving data integrity while ensuring SQL compatibility.
   - Addressed inconsistencies such as:
     - Incorrect relationships between `Year_of_Construction` and `DateOfAssessment`.
     - Anomalous values in `WallArea`, `UValue`, and Boolean columns.
   - Resolved missing values using strategies:
     - **Categorical**: Filled with "Unknown."
     - **Numerical**: Imputed using the median.
     - **Boolean**: Replaced missing values with `False`.

3. **Column Standardization**:
   - Renamed columns to SQL-compatible formats by replacing spaces and special characters.

4. **Handling Outliers**:
   - Kept outliers for later analysis in the **Exploratory Data Analysis (EDA)** phase.

5. **Key Inconsistencies Identified**:
   - Example: Semi-exposed walls with unusually low UValues.
   - Retained these anomalies for further investigation during EDA.

6. **SQL Compatibility Preparation**:
   - Converted Boolean columns to `0/1`.
   - Transformed datetime columns to string format.
   - Flagged columns with >50% missing values for potential exclusion during analysis.

7. **SQL Server Integration**:
   - Prepared the cleaned dataset for ingestion into **Azure SQL Database** using **Azure Data Factory**.
   - Ensured schema compatibility and uploaded the data for further analysis.


## **Tools and Technologies Used So Far**

- **Python**: Pandas, NumPy for data processing and cleaning.
- **Azure Ecosystem**:
  - **Azure Blob Storage**: For raw and cleaned dataset storage.
  - **Azure Machine Learning Studio**: For data cleaning and preparation.
  - **Azure SQL Database**: For structured data storage.
  - **Azure Data Factory**: For creating pipelines to move data between services.
- **Power BI**: Planned for dashboard development.
- **VS Code**: Integrated with Azure ML for coding.

Continued
