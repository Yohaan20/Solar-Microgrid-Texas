# ☀️ Texas Solar Microgrid Suitability Analysis

## Live Map
🗺️ [Click here to explore the interactive map](https://github.com/Yohaan20/Solar-Microgrid-Texas/settings/pages))

## Project Question
Which Texas counties have the highest potential for solar microgrids, 
and which underserved communities should be prioritized first?

## Motivation
In February 2021, Winter Storm Uri caused the Texas ERCOT grid to fail 
for 4.5 million residents. Low-income communities were hit hardest. 
This project uses data science to identify where solar microgrids could 
give those communities energy independence.

## Key Findings
- El Paso County scores highest (82.7/100) — high solar, moderate income
- Brewster County scores #2 (80.2/100) — highest solar potential + low income
- Dimmit County has lowest median income ($27,374) — most energy vulnerable
- West Texas dominates solar potential; South Texas shows highest energy need

## Methodology
1. Pulled solar irradiance data (GHI, DNI) for 49 Texas counties via NASA POWER API
2. Trained a Random Forest model to predict annual solar yield (R²=0.9978)
3. Scored all counties on 4 weighted factors:
   - Solar irradiance: 35%
   - Median household income (inverted): 25%
   - Grid vulnerability (distance from urban centers): 25%
   - Available land area: 15%
4. Built interactive choropleth map with folium

## Results
| County | Score | Annual Yield | Median Income |
|---|---|---|---|
| El Paso | 82.7/100 | 2,154 kWh/m²/yr | $55,417 |
| Brewster | 80.2/100 | 2,114 kWh/m²/yr | $47,747 |
| Pecos | 66.5/100 | 2,056 kWh/m²/yr | $59,325 |

## Tech Stack
Python · pandas · scikit-learn · pvlib · folium · NASA POWER API · US Census API

## Data Sources
- NASA POWER API — solar irradiance and temperature
- US Census ACS 2022 — median household income
- US Census TIGER — county land area

## Setup
```bash
pip install pandas numpy matplotlib scikit-learn pvlib folium requests
```
Run notebooks in order: data_collection → model → map

## Author
Yohaan Mutha | High School Data Science Project | 2026
