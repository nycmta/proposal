Project Proposal
================

## Group Members

- William M. Donovan (wd2328)
- Hantang Qin (hq2229)
- Yongyan Liu (yl6107)
- Yijun Wang (yw4664)
- Heng Hu (hh2648)

## Tentative Project Title

*Weather, Storms, and Big Events: Station-Level Impacts on Manhattan
Subway Ridership*

## Motivation

Transit demand in New York City fluctuates with extreme weather events
(heat waves, heavy rain, snowstorms) and large-scale events (parades,
holiday gatherings, Times Square festivities). This project aims to
quantify station-level ridership changes in Manhattan associated with
weather conditions and permitted events from 2024 to 2025. Manhattan
hosts the majority of major NYC events and has consistent weather
monitoring through Central Park station, making it ideal for studying
these relationships. Our findings will inform service planning, system
resilience, and rider communications.

## Intended Final Products

This project will develop an analytical framework to quantify how
extreme weather and large-scale events are associated with subway
ridership patterns in Manhattan.

Through data wrangling, fixed-effects modeling, and event-window
analyses, we aim to isolate station-level responses to heat waves,
storms, and public gatherings, while documenting assumptions and
limitations.

The main output will be empirical estimates of the magnitude and timing
of ridership changes under different conditions.

Building on these results, we will explore a preliminary predictive
model for short-term ridership changes during future weather extremes
and major events, which may inform service planning and resilience
efforts.

## Anticipated Data Sources

- **MTA Subway Hourly Ridership** (2024-2025): Station-level hourly
  ridership for 123 Manhattan stations; datasets `wujg-7c2s` (2024) and
  `5wq4-mkjj` (2025) from NY Open Data; ~1.92M hourly observations
- **Weather Data**: NOAA GHCN-Daily from Central Park Station
  (USW00094728) including daily maximum temperature, precipitation, and
  snowfall (2024-2025)
- **NYC Permitted Events**: Event permits from NYC Open Data including
  dates, locations, and event types for Manhattan (2024-2025)
- **Station Geocoding**: MTA station complex locations with coordinates
  for spatial analysis

## Planned Analyses, Visualizations, and Coding Challenges

**Analyses**

***Data Wrangling***  
- Create station-day aggregates  
- Define weather indicators: *Heat waves*: max temp ≥ 90°F for ≥ 3 days;
*Storms*: precipitation ≥ 1 inch  
- Geocode event locations and spatially join to the nearest station
complex

***Modeling***  
- Within-station fixed effects models controlling for station and date
fixed effects to estimate impacts of weather and events on
log(ridership)  
- Hourly event-window analyses for selected venues

***Sensitivity Analysis***  
- Alternative weather thresholds  
- Station type interactions

**Visualizations**

- Calendar heatmaps and time series plots for high-traffic stations
- Manhattan maps showing percent change in ridership during heat waves,
  storms, and major events
- Station-type comparisons: transfer hubs vs. local stations

**Coding Challenges:**

- Managing Socrata API pagination for large hourly ridership datasets
- Geocoding event locations and spatially joining to nearest station
  complexes (within 600-800m)
- Defining clean event windows and handling overlapping permits
- Handling missing hourly observations (~1% of records)

## Planned Timeline

- **Nov 7, 1:00 PM:** Submit project proposal
- **Nov 8-12:** Initial data pulls; create exploratory plots; define
  weather and event indicators
- **Nov 10-14:** Project review meeting with teaching team
- **Nov 15-30:** Complete EDA, fit models, conduct sensitivity analyses,
  draft report
- **Dec 1-6:** Finalize report and website; record screencast
- **Dec 6, 11:59 PM:** Submit final deliverables
- **Dec 11:** In-class project discussion
