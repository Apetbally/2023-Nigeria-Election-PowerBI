# 🗳️ 2023 Nigerian Presidential Election Results Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Microsoft](https://img.shields.io/badge/Microsoft-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

## 📊 Project Overview
An interactive Power BI dashboard analysing the 2023 Nigerian Presidential 
Election results as announced by INEC. The report covers all 36 states and 
FCT, visualising vote distributions across the four major parties: APC, PDP, 
LP, and NNPP.

---

## 🛠️ Tools Used
- **Power BI Desktop** — Report building and visualisation
- **Power Query** — Data cleaning and transformation
- **DAX** — Calculated columns and measures
- **Microsoft Bing Maps** — Geographic visualisation

---

## 📁 Dataset
- **Source:** INEC Official Presidential Election Results 2023
- **Format:** CSV
- **Records:** 37 states × 4 parties = 148 rows (after unpivoting)
- **Columns:** STATE, Party, Votes, Geopolitical Zone, Winner

---

## 🧹 Data Cleaning Steps (Power Query)
1. Removed AGGREGATE total row
2. Removed commas from vote numbers
3. Removed spaces from vote numbers
4. Trimmed all text columns
5. Changed party columns from Text to Whole Number
6. Converted STATE column to UPPERCASE
7. Unpivoted party columns to long format
8. Renamed columns to STATE, Party, Votes

---

## 🔗 Data Modelling
- Created **Coordinates table** with Latitude and Longitude for all 37 states
- Established **Many-to-One relationship** between Elections and Coordinates
- Set data categories: Latitude, Longitude, State or Province
- Created **_Measures table** to organise all DAX measures
- Added **Geopolitical Zone** calculated column using SWITCH DAX function
- Added **Winner** calculated column per state

---

## 📐 DAX Measures
| Measure | Description |
|---------|-------------|
| Total Votes | Sum of all votes |
| APC Votes | Total votes for APC nationally |
| PDP Votes | Total votes for PDP nationally |
| LP Votes | Total votes for LP nationally |
| NNPP Votes | Total votes for NNPP nationally |
| National Winner | Overall winning party |
| Winning Margin | Vote gap between 1st and 2nd place |
| States Won | Number of states won per party |

---

## 📄 Report Pages

### Page 1 — National Overview
- KPI cards showing total votes per party
- National Winner card
- Clustered bar chart showing votes by party per state
- Party slicer for interactive filtering

### Page 2 — Geopolitical Analysis
- Interactive Nigeria bubble map coloured by winning party
- Geopolitical Zone bar chart
- Party button slicer for map filtering
- Cross filtering between map and zone chart

### Page 3 — State Detail (Drill Through)
- Drill through from any state on Page 1 or 2
- State name, total votes and winner cards
- Bar chart showing all party votes for selected state
- Back navigation button
- Key findings summary

---

## 🔍 Key Findings
APC won the 2023 Nigerian Presidential Election with 8.8 million votes, 
defeating PDP who came second with 6.9 million votes. Regional voting 
patterns were strongly evident, with LP dominating the South East and 
winning Lagos, NNPP securing Kano with nearly 1 million votes, and APC 
controlling most of the North West. The results highlight that no single 
party had national dominance, as voting behaviour was heavily influenced 
by geopolitical zones and regional loyalties.

---

## 📸 Dashboard Screenshots

### Page 1 — National Overview
![Page 1](screenshots/page1.png)

### Page 2 — Geopolitical Analysis
![Page 2](screenshots/page2.png)

### Page 3 — State Detail
![Page 3](screenshots/page3.png)

---

## 👩‍💻 Author
**Apete Balikis Olanike**
- 3MTT Fellow — Airtel Nextgen Cohort
- Data Analyst | Power BI | SQL | Python
- [LinkedIn](#) | [GitHub](#)

---

## 📌 Note
This project was built as part of the **Microsoft PL-300 Power BI Data Analyst** 
certification learning path.
