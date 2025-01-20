# City Bike Analysis

# CitiBike Data Analysis


## Project Overview

Urban traffic congestion, exacerbated post-COVID due to increased reliance on personal vehicles, has highlighted the need for efficient, cost-effective, and eco-friendly transportation options. CitiBike, a bicycle-sharing service in New York City and New Jersey, aims to bridge the gap in urban mobility by providing electric and classic bike options for commuters and tourists alike.

This project analyzes CitiBike trip data from 2022 to optimize fleet deployment and station management. By understanding rider preferences and station usage patterns, we aim to maximize ridership and revenue while maintaining an equitable distribution of e-bikes.

---

## Goals

- Analyze usage patterns by member type (casual and subscribed users).
- Identify high-demand stations and optimize fleet allocation.
- Study ride durations and rider behaviors to enhance user experience.
- Propose actionable recommendations to improve service efficiency and rider satisfaction.

---

## Dataset

The dataset used for this analysis is CitiBike's public trip history data for the year 2022, available at [CitiBike System Data](https://citibikenyc.com/system-data).

### Key Features

- **ride_id**: Unique identifier for each trip.
- **rideable_type**: Type of bicycle used (electric_bike, classic_bike, docked_bike).
- **started_at, ended_at**: Start and end timestamps of trips.
- **start_station_name, start_station_id**: Name and ID of the starting station.
- **end_station_name, end_station_id**: Name and ID of the ending station.
- **start_lat, start_lng, end_lat, end_lng**: Latitude and longitude of start and end locations.
- **member_casual**: Rider type (member or casual).

---

## Tools and Libraries

- **Programming Language**: Python
- **Libraries**:
  - `pandas`: Data manipulation and cleaning
  - `matplotlib`, `seaborn`: Data visualization
  - `folium`, `plotly`: Interactive map visualizations
  - `numpy`: Numeric computations
  - `glob`: File handling for multiple datasets

---

## Data Preprocessing

1. **Data Cleaning**:
   - Checked for and handled null values.
   - Ensured consistent data types (datetime, numeric).
   - Extracted and formatted relevant features (e.g., dates, times, ride duration).

2. **Feature Engineering**:
   - Derived `ride_duration` and categorized it into blocks for analysis.
   - Segmented rides by time (day, month, and day of the week).

3. **Data Consolidation**:
   - Combined multiple CSV files into a single dataset for analysis.

---

## Visualizations and Insights

### Key Findings

1. **Seasonality**:
   - Ridership peaks during summer and fall (May to October).

2. **Weekly Trends**:
   - Members: Heavy weekday usage, likely for daily commutes.
   - Casual riders: Higher usage during weekends.

3. **Ride Duration**:
   - 85% of trips are short (0-20 minutes), indicating frequent short-distance travel.

4. **Station Analysis**:
   - Most popular stations for starts and ends were identified.
   - Common routes were visualized using `folium` maps.

### Recommendations

1. **Weekend Membership Plans**:
   - Offer budget-friendly plans targeting casual users to increase revenue.

2. **Expand Electric Bike Fleet**:
   - Electric bikes are underutilized but have high potential with targeted pricing and deployment.

3. **Station Upscaling**:
   - Increase docking capacity at high-demand stations like Grove St PATH and 12 St & Sinatra Dr N.

---

## Challenges and Bias

- Data limitations:
  - Missing contextual data (e.g., weather conditions, number of docks available).
  - No demographic information of users.
- Recommendations based solely on available 2022 data.
- Future work could integrate external APIs or datasets to address these gaps.

---

## How to Run the Project

1. Clone this repository.
2. Place all CitiBike data CSV files for 2022 in the `Data/` folder.
3. Install required Python libraries using the command:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the analysis notebook in Jupyter or any Python IDE.
5. Outputs include visualizations and an interactive map (`route_map.html`) for top ride paths.

---

## Citation

- Data Source: [CitiBike NYC Trip Data](https://citibikenyc.com/system-data)
- Created in: [Deepnote](https://deepnote.com)

---

## Contact

For questions or contributions, feel free to contact any of the authors listed above.
