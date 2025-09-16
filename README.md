# EDA-on-Flight-Price-Prediction
## Project Objective
This project focuses on predicting flight ticket prices based on various features such as airline, source, destination, duration, and other relevant parameters. The dataset was cleaned, analyzed, and feature engineered to build predictive models that can estimate flight fares.

## Dataset used
- <a href="https://github.com/Suryxbg/EDA-on-Flight-Price-Prediction/blob/main/Data_Train.xlsx">Dataset 1</a>

- <a href="https://github.com/Suryxbg/EDA-on-Flight-Price-Prediction/blob/main/Test_set.xlsx">Dataset 2</a>

## Key Questions (KPIs)
During the analysis, the following key questions were addressed:

- Which airlines have the highest average ticket prices?
- Which source–destination routes are the most expensive?
- How does the number of stops affect ticket price?
- How do prices vary with the day of journey?
- Does the month/season of travel impact ticket price significantly?
- Is there a relationship between flight duration and ticket price?

## Dashboard

## Process / Workflow (from your notebook)

- Combined them into a single dataframe (df_final) for consistent preprocessing.
- Date & Time Feature Engineering
- Converted data types to integers for modeling.
- Extracted Arrival Hour & Minute from Arrival_Time.
- Extracted Departure Hour & Minute from Dep_Time.
- Converted Total_Stops into numerical format:
  - non-stop → 0
  - 1 stop → 1
  - 2 stops → 2
  - 3 stops → 3
  - 4 stops → 4
  - missing values (NaN) mapped to 1 stop.
- Applied One-Hot Encoding on categorical features like:
  - Airline
  - Source
  - Destination
- Cleaned and structured duration/time-based columns.
- Removed unnecessary columns after transformation.

## Project Insights (from EDA)

- Price Distribution
  - Flight prices are right-skewed, with most tickets in the lower-to-mid range.
  - A few extreme outliers exist where ticket prices are very high.

- Impact of Stops
  - Ticket price increases as the number of stops increases.
  - Non-stop flights are generally cheaper compared to 1-stop, 2-stop, or 3-stop flights.

- Airline-wise Pricing
  - Full-service airlines (e.g., Jet Airways, Air India) charge significantly higher fares compared to budget carriers (e.g., Indigo, SpiceJet).
  - Premium airlines dominate the higher end of the price distribution.

- Route & Connectivity
  - Routes with more layovers tend to be costlier.
  - Popular routes with frequent connectivity have more competitive prices.

- Time-based Factors
  - Prices vary depending on departure and arrival times.
  - Certain times of the day (e.g., early morning, late night) show lower fares compared to peak travel times.
  - Month and season also influence prices — some months show clear demand-driven spikes.

## Conclusion

- Flight ticket prices are influenced by multiple factors, with airline, number of stops, route, and timing being the most critical drivers.
- Full-service airlines and multi-stop flights are consistently more expensive.
- Feature engineering of date/time and categorical variables improved the model’s ability to explain variance in price.
- Predictive modeling confirmed that tree-based models (Random Forest, XGBoost) outperform simple regression methods, delivering better accuracy.
- The insights can help both airlines (for pricing strategies) and passengers (for booking optimization).

