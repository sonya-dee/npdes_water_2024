# EPA Water Pollutant Discharge Analysis

This project analyzes U.S. water pollutant discharge data reported through the **NPDES (National Pollutant Discharge Elimination System)** permits, using data from the **EPA's ECHO (Enforcement and Compliance History Online)** database. The focus is on pollutant loadings at the state and EPA region levels, with comparisons between **major** and **non-major** permit designations.

---

## Project Overview

Using data from the EPA's ECHO tool, this R Markdown report performs:

- Data cleaning and aggregation of state-level discharge records  
- Creation of visualizations, including:
  - Choropleth maps of total pollutant loads
  - Bar plots of top discharging states
  - Scatterplots comparing major and non-major dischargers
  - Distribution plots of reporting rates
  - Total discharges grouped by EPA Region

---

## Dataset

- **Source:** [EPA ECHO Water Pollutant Loading Tool](https://echo.epa.gov/)
- **File:** `discharge_state.csv`
- **Key Fields Include:**
  - Permit counts by state (major and non-major)
  - Pollutant loading totals (lbs/year)
  - Toxic-weighted loadings (lb-eq/year)
  - EPA region affiliations
  - Percent of permits with non-zero discharge

> ⚠️ Data was cleaned using `na.omit()` to remove missing values.

---

## Key Variables

| Variable | Description |
|----------|-------------|
| `Total.Pollutant.Pounds..lb.yr..for.Majors` | Annual total pollutant discharge by major permits |
| `Total.Toxic.Weighted.Pounds..lb.eq.yr..for.Majors` | Toxic-weighted discharges for major permits |
| `Majors.w..Pollutant.Loadings` | % of major permits with > 0 pollutant discharge |
| `EPA.Region` | EPA-assigned region (1–10) |

---

## Visual Outputs

- **Choropleth Map:** Total pollutant pounds discharged per state  
- **Top 10 Toxic Dischargers:** Ranked by toxic-weighted pounds  
- **Comparison Plot:** Major vs non-major pollutant discharges  
- **Boxplot:** Reporting rate distribution across states  
- **Regional Summary:** Total discharge by EPA region  

---

## R Packages Used

- `tidyverse`for data manipulation and wrangling  
- `ggplot2` for visualization  

---

## How to Run

1. Place `discharge_state.csv` inside the `./data/` folder  
2. Open `npdes_state_2024.Rmd` in RStudio  
3. Knit the file to **HTML** or **PDF** to render the full analysis  

---

## Further Research

- Break down results further by facility type or specific pollutants  
- Explore time-series trends using multi-year discharge data  

---

## License

This project uses publicly available data from the U.S. Environmental Protection Agency (EPA). Attribution is recommended when using the data or visualizations.

