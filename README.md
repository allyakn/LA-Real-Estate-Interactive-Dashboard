# Los Angeles Renovation Permit Analysis & Dashboard

This project examines Los Angeles building permit data to uncover patterns in renovation activity across neighborhoods and over time.  
The objective is to translate permit records into practical insights that help identify active renovation markets, timing trends and areas associated with higher renovation investment levels

## 📊 Overview

**Data Source:**  
Los Angeles Building Permit Records

**Unit of Analysis:**  
Each record corresponds to an individual building permit issued in Los Angeles.

**Key Variables:**

- **Location:** zip code, census tract, latitude, longitude  
- **Timing:** issue date, issue year, status date  
- **Permit Attributes:** permit type, permit sub-type, permit status  
- **Investment Indicator:** declared permit valuation  
- **Engineered Fields:** time elapsed between issuance and status

## 🔎 Research Questions

This project focuses on answering the following questions:

1. Which areas of Los Angeles experience the highest concentration of renovation permits?
2. How does renovation activity fluctuate over time, and what does this suggest about market conditions?
3. Which neighborhoods are associated with higher average renovation valuations?
4. How do patterns differ between high-frequency renovation markets and high-value renovation markets?

## 🧠 Methodologies

### 1. Data Preparation
- Extracted permit records using Snowflake Snowpark
- Standardized date formats and valuation fields
- Parsed geographic coordinates from raw text fields
- Created time-based and duration-related features

### 2. Descriptive Analysis
- Evaluated the distribution of permit valuations
- Identified common renovation cost ranges as well as high-end outliers
- Used summary statistics to characterize overall renovation activity

### 3. Spatial Aggregation
- Aggregated permit counts and average valuations by zip code
- Compared neighborhoods by renovation volume and investment intensity
- Highlighted geographic clustering of renovation activity

### 4. Temporal Analysis
- Grouped permits at a monthly level to assess changes over time
- Examined periods of growth, decline, and volatility in renovation activity
- Used permit volume as an indicator of market momentum

### 5. Interactive Visualization
- Developed a Streamlit dashboard to explore results dynamically
- Implemented filters for time range, permit type, and location
- Displayed summary metrics and comparative charts to support interpretation

## 🛠️ Technologies

- Python  
- SQL  
- Snowflake Snowpark  
- Pandas & NumPy  
- Streamlit   

## 🎯 Key Insights

- Renovation permits are not evenly distributed across the city, with certain zip codes showing sustained activity.
- Renovation volume exhibits cyclical behavior, including periods of increased volatility.
- Neighborhoods with higher average permit valuations tend to reflect more capital-intensive renovation projects.
- Permit data serves as a useful proxy for understanding local investment behavior and development activity.

## 📁 Project Components

- **Data Pipeline:** `Data-Pipeline.ipynb`  
- **Interactive Dashboard:** `LA-Dashboard.png`  

## 🔮 Future Enhancements

- Integrate geospatial maps for neighborhood-level visualization
- Analyze permit approval duration and workflow delays
- Automate data refresh and pipeline execution
- Extend analysis to contractor and permit sub-type behavior
