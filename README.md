## BI Internship Projects – End-to-End Microsoft BI Stack

### Overview

This repository showcases selected work from my **industry-based BI / Data Analytics internship**, where I built end-to-end solutions using the **Microsoft BI stack**:

- **SSIS** – ETL from raw CSV/Excel/flat files into staging and data warehouse tables  
- **SSMS (SQL Server)** – data modelling, star schema design, table creation, and validation  
- **SSRS** – paginated reports with parameters and clean layouts  
- **Power BI** – interactive dashboards with slicers, KPIs, and visual storytelling  

The projects focus on **property analysis, crime analysis, and house value trends**, etc designed using a **Kimball-style star schema** and data warehouse approach.

---

### Architecture & Data Warehouse Design

Across both projects, I followed a standard BI architecture:

1. **Raw data** (CSV / Excel / flat files)
2. **Staging tables** in SQL Server
3. **Cleaned and transformed data** loaded into dimension and fact tables
4. **Star schema** designed using Kimball methodology
5. **Reporting layer** – SSRS paginated reports
6. **Analytics & dashboards** – Power BI visuals and slicers

Key design elements:

- **Dimensions** such as:
  - Time (Dim_Time)
  - Geography (Dim_Geography)
  - School (Dim_School)
- **Facts** such as:
  - Property values (Fact_Property_Value)
  - Crime metrics / incidents
  - School metrics

I also considered a **bus matrix** to ensure shared dimensions (Time, Geography, School) could support multiple subject areas.

**Artifacts:**

- Star schema / database diagram (e.g. `03ssmsdiagram.png`)
- Example SQL scripts for table creation and validation (in `/sql` if added)

---

### Project 1 – Single-File ETL (Property / House Value Analysis)

**Goal:**  
Build an end-to-end pipeline from **single CSV/Excel/flat files** into a star-schema data warehouse, and create reports and dashboards for property / house value analysis.

**Process:**

1. **Extract:**
   - Loaded raw property/house value data from a single source file into **staging tables** using SSIS.

2. **Transform:**
   - Cleaned and standardised columns (dates, geography, numeric values).
   - Used **Derived Column**, **Data Conversion**, and **Lookup** to map to dimension keys.

3. **Load:**
   - Loaded cleaned data into **dimension and fact tables** in SQL Server.

4. **Validate:**
   - Checked row counts, joins, and sample outputs in **SSMS**.

5. **Report & Visualise:**
   - Built **SSRS reports** to show house values by state, city, suburb, using parameters.
   - Built **Power BI dashboards** with slicers and KPIs to analyse trends and comparisons.

**Example screenshots:**

- `01ssiscontrolsingle.png` – SSIS Control Flow for the single-file ETL  
- `02ssisflowsingle.png` – SSIS Data Flow with Derived Column and Lookup  
- `03ssmsdiagram.png` – Star schema / database diagram in SSMS  
- `04ssrspropertyreport.png` – SSRS report preview (house value / property analysis)  
- `05pbdashboardproperty.png` – Power BI property/house value dashboard  

---

### Project 2 – Multi-File ETL (Folder Source with UNION ALL)

**Goal:**  
Extend the ETL process to handle **multiple files in a folder** (e.g. multiple months or regions), using **UNION ALL** in SSIS, and integrate this into the same data warehouse.

**Process:**

1. **Extract (multiple files):**
   - Configured **SSIS** to load data from multiple files in a folder.
   - Used multiple sources combined with **Union All** in the Data Flow.

2. **Transform:**
   - Applied common transformations across all files:
     - **Derived Column** for calculated or cleaned fields
     - **Data Conversion** for consistent data types
     - **Lookup** to map to dimension keys

3. **Load:**
   - Loaded consolidated, cleaned data into the same **fact tables** used in Project 1.

4. **Validate:**
   - Used **SSMS** to verify totals across all files and confirm data correctness after Union.

5. **Report & Visualise:**
   - Extended / created **SSRS reports** to use the expanded dataset.
   - Updated or built **Power BI dashboards** to show trends over time, across more periods or regions.

**Example screenshots:**

- `06ssiscontrolmulti.png` – SSIS Control Flow for multi-file ETL  
- `07ssisflowmultiunion.png` – Data Flow showing multiple sources with Union All  
- `08ssisflowmultilookup.png` – Data Flow with transformation and lookups after Union  
- `09ssmsvalidation.png` – SSMS validation query (row counts / sample joins)  
- `10ssrscombinedreport.png` – SSRS report preview (e.g. crime, schools, or combined metrics)  
- `11pbdashboardcrime.png` – Power BI crime/incident analysis dashboard  
- `12pbdashboardsummary.png` – Summary dashboard showing key metrics and trends  

---

### Tools & Skills Demonstrated

- **Data Warehouse & Modelling**
  - Kimball-style star schema (facts and dimensions)
  - Bus matrix thinking for shared dimensions

- **ETL – SSIS**
  - Loading from CSV / Excel / flat files
  - Using staging tables
  - Derived Column, Data Conversion, Lookup, Union All
  - Handling both single-file and multi-file scenarios

- **SQL / SSMS**
  - Creating staging, dimension, and fact tables via SQL scripts
  - Validating data with joins and row counts
  - Working directly in SQL Server Management Studio

- **Reporting – SSRS**
  - Designing paginated reports
  - Using parameters (e.g. state, city, suburb)
  - Working with multiple datasets

- **Dashboards – Power BI**
  - Connecting to the data warehouse
  - Building dashboards with slicers, KPIs, and visual storytelling
  - Analysing property, crime, and house value metrics

- **General BI Skills**
  - End-to-end thinking from raw data to insights
  - Data quality and validation
  - Presenting findings clearly to stakeholders/mentors

