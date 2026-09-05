# Solar Energy Optimization & Microgrid Mapping — Texas

## Project Question
Which Texas counties have the highest potential for solar microgrids,
and which underserved communities should be prioritized first?

## Motivation
In February 2021, Winter Storm Uri caused the Texas power grid (ERCOT)
to fail for millions of residents — some for over a week in freezing
temperatures. Low-income communities were hit hardest and had the fewest
resources to recover. This project uses data science to identify where
solar microgrids could give those communities energy independence,
so a grid failure never has the same impact again.

## What This Project Does
- Pulls real solar irradiance data from NASA POWER API
- Builds a machine learning model to predict solar energy yield by county
- Scores all 254 Texas counties on microgrid suitability
- Visualizes results on an interactive map

## Tools Used
Python, pandas, scikit-learn, pvlib, geopandas, folium

## Data Sources
- NASA POWER API (solar data)
- US Census Bureau (income data)
- ERCOT (grid reliability data)

## Author
Yohaan Mutha | High School Data Science Project | 2026

## Data Sources
- NASA POWER API — solar irradiance (GHI, DNI) and temperature
- US Census ACS 2022 — median household income by county
- USGS/Census TIGER — land area by county

## Key Early Findings
- El Paso and Brewster counties have highest solar potential (246 W/m² avg GHI)
- Dimmit County has lowest median income ($27,374) — most energy vulnerable
- Brewster County is both high solar AND low income — top microgrid candidate
- Income range across Texas counties: $27K–$113K showing stark inequality
- West Texas dominates solar potential; South Texas dominates energy vulnerability
