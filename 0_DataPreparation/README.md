# Data Preparation

# 1. Data Cleaning
   - Handling Missing Values: Missing data is identified and either imputed using statistical methods (e.g., mean or median replacement) or removed if deemed unnecessary.
   - Removing Duplicates: Duplicate entries are detected and removed to avoid redundant data points that could bias the model.
   - Data Type Standardization: Variables are converted to appropriate data types (e.g., datetime conversion for timestamps, categorical encoding where necessary).

#  2. Feature Engineering
   - Creation of New Features: Additional variables are derived from the existing dataset to improve model performance.
   - Transformation of Variables: Numerical transformations such as logarithmic scaling, min-max normalization, or binning categorical values are applied.
   - Temporal Features: Extracting time-based attributes such as day of the week, holidays, or trends in demand based on historical data.

#   3. Data Standardization
   - Normalization: Features are rescaled to have similar ranges to prevent large-scale variables from dominating model training.
   - Encoding Categorical Variables: One-hot encoding or label encoding is used where necessary.
   - Scaling Numerical Features: Using standard scaling techniques to ensure all features contribute proportionally to the model.

#  4. Integration of External Data Sources
   - Weather Data: Weather conditions such as temperature, precipitation, and humidity are integrated to account for their influence on bakery sales.
   - Local Events and Sports Games: Home matches of Holstein Kiel and THW Kiel are added as additional factors affecting customer behavior.
   - School Holidays: The dataset includes information on school vacations, which can influence sales patterns due to changes in consumer demand.

#  5. Final Data Processing
   - A consolidated Pandas DataFrame is created containing all cleaned and enriched data.
   - The prepared dataset is saved in a structured format to be used in subsequent modeling phases.
   - Summary statistics and visualizations are generated to validate the integrity of the processed data.

This comprehensive data preparation ensures that the input for machine learning models is clean, structured, and enriched with meaningful external factors. The processed dataset serves as the foundation for accurate sales forecasting and performance evaluation.

