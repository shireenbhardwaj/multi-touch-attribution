# Multi-Touch Attribution Analysis

## Project Introduction

This project focuses on multi-touch attribution in digital marketing, aiming to analyze how different marketing channels contribute to user conversion. The motivation behind this project is to understand customer journeys, optimize marketing spend, and improve conversion rates by analyzing user interactions across multiple touchpoints.

## Dataset Information

The dataset consists of 10,000 user interactions and was sourced from Kaggle. The dataset includes the following columns:

- **User ID:** Unique identifier for each user.

- **Timestamp:** The date and time of the interaction.

- **Channel:** The marketing channel through which the interaction occurred (e.g., Email, Search Ads, Social Media, Direct Traffic).

- **Campaign:** The specific marketing campaign linked to the interaction.

- **Conversion:** Whether the user converted ("Yes" or "No").

- **Interaction_Count:** The total number of interactions a user had before converting (or not converting), derived from the dataset.

## Problems to Solve

The primary questions addressed in this analysis include:

- How does the number of interactions affect the probability of conversion?

- Which marketing channels contribute the most to user conversion?

- What is the optimal number of interactions before a user is likely to convert?

- Are there patterns in conversion behavior across different campaigns?

## Data Cleaning

To prepare the dataset for analysis, the following data cleaning steps were performed:

- **Handled missing values:** Checked and addressed any null or incomplete data.

- **Standardized data formats:** Converted timestamps into a uniform format for time-based analysis.

- **Created the Interaction_Count feature:** Aggregated interactions per user to quantify engagement levels.

- **Converted categorical variables:** Transformed "Yes" and "No" in the Conversion column into binary values (1 and 0) for modeling.

## Analysis

After data cleaning, the following analyses were conducted:

- **Exploratory Data Analysis (EDA):** Summary statistics, missing values, unique values, and general dataset structure.

  ![image](https://github.com/user-attachments/assets/2db23518-ce76-456a-a959-988ba6911ad6)


- **Logistic Regression Model:** Examined how the number of interactions impacts conversion probability.

   ![image](https://github.com/user-attachments/assets/a06b790e-c3f7-4d96-821e-6b096bad84f9)

- **XGBoost Model:** Implemented an extreme gradient boosting model to enhance conversion prediction accuracy. XGBoost was chosen for its ability to handle complex relationships in the data and improve predictive power. Feature importance analysis from XGBoost helps identify the most influential factors driving conversions.

  ![image](https://github.com/user-attachments/assets/4e3cb704-90a4-4a26-8a42-09a97e47b784)

- **Channel Performance Analysis:** Determined which marketing channels are most effective.

- **Customer Journey Analysis:** Evaluated the number of touchpoints required for a successful conversion.
After data cleaning, the following analyses were conducted:

Rows added/removed:

- Created the Interaction_Count feature based on user engagement history.

- Dropped duplicate interactions to ensure unbiased results.

## Conclusion
![image](https://github.com/user-attachments/assets/3f59f330-3ed0-4fbf-9b39-dbb13004db0f)

From the analysis, the key takeaways include:

- The highest conversions occur at 3 to 4 interactions, indicating users are more likely to convert after a few engagements rather than immediately. Beyond 4 interactions, conversion rates drop sharply, suggesting diminishing returns.
- Each additional interaction doubles the likelihood of conversion up to the 4th touchpoint, with the 4th interaction converting twice as well as the 3rd, the 3rd better than the 2nd, and so on. Beyond this, conversion lift diminishes, indicating a need to shift strategies from engagement to urgency.

## Business Implications & Recommendations
- **Optimize Early Engagement (1-4 Touchpoints):** Since conversions peak at 3-4 interactions, marketing efforts should focus on delivering the most impactful messaging within this window. Use personalized content, strong CTAs, and retargeting ads to accelerate decision-making.
- **Limit Over-Retargeting:** As conversion rates drop sharply beyond 4 interactions, avoid excessive follow-ups that may lead to user fatigue. Implement frequency capping on ads and adjust messaging to prevent disengagement.
- **Shift from Engagement to Urgency After 4 Touchpoints:** Beyond the 4th interaction, transition marketing strategies to urgency-driven tactics such as limited-time discounts, exclusive offers, or scarcity messaging to nudge hesitant users toward conversion.
- **Leverage Predictive Analytics & A/B Testing:** Use data-driven insights to identify the optimal moment for conversion and refine engagement strategies. A/B test different messaging sequences to determine which combinations maximize conversions within the first 4 interactions.
- **Channel-Specific Optimization:** Identify which marketing channels drive the highest engagement within 1-4 touchpoints and allocate budget accordingly to maximize ROI while reducing inefficient touchpoints.
