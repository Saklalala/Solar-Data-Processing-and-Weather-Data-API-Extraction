# Solar-Data-Processing-and-Weather-Data-API-Extraction

## Project Overview
This project extends the analysis of the Ausgrid Solar home electricity dataset by integrating historical weather data for load forecasting research. The original dataset contains electricity consumption and solar generation data from 300 customers in New South Wales, Australia.

## Data Processing Pipeline

### 1. Data Preprocessing
- Filtered prosumer users (households with solar panels) based on daily/hourly GG (generation) and GC (consumption) patterns
- Excluded users with CL (controlled load) usage
- Created separate daily and hourly datasets containing:
  - User ID
  - Postcode
  - Generation (GG)
  - Consumption (GC)

### 2. Geolocation Integration
- Implemented geocoding API integration to extract latitude and longitude coordinates based on postcodes
- Optimized API calls by processing unique postcodes to improve efficiency
- Generated comprehensive dataset with geographical coordinates

### 3. Weather Data Integration
- Utilized OpenWeatherMap API to fetch historical weather data
- Mapped weather data to user locations using extracted coordinates
- Current implementation includes test data for 2024-2025 (prepared for API validation)

### 4. Data Visualization
- Implemented basic visualizations to analyze:
  - Weather patterns by location
  - Energy generation/consumption correlations
  - Geographical distribution of prosumers

## Current Status
- Completed data preprocessing and cleaning
- Successfully implemented weather data integration pipeline via OpenWeatherMap API service
- Prepared dataset for load/net load forecasting

## Next Steps
- Implement load forecasting models
- Expand weather data coverage to original timeframe (2010-2013)
- Enhance visualization suite
- Develop net load forecasting capabilities

## Technical Implementation
- Python-based data processing pipeline
- Jupyter Notebooks for analysis and visualization
- API integration for geocoding and weather data
- Data processing optimization for large-scale dataset handling

## Dataset Attribution
This work builds upon the Ausgrid Solar home electricity dataset, originally created by E. L. Ratnam, S. R. Weller, C. M. Kellett, and A. T. Murray, and published in "Residential load and rooftop PV generation: an Australian distribution network dataset," International Journal of Sustainable Energy, 2017. DOI: 10.1080/14786451.2015.1100196

###Download:
  - 1 July 2012 to 30 June 2013: https://www.ausgrid.com.au/-/media/Documents/Data-to-share/Solar-home-electricity-data/Solar-home-half-hour-data---1-July-2012-to-30-June-2013.zip
  - 1 July 2011 to 30 June 2012: https://www.ausgrid.com.au/-/media/Documents/Data-to-share/Solar-home-electricity-data/Solar-home-half-hour-data---1-July-2011-to-30-June-2012.zip
  - 1 July 2010 to 30 June 2011: https://www.ausgrid.com.au/-/media/Documents/Data-to-share/Solar-home-electricity-data/Solar-home-half-hour-data---1-July-2010-to-30-June-2011.zip

## License
This project is available under a CC BY 4.0 license, maintaining compatibility with the original dataset's licensing.

---
*Note: This project is part of ongoing research work in load/net load forecasting.*
