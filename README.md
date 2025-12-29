## BI Internship – End-to-End Microsoft BI Projects

### Overview

This repository showcases selected work from my industry-based Business Intelligence / Data Analytics internship, where I designed and implemented end-to-end BI solutions using the Microsoft stack.

I built pipelines starting from raw CSV / Excel / flat files and progressed to more advanced solutions handling multiple files from folders, including consolidation using Union All in SSIS.

The work includes:
- ETL with SSIS
- Data warehouse design in SQL Server
- Paginated reporting in SSRS
- Interactive dashboards in Power BI

The analysis focuses on property, crime, and house value datasets, etc designed using a Kimball-style star schema with shared dimensions.

---

###  Demo Video

The video in this repository demonstrates:
- a Power BI dashboard
- navigation from Power BI to linked SSRS report pages

If it does not preview in the browser, download and play locally.

---

##  What this repository contains

This repository includes selected screenshots and the demo video showing:

- SSIS control flows
- SSIS data flows
- single-file ingestion pipelines
- multi-file folder ingestion using Union All
- star-schema database diagrams in SQL Server
- SQL validation queries
- Power BI dashboards
- SSRS report previews linked from Power BI

Screenshots are used instead of raw data to maintain confidentiality.

---

##  End-to-End Architecture

Raw files (single file & multiple files in folder)  
→ SSIS load to staging tables  
→ SSIS transforms and lookups  
→ Dimension & Fact tables (Kimball star schema)  
→ SQL Server data warehouse  
→ SSRS paginated reports  
→ Power BI dashboards (with links to SSRS)

---

##  Work completed during internship

During this internship, I:

- built ETL for single CSV / Excel / flat files  
- extended ETL to multiple files from folders  
- used Union All to consolidate multi-file inputs  
- implemented Derived Column, Data Conversion, Lookup  
- created staging, dimension, and fact tables using SQL  
- validated row counts and joins in SSMS  
- designed SSRS reports with parameters  
- built Power BI dashboards with slicers and KPIs  
- linked Power BI dashboards to SSRS reports  

The warehouse was designed using Kimball star schema principles with:

- shared Time, Geography, and School dimensions etc measures
- fact tables for property values, crime data, and school metrics  

---

##  Tools & Skills Demonstrated

- SSIS ETL (single-file and multi-file pipelines)  
- Union All for consolidating folder-based inputs  
- Data warehouse design (Kimball/star schema)  
- SQL Server (table creation, validation queries)  
- SSRS paginated reporting with parameters  
- Power BI dashboards and report navigation  
- End-to-end BI solution design from raw files to insights  

---

###  Confidentiality Note

- No internship raw data is shared  
- Only screenshots and my own demo video are included  
- Any identifying names or logos were removed or avoided  


