# BEACONs Movement Mapper

Updated: August 25, 2025

The function of the Movement Mapper is to assist in mapping movement segments e.g., to defining seasonal migration periods.

## Running the app

- https://beaconsproject.shinyapps.io/movement_mapper/

## Workflow

1. Start the app

2. Define segments using sliders
  - load caribou movement data ("caribou.csv")
  - select the Caribou and Year
  - use the Spring and Fall sliders to define start and end dates
  - save segments after each Id/Year combination

## Notes

- NSD is calculated for each caribou for each year, starting on Jan 1st.
- Start and end dates are calculated form day-of-year minus 1 since year starts on Jan 1st.
