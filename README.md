# Exploratory-Data-Analysis-EDA-on-Food-Service-Data
# Exploratory Data Analysis on Food Service Data

## Introduction
This repository contains an Exploratory Data Analysis (EDA) project focused on food service data. The objective is to analyze operational efficiency, food waste management, and the impact of environmental and staffing conditions in a kitchen or cafeteria setting.

## Dataset Overview
The dataset includes key variables such as daily meal counts, staffing levels, weather conditions, staff experience, special events, and detailed food waste data categorized by type.

### Columns in the dataset:
- `ID`: Unique identifier for each record.
- `date`: Date of observation.
- `meals_served`: Number of meals served on that day.
- `kitchen_staff`: Number of kitchen staff working.
- `temperature_C`: Recorded temperature (°C).
- `humidity_percent`: Humidity percentage.
- `day_of_week`: Numeric representation of the day (0 = Sunday, …, 6 = Saturday).
- `special_event`: Binary flag indicating a special event (1 = event, 0 = no event).
- `past_waste_kg`: Amount of food waste in kilograms from previous days.
- `staff_experience`: Experience level of kitchen staff (Beginner, Intermediate, etc.).
- `waste_category`: Category of food waste (Meat, Dairy, Vegetables, etc.).

## Data Cleaning
### Addressing Label Inconsistencies
- Standardized categorical labels (`staff_experience` and `waste_category`) by converting text to lowercase and mapping cleaned strings to proper labels.
- Corrected textual representation of numbers in `special_event` and `kitchen_staff`.

### Handling Missing Values
- Used median imputation for `meals_served`, mean imputation for numerical columns, and placeholder values for categorical columns (`Unknown`).

### Checking for Duplicates
- Verified that there were no duplicate rows in the dataset.

## Exploratory Data Analysis (EDA)
### Summary Statistics
Generated statistical summaries using `describe()` to explore numerical distributions.

### Data Visualization
- **Histograms:** Visualized distributions for `meals_served`, `temperature_C`, `humidity_percent`, and `past_waste_kg`.
- **Boxplots:** Identified outliers in numerical categories.
- **Bar Plots:** Showed distributions for `staff_experience` and `waste_category`.
- **Heatmap:** Examined correlations between key variables.

### Outlier Treatment
- Applied log transformation for `meals_served` to compress high values.
- Used interquartile range (IQR) clipping for extreme temperature values.

## Hypothesis Testing
### Impact of Kitchen Staff on Food Waste
- Conducted one-way ANOVA to test whether the number of kitchen staff affects food waste.
- Results: Statistically significant difference in average food waste between different staff levels.

### Special Events and Food Waste
- Performed t-tests comparing food waste on special event days vs. non-event days.
- Results: No significant difference in food waste due to special events.

## Key Insights & Recommendations
### Insights
- No significant correlation between temperature, humidity, and food waste.
- Meal demand surges on weekends.
- Staff levels do not strongly influence food waste.

### Recommendations
- Optimize staff based on efficiency rather than waste reduction.
- Implement automated meal tracking systems.
- Improve inventory management and food storage techniques.
- Develop strategic meal planning based on demand forecasting.


