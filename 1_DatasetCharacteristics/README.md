# Dataset Characteristics

## Dataset Description from a Data Science Perspective

### Overview
The dataset **01_merged_data.csv** provides a comprehensive time-series dataset that integrates sales data with external influencing factors, such as weather conditions, holidays, and special events. It consists of **11,164 rows** and **19 columns**, making it a valuable resource for predictive modeling and data-driven decision-making in the context of retail and bakery sales forecasting.

### Data Schema and Features
The dataset includes a variety of feature types, which can be categorized as follows:

#### **Target Variable:**
- **Umsatz** (Sales Revenue): The dependent variable representing the daily revenue for different product categories.

#### **Time Features:**
- **Datum** (Date): A temporal index for time-series analysis.
- **wochentag** (Weekday): Encoded from 0 (Monday) to 6 (Sunday), useful for capturing weekly sales trends.

#### **Product Features:**
- **Warengruppe** (Product Category): A categorical variable identifying different product groups within the bakery.

#### **Weather Features:**
- **Bewoelkung** (Cloud Coverage): A numerical feature representing cloud cover on a scale from 0 to 8.
- **Temperatur** (Temperature in °C): A continuous feature that helps identify seasonal effects on sales.
- **Windgeschwindigkeit** (Wind Speed in km/h): Another continuous feature that might correlate with customer footfall and sales performance.
- **is_niederschlag** (Precipitation Indicator): A binary feature indicating whether it rained (1) or not (0).
- **niederschlag_intesitaet** (Precipitation Intensity): A categorical feature that classifies the level of rainfall (0 = none, 1 = light, 2 = heavy).
- **is_gewitter** (Thunderstorm Indicator): A binary feature indicating whether thunderstorms occurred on the given day (1) or not (0).
- **temperatur_cat** (Temperature Category): A discretized version of the temperature feature, grouping days into different temperature ranges.

#### **Event and Holiday Features:**
- **is_kielerWoche** (Kieler Woche Indicator): A binary variable marking whether the date falls within the Kieler Woche event, which can influence foot traffic and sales.
- **holiday_name** (Holiday Name): The name of a public holiday, if applicable; otherwise, it remains "None".
- **is_holiday** (Holiday Indicator): A binary feature marking whether the date is a public holiday (1) or not (0).
- **is_heimspiel_thw** (THW Kiel Home Game Indicator): A binary feature indicating whether the handball team THW Kiel had a home game.
- **is_heimspiel_holstein** (Holstein Kiel Home Game Indicator): A binary feature indicating whether the football team Holstein Kiel had a home game.
- **is_school_holidays** (School Holiday Indicator): A boolean variable indicating whether the date falls within a school holiday period.
- **school_holiday_name** (School Holiday Name): The specific name of the school holiday, if applicable.

### Data Quality and Preprocessing Considerations
- **Missing Values:**
  - **Umsatz (Sales Revenue):** 1,830 missing values → Requires imputation or removal depending on analysis goals.
  - **Bewoelkung (Cloud Coverage):** 135 missing values → Possible interpolation based on nearby dates.
  - **Temperatur (Temperature):** 81 missing values → Can be filled using historical weather data.
  - **Windgeschwindigkeit (Wind Speed):** 81 missing values → Similar handling as temperature.

- **Feature Engineering Opportunities:**
  - **Time-Based Aggregation:** Weekly or monthly rolling averages could be useful for trend analysis.
  - **Lagged Features:** Creating lag variables for sales, weather, or event indicators to model temporal dependencies.
  - **Interaction Features:** Examining interactions between holidays, weather, and sales to improve predictive power.

### Potential Use Cases in Data Science
- **Sales Forecasting:** Using machine learning models such as ARIMA, LSTMs, or XGBoost to predict future sales.
- **Demand Planning:** Identifying peak demand periods to optimize inventory and staffing.
- **Marketing Strategy Optimization:** Evaluating how external factors (weather, holidays, events) impact sales to fine-tune promotional campaigns.
- **Customer Behavior Analysis:** Understanding how customer purchasing patterns change with weather conditions and local events.

### Conclusion
This dataset provides a robust foundation for advanced data analysis and machine learning applications. By leveraging the available features, data scientists can build predictive models that help businesses make data-driven decisions regarding sales forecasting, demand management, and operational optimization.

