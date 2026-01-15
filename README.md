# Transit Access Inequity in Los Angeles County  
Spatial analysis of socioeconomic vulnerability and proximity to LA Metro bus stops

## Table of Contents
- [About](#about)
- [Research Questions](#research-questions)
- [Data](#data)
- [Workflow](#workflow)
- [Key Results](#key-results)
- [Recommendations](#recommendations)
- [Project Files](#project-files)
- [Authors](#authors)
- [References](#references)

## About
This project investigates **transportation equity in Los Angeles County** by analyzing the spatial relationship between **socioeconomic variables** (poverty, income, poverty probability index, and households without a vehicle) and **proximity/density of LA Metro bus stops**. The goal is to identify where transit need is highest and whether bus stop infrastructure aligns with that need. :contentReference[oaicite:0]{index=0}

## Research Questions
1. Where is the highest concentration of socioeconomically vulnerable people within Los Angeles County?
2. Do these communities have enough access to bus stops, or is there a deficit relative to need?
3. What patterns emerge across income, poverty, and vehicle access that can inform transit planning? :contentReference[oaicite:1]{index=1}

## Data
### Layers Used
| Layer | Description | Source | Geometry |
|------|-------------|--------|----------|
| LA Metro Bus Stops | Point locations of LA Metro bus stops | LA Metro GTFS (`stops.txt`) | Points |
| Bus Stop Kernel Density Surface | Concentration of bus stops | Generated in ArcGIS Pro (Kernel Density) | Raster |
| Median Household Income (ACS 2023) | Income by census tract | ACS 2023 via Esri Enrichment | Polygons |
| Poverty Index (ACS 2023) | Poverty indicators by tract | ACS 2023 via Esri Enrichment | Polygons |
| Households Without a Vehicle (ACS 2023) | Zero-vehicle households by tract | ACS 2023 via Esri Enrichment | Polygons |
| LA County Boundary | Clip/analysis boundary | TIGER/Line 2023 | Polygons | :contentReference[oaicite:2]{index=2}

## Workflow
1. **Collect & prepare datasets**
   - Import GTFS bus stops and census-tract socioeconomic layers
   - Clip layers to the Los Angeles County boundary :contentReference[oaicite:3]{index=3}
2. **Create bus stop density surface**
   - Use **Kernel Density** in ArcGIS Pro to generate a raster surface of bus stop concentration :contentReference[oaicite:4]{index=4}
3. **Map socioeconomic vulnerability**
   - Thematic mapping of:
     - Median household income
     - Poverty Probability Index
     - Households without a vehicle :contentReference[oaicite:5]{index=5}
4. **Compare need vs. access**
   - Visually assess mismatches between high-need areas and bus stop density
   - Review correlation results referenced in the report (weak relationship between poverty and bus stop count) :contentReference[oaicite:6]{index=6}

## Key Results
- Socioeconomic disadvantage is concentrated in **South Los Angeles, East Los Angeles, and parts of the San Fernando Valley** (low income, higher poverty, higher rates of households without cars). :contentReference[oaicite:7]{index=7}
- **Bus stop density is highest in Downtown Los Angeles**, decreasing farther from the urban core. :contentReference[oaicite:8]{index=8}
- Areas such as **Compton and East Los Angeles** show **high transit dependency** (many households without vehicles, low income) but **lower bus stop density** compared to transit-rich areas like Koreatown/Downtown. :contentReference[oaicite:9]{index=9}
- The report notes a **weak correlation** between poverty and number of bus stops (R² ≈ 0.03), suggesting transit infrastructure does not strongly track poverty levels. :contentReference[oaicite:10]{index=10}

## Recommendations
- Prioritize **targeted transit expansion** in **Compton and East Los Angeles** to improve transportation equity.
- Improve stop-area safety and usability (e.g., lighting, safer crossings) where upgrades are needed.
- Focus investments on **underserved, transit-dependent communities** rather than areas already well served. :contentReference[oaicite:11]{index=11}

## Project Files
- `BusStopsSpatialAnalysis.aprx` — ArcGIS Pro project
- `Spatial Analysis Project Report.docx` — Full written report and discussion :contentReference[oaicite:12]{index=12}

## Authors
- Brandon Acosta  
- Fong Lieu  
- Marcela Lozano  
- Yarden Sasson  
- Jessica Thai :contentReference[oaicite:13]{index=13}

## References
- Los Angeles County Metropolitan Transportation Authority. GTFS Schedule Data – Metro Open Data. (Retrieved Dec 9, 2025)
- Poverty Probability Index (PPI). Measure Poverty Outreach. (Retrieved Dec 6, 2025)
- U.S. Census Bureau (2018–2022 ACS 5-Year). Tables B08201, B19013 (Retrieved Dec 9, 2025) :contentReference[oaicite:14]{index=14}
