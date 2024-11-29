# Kia and Hyundai Vehicle Warranty Claims Analysis Dashboard

## Project Overview
This project focuses on analyzing warranty claims data for Kia and Hyundai vehicles from 2020 to 2024. Using the National Highway Traffic Safety Administration (NHTSA) dataset, the analysis aims to identify trends and actionable insights into defect types, repair durations, severity, and regional defect patterns. The data preprocessing was performed using Python, and the dashboard was created in Power BI.

---

## Data Preparation
The raw data was obtained from the NHTSA website:
- **Source**: [NHTSA Datasets and APIs - Complaints](https://www.nhtsa.gov/nhtsa-datasets-and-apis#complaints)

### Steps:
1. **Dataset Format**: The raw data was in `.txt` format and included complaints data from 2020 to 2024.
2. **Preprocessing**: Using Python, the following steps were applied:
   - Converted text files into a structured tabular format (CSV).
   - Filtered the data to include complaints related to Kia and Hyundai vehicles only.
   - Created derived columns such as:
     - `RepairDuration`: Difference between `DateFiled` and `RepairDate`.
     - `SeverityScore`: Numerical value for severity based on complaint details.
     - `MileageRange`: Categorized mileage into bins (e.g., 0-5k, 5k-10k).
3. **Upload to Power BI**: The preprocessed dataset was imported into Power BI for further analysis.

### Additional Data Transformation in Power BI:
Using DAX, additional calculations were performed:
- Created measures for high-severity complaint counts.
- Implemented custom calculations for trends over time and defect distributions.

---

## Dashboard Features
The dashboard contains six distinct visualizations to address key analytical questions.

### 1. **Top Defect Types for Kia and Hyundai**
   - **Type**: Bar Chart
   - **Insights**: Highlights the most frequently reported defects for each manufacturer.
   - **Actionable Insight**: Engine and electrical system defects dominate the claims, indicating potential areas for product improvement.

### 2. **Impact of Mileage on Defect Severity**
   - **Type**: Scatter Plot
   - **Insights**: Shows the relationship between mileage and average severity score.
   - **Actionable Insight**: High-severity complaints are more concentrated in lower mileage ranges, suggesting potential manufacturing or design defects.

### 3. **Proportion of High-Severity Defects**
   - **Type**: Donut Chart
   - **Insights**: Breaks down high-severity defects by defect type.
   - **Actionable Insight**: Engine defects account for the largest proportion of high-severity claims.

### 4. **Defect Severity Trends Over Time**
   - **Type**: Line Chart
   - **Insights**: Tracks severity trends from 2020 to 2024 for both manufacturers.
   - **Actionable Insight**: Provides insight into how defect severity has evolved, helping to assess the impact of quality improvement initiatives.

### 5. **Regional Defect Patterns**
   - **Type**: Tree Map
   - **Insights**: Visualizes the frequency of complaints by state.
   - **Actionable Insight**: California, Florida, and Texas report the highest number of complaints, pointing to regional trends in vehicle performance.

### 6. **Repair Duration Distribution by Defect Type**
   - **Type**: Box Plot
   - **Insights**: Compares the distribution of repair durations for different defect types.
   - **Actionable Insight**: Certain defect types (e.g., Parking Brake) have significantly longer repair times, highlighting potential supply chain or technical challenges.

---
## Insights and Recommendations
1. **Focus on Engine Defects**: Engine-related issues are the most frequent and severe, requiring targeted investigation.
2. **Address Regional Trends**: States like California and Texas show high claim volumes; localized manufacturing or environmental factors may play a role.
3. **Optimize Repair Processes**: Prolonged repair durations for specific defect types should be addressed by streamlining parts supply chains.
4. **Monitor Severity Trends**: Regular monitoring of severity trends can help measure the success of quality improvement initiatives.

---

## Tools Used
- **Data Preparation**: Python (Pandas, NumPy)
- **Visualization**: Power BI
- **Dataset Source**: NHTSA Complaints Dataset (2020–2024)

---

## How to Use
1. Open the `dashboard.pbix` file in Power BI.
2. Interact with the visualizations to explore specific trends and insights.
3. Apply filters (e.g., Manufacturer, Defect Type) for a customized view.

---

