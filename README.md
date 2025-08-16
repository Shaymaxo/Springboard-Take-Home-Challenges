# Data Analysis Interview Challenge

This challenge is your opportunity to demonstrate creative and rigorous data analysis skills. You may include your code at the end of your submission or in a separate file. Incomplete solutions are also acceptable.

---

## Part 1 — Exploratory Data Analysis

The file `logins.json` contains simulated timestamps of user logins in a particular geographic location.

**Tasks:**
1. Aggregate login counts based on **15-minute intervals**.
2. Visualize the resulting time series to best characterize underlying patterns of demand.
3. Describe important features, such as daily cycles or trends.
4. Report any data quality issues you encounter.

---

## Part 2 — Experiment and Metrics Design

Two neighboring cities, **Gotham** and **Metropolis**, have complementary activity patterns:
- **Weekdays:** Gotham is most active at night; Metropolis is most active during the day.
- **Weekends:** Reasonable activity in both cities.

A toll bridge connecting the two cities encourages driver partners to remain exclusive to one city. Ultimate managers propose reimbursing toll costs to encourage drivers to serve both cities.

**Questions:**

1. **Key measure of success**  
   - Choose a metric to measure whether driver partners serve both cities.  
   - Explain why this metric is appropriate.

2. **Experiment Design**  
   Describe a practical experiment to test the effectiveness of toll reimbursement:
   - **Implementation:** How will you run the experiment?
   - **Statistical Test:** Which tests will you use to verify significance?
   - **Interpretation:** How would you interpret results and provide recommendations to city operations? Include caveats if necessary.

> Note: Gotham and Metropolis data are not included in the dataset; you can answer this without them.

---

## Part 3 — Predictive Modeling

Ultimate wants to predict **rider retention**. You are provided with a cohort of users who signed up in **January 2014**. Users are considered retained if they were **active (took a trip) in the preceding 30 days**.

**Data File:** `ultimate_data_challenge.json`

**Tasks:**

1. **Cleaning and Exploratory Analysis**  
   - Perform data cleaning and basic exploration.  
   - Visualize key patterns.  
   - Report the fraction of users retained.

2. **Predictive Modeling**  
   - Build a model to predict if a user will be active in their 6th month.  
   - Discuss your approach, alternatives considered, and potential concerns.  
   - Evaluate model validity using key metrics (accuracy, ROC AUC, etc.).

3. **Operational Insights**  
   - Briefly describe how Ultimate can use insights from your model to improve long-term rider retention.

---

## Data Description

| Column | Description |
|--------|-------------|
| `city` | City in which the user signed up |
| `phone` | Primary device used by the user |
| `signup_date` | Date of account registration (`YYYYMMDD`) |
| `last_trip_date` | Last date the user completed a trip (`YYYYMMDD`) |
| `avg_dist` | Average distance (miles) per trip in the first 30 days |
| `avg_rating_by_driver` | Rider’s average rating given by drivers |
| `avg_rating_of_driver` | Rider’s average rating of drivers |
| `surge_pct` | Percentage of trips taken with surge multiplier > 1 |
| `avg_surge` | Average surge multiplier across all trips |
| `trips_in_first_30_days` | Number of trips taken in the first 30 days |
| `ultimate_black_user` | TRUE if user took an Ultimate Black in the first 30 days; FALSE otherwise |
| `weekday_pct` | Percentage of trips occurring on weekdays |
