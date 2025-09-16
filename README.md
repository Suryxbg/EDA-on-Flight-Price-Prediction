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

