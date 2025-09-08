# BEACONs Movement Mapper

The purpose of the Movement Mapper app is to assist users with animal movement data (e.g., GPS relocations) to define seasonal migration periods for caribou (and other ungulate species). Currently, the app works best for defining segments where rapid movements occurs, for example during spring and fall migration periods.

## Data requirements

The Movement Mapper requires animal movement data and, optionally, a segments table.

### Movement data (csv)

The movement data provides information on the location of individual animals along with a timestamp for each relocation. It should be in CSV format and include at least the following attributes:

- **id** - animal identification
- **timestamp** - timestamp
- **longitude** - longitude
- **latitude** - latitude

### Segments table (csv)

The segments table provides information on the start and end dates for migration periods for each individual animal, year, and season. It should also be in CSV format. If the table does not exist, an empty table will be created based on the animal movement data. The segments table consists of 5 attributes:

- **Id** - animal identification
- **Year** - year of GPS relocations
- **Migration** - Spring or Fall migration period
- **Start** - migration period start date in year-month-day format e.g., 2025-05-15
- **End** - migration period end date in year-month-day format e.g., 2025-06-30

## Segmentation workflow

### Upload data

- Upload movement data using the "Movement data (csv)" button
- Upload segments table using the "Segments table (csv)" button (optional)

### Select Caribou and Year

- Use the drop down boxes to select and individual caribou and a year.
- If you do not want to define segments for Spring or Fall migration periods for a given Id/Year combination, just unselect the "Spring migration" or "Fall migration" checkbox.
- If the fall migration period extends into the following year, just select the "Extend fall season into next year" checkbox located in the sidebar.

### Define segments using sliders

- Use the Spring and Fall sliders to define start and end dates.
- Click on the "Save segments" button after defining segments for each Id/Year combination.

### Download final segments

Click on the "Download final segments" button when you are done defining segments for all individuals, years, and migration periods of interest.


## Notes

- NSD is calculated for each caribou for each year, starting on Jan 1st.
- Start and end dates are calculated form day-of-year minus 1 since year starts on Jan 1st.
