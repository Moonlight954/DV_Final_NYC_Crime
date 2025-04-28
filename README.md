# DV_Final_NYC_Crime
# NYC Arrests Data Analysis

This project focuses on analyzing NYPD arrest records in New York City, enriched with neighborhood and police precinct information.  
The final dataset integrates location, demographic, crime type, and precinct metadata, providing a comprehensive view suitable for further visualization and analysis (e.g., Tableau, Power BI).

---

## 📚 Data Sources

- [2020 Neighborhood Tabulation Areas (NTAs) | NYC Open Data](https://data.cityofnewyork.us/City-Government/2020-Neighborhood-Tabulation-Areas-NTAs-/9nt8-h7nd/about_data)  
  *Used for matching arrests to NYC neighborhoods based on geolocation.*

- [NYPD Arrest Data (Year to Date) | NYC Open Data](https://data.cityofnewyork.us/Public-Safety/NYPD-Arrest-Data-Year-to-Date-/uip8-fykc/about_data)  
  *Current year NYPD arrest records.*

- [NYPD Arrests Data (Historic) | NYC Open Data](https://data.cityofnewyork.us/Public-Safety/NYPD-Arrests-Data-Historic-/8h9b-rp9u/about_data)  
  *Historic NYPD arrest records covering prior years.*

- [Police Precincts | NYC Open Data](https://data.cityofnewyork.us/City-Government/Police-Precincts/y76i-bdw7/about_data)  
  *Geographic boundaries of NYPD precincts (used for spatial context).*

- [Precincts - NYPD Official Website](https://www.nyc.gov/site/nypd/bureaus/patrol/precincts-landing.page)  
  *Precinct-level metadata including commanding officers and addresses (scraped using custom scripts).*

---

## 🛠️ Processing Steps

1. **Arrest Data Cleaning**:  
   - Standardized borough names, suspect demographics, crime categories.
   - Converted latitude and longitude to numeric formats.
   - Dropped invalid or missing coordinate entries.

2. **Neighborhood Enrichment**:  
   - Mapped arrest locations to NYC Neighborhood Tabulation Areas (NTAs) via spatial joins.

3. **Precinct Metadata Integration**:  
   - Mapped each arrest record to its corresponding NYPD precinct and borough.

4. **Final Dataset Export**:  
   - Saved as a cleaned and enriched CSV ready for analysis.

---

## 📦 Final Deliverable

- `nyc_arrests_full_cleaned.csv`  
  *(6057262 rows × 24 columns)*  
  Contains arrest details along with geographic and precinct-level metadata, ready for visualization.

---

## ✨ Potential Visualizations

- Arrest distribution by Neighborhood and Borough
- Crime type breakdown (felonies, misdemeanors, violations)
- Temporal trends in arrests (monthly, yearly)
- Demographic analysis (race, sex) of arrestees
- Geographic precinct-based crime heatmaps

---

## 💬 Notes

- Spatial joins were performed using GeoPandas with appropriate CRS (EPSG:4326) alignment.
- Custom scraping scripts were used for precinct officer metadata from the official NYPD site.

---
